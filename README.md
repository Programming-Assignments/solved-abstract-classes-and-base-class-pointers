Download Link: https://assignmentchef.com/product/solved-abstract-classes-and-base-class-pointers
<br>
This is a problem with abstract classes and base class pointers. There will be <strong>two</strong> classes:

<ol>

 <li>Abstract Base Class: ProSportsTeam</li>

 <li>Derived Class: Football or other pro team sport of your choice.</li>

</ol>

The UML for the abstract base class is given below. Methods in italics should be made into pure virtual functions. This means that the derived class MUST have an implementation of these methods. Note: you should code the constructors even though this base class will never be instantiated; the constructors can be used by the derived class. I will leave it to you to decide if you need setters and getters for your purposes.

Create <strong>your own derived class of your own design</strong>. Examples could be Football, Soccer, Baseball, Basketball, Hockey, etc. Your derived class must inherit from ProSportsTeam. This will cause you to implement the pure virtual methods in your derived class. You are also required to add at least one private attribute to your class – something that is found in your derived class (and maybe some other sports) but not ALL sports. An example might be some kind of unique statistic like touchdowns for football or RBIs for baseball. Optional: Add anything else you want to display in your output.

Add appropriate constructors. Adding setters and getters is optional – see if you need them or not. The printInfo() method should report on the base class attributes and the added attribute(s) in your derived class. The calcRecord() should report the team points or percentage – whatever they use for the team standings in their divisions. An example is given below for Football if you want to use that. You can call calcRecord() from printInfo() or from main() – your choice.

Your main function should demonstrate the operation of your class. Instantiate a team with its name, city and colors and add the win/loss/tie stats. Some sports don’t use ties; if your sport doesn’t use ties, pass a zero for ties to the base class constructor.

<strong>IMPORTANT</strong>: You are required to use dynamic binding (pointer to the base class) in your main function. Be sure to give a value to your added attribute(s) using the constructor or a setter. You don’t need to enter input from the user at the keyboard unless you want to. Then use printInfo() and calcRecord(); again, it is OK to call calcRecord() from printInfo() to meet this requirement.

<strong>STEP 1</strong>

Use this UML diagram for the abstract base class. DO NOT CHANGE OR OMIT ANYTHING IN THIS CLASS.

<table border="1">

 <tbody>

  <tr>

   <td><em>ProSportsTeam</em></td>

  </tr>

  <tr>

   <td>#name : string                                  //like Cubs, Bears, etc.#homeTown : string#uniformColors : string#wins : double#losses : double#ties : double</td>

  </tr>

  <tr>

   <td>&lt;setters and getters are optional&gt;+<em>calcRecord() : double                    </em>//pure virtual function reporting standings points or percentage +printInfo() : void                             //pure virtual function reporting on attributes</td>

  </tr>

 </tbody>

</table>

<strong>STEP 2</strong>

Create a class for any professional sport; no UML is given – your design! Use a sport (not a team); for example, create Football, Baseball, Soccer, Hockey, etc. — not Bears, Packers, etc.

The only requirements for your class are:

<ul>

 <li>It inherits from the abstract base class, ProSportsTeam.</li>

 <li>It has at least one added private attribute that is unique to the sport chosen.</li>

 <li>The methods calcRecord() and printInfo() are coded. PrintInfo() should display the team name, home town, uniform colors and points/percentage; you may add anything else you wish.</li>

</ul>

<strong>STEP 3</strong>

Create a main function in a separate file. Requirements for main function:

<ol>

 <li>Create an object for your derived class using a pointer to the base class, ProSportsTeam.</li>

 <li>instantiate the object with data using either a constructor or setters; use the pointer if you use setters.</li>

 <li>display the data using printInfo() and calcRecord() – use the pointer; it is OK to call calcRecord() from the printInfo() method or from the main function.</li>

</ol>

*Calculation for Football percentage: (wins plus (ties/2)) divided by (total games). Usually reported to three decimal places.