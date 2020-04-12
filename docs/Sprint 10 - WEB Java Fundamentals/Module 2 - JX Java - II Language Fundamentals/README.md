Metadata

# Module 2 - JX Java - II Language Fundamentals

## [Training Kit](www.example.com)

### Sprint 10 - WEB Java Fundamentals

## Objectives

Overall the student will be able to construct a Java statements using looping, branching, and collections

At the end of this module, a student should be able to:

* Craft and use for loops
* Craft and use while loops and do while loops
* Craft and use recursion
* Craft and use Java conditionals, branching, including if-then, if-then-else, and switch statements
* Craft and manipulate Collections
* Craft and manipulate Arrays Collections
* Craft and manipulate ArraysList Collections
* Craft and manipulate HashMap Collections
* Craft and manipulate HashSet Collections

### Core Objectives

* Craft and use for loops
* Craft and use Java conditionals, branching, including if-then, if-then-else, and switch statements
* Craft and manipulate Collections
* Craft and manipulate Arrays Collections
* Craft and manipulate ArraysList Collections
* Craft and manipulate HashMap Collections

### Objective to Cover if Time Permits

* Craft and use while loops and do while loops
* Craft and use recursion
* Craft and manipulate HashSet Collections

----

## Before Class

### Instructor Resources

* Repos to Keep Updated
  * [Teacher's Edition of Class LambdaJX](https://github.com/LambdaSchool/LambdaJX.git)
  * [Guided Project java-LoopingAndCollections](https://github.com/LambdaSchool/java-LoopingAndCollections.git)
  * [Module Project java-WordCount](https://github.com/LambdaSchool/java-WordCount.git)

* Guided Project Repos
  * java-EmployeeApp - Guided Project build from scratch
  * [java-LoopingAndCollections - Guided Project Solution](https://github.com/LambdaSchool/java-LoopingAndCollections.git)

* Notes to Presenter
  * Watch pacing in Guided Project.
  * Do NOT add javadocs to the Guided Project code. Those will be available in the final Repo.
  * Do NOT add other comments as well. These can be used as a guide to explain what is happening in the code. Again, these are available in the final Repo.
  * Remember this is only the second Java program we have written together. Be very explicit about each step!

### Student-Facing Resources and Materials

#### Software Needed for this Guided Project

* Java Development Kit (JDK) - at least version 11
* You choice of Text Editor

#### Previous Lessons

![Model Presentation of Guided Project](assets/novideo.png)

#### Preclass Announcements

@channel
Good Morning. Welcome to the second day of Java! You will need to have the Java Development Kit and the text editor of your choice installed for today's guided project. Today we add some useful statements to our Java knowledge. Remember to work through the Training Kit material for today. In the guided project, I assume you are familiar with the terms and concepts from the Training Kit videos and documentation!

### Training Kit Hour

* [Objective 1 - FOR Loops](Objective%201%20-%20FOR%20Loops.md)
* [Objective 2 - WHILE Loops](Objective%202%20-%20WHILE%20Loops.md)
* [Objective 3 - Recursion](Objective%203%20-%20Recursion.md)
* [Objective 4 - Branching](Objective%204%20-%20Branching.md)
* [Objective 5 - Collections](Objective%205%20-%20Collections.md)
* [Objective 6 - Collections Array](Objective%206%20-%20Collections%20Array.md)
* [Objective 7 - Collections ArrayList](Objective%207%20-%20Collections%20ArrayList.md)
* [Objective 8 - Collections HashMap](Objective%208%20-%20Collections%20HashMap.md)
* [Objective 9 - Collections HashSet](Objective%209%20-%20Collections%20HashSet.md)

#### Training Kit Announcements

< NONE >

----

## During Class

### Morning Announcements

< NONE >

#### Entry Ticket

Please take a moment to reflect on what you have previously learned and hope to learn by completing this Google Survey. Remember your responses will be read by your instructor to help guide future lessons.

* [Guided Project Entry Ticket](https://forms.gle/8aHTWdz7u87sbxR46)

#### Daily Resources

* No Guided Project Starter - built from scratch
* [Slido](https://app.sli.do/event/XXXXXXXX)
* [Zoom like](https://lambdaschool.zoom.us/j/#########)

#### Slack Message

@channel
Let's do this! The Java Class will be starting in 3 minutes at (https://lambdaschool.zoom.us/j/#########)
Please post questions to the Slido link at (https://app.sli.do/event/XXXXXXXX)

### Introduction and Hook

Let's Explore Java!

Like most languages Java has

* loops
* conditionals and branching
* collections - arrays and such

But being strongly typed and Object Oriented, these standard things do come with a twist in Java. Let's take a look!

### Purpose

Now that we have a foundation in Java, we need to add constructs that help us get the job done. So, let's do just that!

### Learning Activities

Create an application called `LoopingAndCollections` and a package called `loopingandcollections`

```BASH
<home dir><work dir>/LoopingAndCollections/src/loopingandcollections
```

Enter the code from `Dogs.java` into a file in the `loopingandcollections` folder called `Dog.java`. You will need to explain the interface Comparable and the method compareTo.

Enter the following code into a file in the `loopingandcollections` folder called `Main.java`. This is just to get started

```JAVA
package loopingandcollections;

public class Main
{
    public static void main(String[] args)
    {
        System.out.println("Welcome to Lambda School's Java Module 2!!!");
    }
}
```

Wait on these:

* the gcd method will be entered for recursion at the end of the project!
* The random is for while loops

To run our code, we go through the following steps, running these commands from the `src` directory. These are steps to repeat after each change of the source code

```BASH
javac loopingandcollections/*.java
jar cvfe loopingandcollections.jar loopingandcollections.Main loopingandcollections/*.class
java -jar loopingandcollections.jar
```

So the order is

* Convert to bytecode
* Archive to a single file
* Execute the program

Remember

* c – create new archive file with given name
* v – generate verbose output
* f – specifies the jar output file to be created
* e – sets the main class also called the entry point

#### Working with the Objective: Craft and manipulate Collections

In general we are working with Collections using looping and branching

#### Working with the Objective: Craft and manipulate Arrays Collections

Enter the parts related to Arrays, section by section explaining as you go along

#### Working with the Objective: Craft and use for loops

* [Check for Understanding CFU - Google Form]()

#### Back to Working with the Objective: Craft and manipulate Arrays Collections

* [Check for Understanding CFU - Google Form]()

#### Working with the Objective: Craft and manipulate ArraysList Collections

Enter the parts related to ArrayLists, section by section explaining as you go along

#### Working with the Objective: Craft and use Java conditionals, branching, including if-then, if-then-else, and switch statements

* [Check for Understanding CFU - Google Form]()

#### Back to Working with the Objective: Craft and manipulate ArraysList Collections

* [Check for Understanding CFU - Google Form]()

#### Working with the Objective: Craft and manipulate HashMap Collections

Enter the parts related to HashMaps, section by section explaining as you go along

* [Check for Understanding CFU - Google Form]()

#### Back to Working with the Objective: Craft and manipulate Collections

* [Check for Understanding CFU - Google Form]()

### Objective to Cover if Time Permits

#### Working with the Objective: Craft and manipulate HashSet Collections

Enter the parts related to HashSets, section by section explaining as you go along

* [Check for Understanding CFU - Google Form]()

#### Working with the Objective: Craft and use recursion

Enter the parts related to Recursion, section by section explaining as you go along

* [Check for Understanding CFU - Google Form]()

#### Working with the Objective: Craft and use while loops and do while loops

Enter the parts related to Recursion, section by section explaining as you go along

* [Check for Understanding CFU - Google Form]()

#### Conclusion

##### Review what we just learned

Today we covered some fundamental constructs of Java, useful statements we will be using as we go forward!

* Collections
* Loops
* Branching

##### How is this related to tomorrow's topic

* Tomorrow we will look at more Object Oriented Aspects of Java, especially related to inheritance and open and closed principles!
  * Interfaces
  * Abstract classes
  * Lambda Expressions

----

## After Class

### Introduce Module Project

* Remember it is based on what we did in the guided project!
* Just about every Java interview I have had has included an engineering challenge based on today's module project. So why not practice it now!
* [Word Count Module Project](https://github.com/LambdaSchool/java-WordCount.git)
  * [Module Project Solution and Rubric](https://github.com/LambdaSchool/LambdaJX/tree/master/solutions/Module%20Solutions/Sprint%2010%20-%20WEB%20Java%20Fundamentals/Module%202%20-%20JX%20Java%20-%20II%20Language%20Fundamentals)

### Exit Ticket

Please take a moment to reflect on what you have learned in today's Guided Project. Remember your respond will be read by your instructor to help guide future lessons.

* [Guided Project Exit Ticket](https://forms.gle/wokWRJonaLSWGnMA6)
