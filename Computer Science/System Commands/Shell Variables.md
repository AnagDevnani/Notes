Frequently used shell variables:
- `$USERNAME` $\sim$ `$USER`
- `$HOME`
- `$HOSTNAME`
- `$PWD`
- `$PATH`

also bultins: `printenv`, `env`, `set`

special shell vars:
- `$0`: name of the shell
- `$$`: pid of the shell
- `$?`: return code of the previously run program
- `$-`: flags set in the shell (bash)

### flags set in bash:
- `h`: locate and hash commands
- `B`: brace expansion enabled
- `i`: interactive mode
- `m`: job control enabled.
- `H`: ! style history substitution enabled
- `s`: commands are read forom stdin.
- `c`: commands are read from arguments.

shell variables will be interpreted even through double quotes (`""`) but not through single quotes (`''`)

backslash can be used as an escape character.
e.g: `"\$HOSTNAME"`

this backslash can also be used to escape aliases

# Process Management
- `sleep`: takes away control for a set amount of seconds.
- `coproc`: sends a process to the background (creates a coprocess)
- `fg`: foreground
- `kill` and `(ctrl+c)`: kills a command by its pid
- `jobs`: lists all the processes running in the background (shell builtin)
- `ps`: lists active processes of the terminal
    - `--forest`: shows child processes.
- `top/htop`: lists system info and all active processes.
- `(ctrl+z)`: suspeds a program (and sends it to the background).

## Child Shells
e.g. `bash -c "echo \$-"`

here `-c` is the argument given to `bash` to create a child process.

The reason for using the escape character, `\` is so it is not evaluated before it is passed to the child shell.

## Explanation of bash arguments
- `bash -H`: stands for histroy and documentation can be accesses by `man history`
    - `history`: lists the commands executed with their sequence.
        - the desired command can be executed using `!n` where $n$ is the $n^{\text{th}}$ command executed.

- `bash -B`: brace expansion
    - if enabled:
        - `echo {a..z}` will return `a b c ... z`
        - `echo D*` will return all files starting with 'D'
        - `ps -e`: lists the processes that are running systemwide.
        - `bc`: bench calculator.

- When enclosing a command in parenthesis `()`, the command is executed in a subshell and then returned to the parent shell.

- `$BASH_SUBSHELL`: variable that holds the shell level or depth. basically stores the number of subshells.

# File Descriptors
linux commands have 3 file descriptors:
1. `stdin(0)`
2. `stdout(1)`
3. `stderr(2)`

```mermaid
flowchart LR;
s[stdin]-->c<command>
c-->so[stdout]
c-->se[stderr]
```

These descriptors can be redirected or recombined.

example:

- `command > file1`
    - writes stdout of `command` to `file1`.
    - `file1` will be overwritten.
    - if `file1` does not exist, it will be created.

- `command >> file1`
    - appends stdout of `command` to `file1`
    - if `file1` does not exist, it will be created.

**Note:** `cat` when provided with no options or filenames, will read from stdin.

**Note:** `ls -R`: Recursively lists files.

- `command 2> file1`
    - write stderr to `file1`
    - `file1` will be overwritten.
    - if `file1` does not exist, it will be created.

- `command > file1 2> file2`
    - writes stdout to `file1` and stderr to `file2`
    - `file1` and `file2` will be overwritten.
    - if `file1` and `file2` do not exist, they will be created. 

- `command < file1`
    - writes stdin to `file1`
    - `file1` will be overwritten.
    - if `file1` does not exist, it will be created.

- `command > file1 2> &1`
    - redirects both stdout & stderr to `file1`
    - `file1` will be overwritten.
    - if `file1` does not exist, it will be created.

**Note:** `command > file1 2> file1` will not work because error is redirected first and is then overwritten by stdout.

- `command1 | command2`
    - stdout of command1 is inputted as stdin of command2.
    - The stderr of both commands are returned together.

- `command1 | command2 > file1`
    - stdout of command1 will become stdin for command2 and stdout of command2 is written to `file1`.
    - stderr are combined
    - `file1` will be overwritten.
    - if `file1` does not exist, it will be created.

- `/dev/null`: file intended to be used as a black hole. i.e. a sink for output to be discarded.

- `tee`: creates a copy of stdin and redirects it without touching the original.
    - e.g. `command | tee file1` here stdout of command is sent to file1 and to the console.


# Shell Variables (contd.)
Naming Rules:
- can't start witha a number
- mix b/w Alphanumeric characters and underscore (`_`)
- No space around `=` sign

e.g. `myvar="value string"`

## Exporting a variable
exporting can be done during declaration or after variable definition.

e.g. `export myvar="value string"` 
or `export myvar`

## Using variable values
`$myvar`

`${myvar}`

`"${myvar}_something"`

## Removing a variable
`unset myvar`

or

`myvar=`

## Test if a variable is set
`[[ -v myvar ]];`
`echo $?`

`0`: variable is set
`1`: variable is not set

## Testing if a variable is not set:
`[[-z ${myvar+x} ]];`
`echo $?`

`0`: variable is not set
`1`: variable is set

## Using default value
i.e. if a variable is not set then use "default" as its default value

i.d.k. how this is different from just initializing `myvar="default"`

`echo ${myvar:-"default"}`

if `myvar` is set: display its value

else: display `"default"`

## Setting a default value
i.e. if a variable is not set then set "default" as its default value

`echo ${myvar:="default"}`

if `myvar` is set: display its value

else: set `myvar="default` and display its new value (`"default"`)

