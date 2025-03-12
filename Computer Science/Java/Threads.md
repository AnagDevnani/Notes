# Creating a Thread <font color=red>how tf do you CREATE a thread</font>

## using `extends`
``` java
public class Multithreading extends Thread{
	public void run(){  //override
		for (int i=1; i<=5; i++){
			System.out.println(i);
			try{
				thread.sleep(1000) //here the parameter is time in ms
			}
			catch(InterruptException e){}
		}
	}
	public static void main(String[] args){
		Multithreading mything = new Multithreading();
		mything.run();
		mything.start();
		Multithreading mything1 = new Multithreading();
		mything1.start();
		mything1.run();
	}
}
```


## using `implements`
```java
public class Multithreading implements Runnable{
	... //same code as extends
	public static void main(String[] args){
		Multithreading mything = new Multithreading();
		Thread mythread = new Thread(mything);
		mythread.start();
	}
}
```

# Lab program 
```java
// Write a program which creates 2 threads, one thread displaying "BMS College of Engineering" once every ten seconds and another displaying "CSE" once every two seconds. 
```