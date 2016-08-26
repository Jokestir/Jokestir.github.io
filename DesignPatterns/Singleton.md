---
title: Singleton Design Pattern
layout: page
sort: 2
---

### Problem : Design a class so that only **one** instance of it exists ever.

The class whose only one instance is available all the time is called a singleton class.

Example: Earth, Mars etc.


### Design

#### Design 1 - Make constructor private and have a static factory method.

Step 1 : Mark constructor private.

Step 2  : Declare Private static final reference var Earth

Step 3  :  Declare static factory method which returns singleton

{% gist Jokestir/138cd6121c842ae18e9a620bac68ebc8 %}



**This method is susceptible to reflection attacks**.


#### Design  2 - Have a single element enum

Code


```java

	public enum Earth{

		INSTANCE;

		public void goRoundTheSun(){

		}

	}

```


This method is reflection safe.

Though less used, this method is the best.


### Real Time Use

Example 1: Logger class to log errors and events. There should only be one per system. Hence singleton.

Example 2: Manager type classes like WiFiManager. Or Controller.


#### Tester Class Code

```java

	public class SingletonTest{

		public static void main(String[] args){

           Earth e1 = Earth.getInstance();

		   Earth e2 = Earth.getInstance();

		   System.out.println(e1==e2);

		   //Above statement should always return true for singleton.

		}
	}

```


[TL;DR]({{ site.url }}/assets/singleton_tl_dr.png)