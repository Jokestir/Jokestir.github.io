---
title: Singleton Design Pattern
layout: page
sort: 2
---

### Problem : Design a class so that only **one** instance of it is available all the time

The class whose only one instance is available all the time is called a singleton class.

Example: Earth, Mars etc.


### Design

There are two ways to design singleton

1. Make constructor private. Expose static factory method which returns singleton

2. Single field enum.

#### First Design

Step 1 : Mark constructor private.

Step 2  : Declare Private static final reference var Earth

Step 3  :  Declare static factory method which returns singleton

```java

	public class Earth{

			// Step 2. static final private ref var.
            private static final Earth instance = new Earth();

            //  Step1. private constructor
			private Earth(){}

			// Step 3 : static factory method
			public static Earth getInstance(){
				return instance;
			}

	}

```


This method is susceptible to reflection attacks by using reflection.