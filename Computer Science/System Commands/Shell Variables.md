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