## Reset value if variable is set
i.e. is variable is set, then set "default" as its value.

`echo ${myvar:+"default"}`

if `myvar` is set:<br>
    &emsp;set `"default"` as its value<br>
    &emsp;display its new value.<br>
else:<br>
&emsp;display null.

## Listing variable names

`echo ${!H*}`

list of names of shell variables that start with H.

## Length of string value

Display length of string value of the variable `myvar`

`echo ${#myvar}`

if myvar is not set, display 0.

## String slicing
`echo ${myvar:5:4}`

here `5` is the `offset` and `4` is the `slice length`

this command displays 4 chars of string value of `myvar` skipping the first 5 chars.

## Matching pattern from string value of variable
`echo ${myvar#pattern}` match once

`echo ${myvar##pattern}` match all

## Keeping matching pattern
`echo ${myvar%pattern}` match once

`echo ${myvar%%pattern}` match all

## Replace matching pattern
`echo ${myvar/pattern/string}` match once & replace with `string`

`echo ${myvar//pattern/string}` match max possible & replace with `string`

## Replacing matching pattern by location
`echo ${myvar/#pattern/string}` match at the beggining & replace with `string`

`echo ${myvar/%pattern/string}` match at the end & replace with `string`

## Changing case of string value
`echo ${myvar,}` change first character to lower case

`echo ${myvar,,}` change all characters to lower case


`echo ${myvar^}` change first character to upper case

`echo ${myvar^^}` change all characters to lower case

## Restricing value types (declare)
`declare -i myvar` Only integers

`declare -l myvar` Only lowercase

`declare -u myvar` Only uppercase

`declare -r myvar` Read-only

## Removing declaration / unrestricting
`declare +i myvar` Remove integers restriction

`declare +l myvar` Remove lowercase restriction

`declare +u myvar` Remove uppercase restriction

**Note: **`declare +r` does not work as a variable once set as read-only cannot be unset 


## Arrays [Indexed]

`declare -a arr`
define `arr` as an indexed array

`$arr[0]="value"`
set value of element with index 0 in the array.

`echo ${arr[0]}`
value of element with index 0

`echo ${#arr[@]}`
number of elements in the array

`echo ${!arr[@]}`
All indices used in the array
