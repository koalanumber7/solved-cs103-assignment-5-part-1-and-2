Download Link: https://assignmentchef.com/product/solved-cs103-assignment-5-part-1-and-2
<br>
PART 1

<strong>Question 1:</strong> <strong> </strong>

In this question, you are required to develop a host of classes, and place them in a reasonable hierarchy, as shown below:







<strong>Description </strong>

<strong> </strong>

For the <em>Shape</em> class hierarchy, create a <em>Shape</em> class that will be the base class of all the other shapes. It should have one private string instance variable representing the shape’s color, and should have the following public member functions:







Shape()   //Default constructor

Shape(<strong>const</strong> string&amp; color) // a constructor that sets the color instance value. string getColor() <strong>const</strong> //a const member function returning the object’s color  void setColor(const string&amp; color)//a member function setting the object’s color value.

string toString() //function that returns the shape’s description (color, type,position, measurements, and area) as a string. It must be overridden in each derived class.




Create a 2DPoint class. It should have two private double instance variable representing the x and y coordinates of position and should have the following public member functions:







2 DPoint() //Default constructor

<ul>

 <li>DPoint(<strong>double</strong>, <strong>double</strong>) //Parameterized constructor</li>

</ul>

<strong>double </strong>getX()<strong> const </strong>//a const member function returning the x coordinate value<strong>  void </strong>setX(<strong>double</strong>) //a member function setting the x coordinate value<strong> double </strong>getY()<strong>const </strong>// a const member function returning the y coordinate value.

<strong>void </strong>setY(<strong>double</strong>) //a member function setting the y coordinate value.




Create a 3DPoint that is derived from 2DPoint. It should have a private double instance variable representing the z coordinate of position and should have the following public member functions:




<ul>

 <li>DPoint() //Default constructor</li>

</ul>

3DPoint(<strong>double</strong>,<strong>double, double</strong>) //Parameterized constructor that invokes the base 2 DPoint class to set x,y coordinates values then sets its z dimension.

<strong>double </strong>getZ()<strong>const </strong>// a const member function returning the Z coordinate value.

<strong>void </strong>setZ(<strong>double</strong>) //a member function setting the Z coordinate value.<strong>  </strong>




Create a 2DShape class that is derived from Shape. It should have one private 2DPoint instance variable representing the position of 2D shape, and should have the following public member functions:







2 DShape() //Default constructor

2DShape(<strong>const</strong> string&amp; color ,<strong> double </strong>x,<strong> double </strong>y) //Parameterized constructor that invokes the base Shape constructor to set color then sets its own coordinates instance value.

<strong>double </strong>area() //member function that computes and returns the object’s area. It must be overridden in each derived class.

<strong>double </strong>perimeter(); //member function that computes and returns the object’s perimeter. It must be overridden in each derived class.




Create a 3DShape class that is derived from Shape. It should have one private 3DPoint instance variable representing the position of 3D shape, with a default and parametrized constructor and member functions for volume.




Create a Circle class that is derived from 2DShape. It should have one private double instance variable representing the radius, and should have the following public member functions:




Circle(const string&amp; color,<strong> double </strong>x,<strong> double </strong>y ,<strong> double</strong> radius) //a constructor that invokes the base             2DShape constructor then sets its own radius instance value.

<strong>double </strong>area() //this overriding member function computes and returns the Circle       <strong> </strong>object’s area value.

<strong>double </strong>perimeter () //this overriding member function computes and returns the Circle    <strong> </strong>object’s perimeter value. string toString() //this overriding member function returns the Circle object’s description ( color, type, measurements, perimeter and area) like  Red Circle Position:(x,y) Radius:Value1 Perimeter:Value2 Area:Value3




Create a Square class with one private double instance variable representing the side length, with a default and parametrized constructor and overriding member functions for area(), perimeter() and toString().




Create a Traingle class with two private double instance variable representing the width, length, with a default and parametrized constructor and overriding member functions for area(), perimeter() and toString().







Create a Sphere class that is derived from 3DShape. It should have one private double instance variable representing the radius, and should have the following public member functions:







Sphere(<strong>const </strong>string&amp; color,<strong> double </strong>x,<strong> double </strong>y<strong>, double </strong>z<strong>, double</strong> radius)//a constructor that invokes the base 3DShape constructor then sets its own radius instance value.

<strong>double </strong>voulme() //this overriding member function computes and returns the Spehere object’s volume value.

<strong>string </strong>toString()//this overriding member function returned the object’s description ( color, type, measurements, volume) like

Red Sphere Position:(x,y,z) Radius:Value1 Vloume:Value3




Create a Cube class with one private double instance variable representing the side length, with a constructor and overriding member functions for volume() and toString().




Create a Tetrahedron class with one private double instance variable representing the length of edge, with a constructor and overriding member functions for volume() and toString().







Each derived class constructor must use the constructor initializer syntax to call the base Shape constructor.<sub>        </sub>

To check shape data, create a ShapeFactory.cpp file containing a getShape() function and polymorphic arrays of type 2DShape and 3DShape It should read a shape description from the input stream, create the correct type of derived shape with the new operator and parameters to the constructor. After reading a shape type (e.g. circle), it reads the additional information specific to that type of shape (e.g. for a circle, it reads the radius position and color), and then uses the new operator to create the specific derived type of shape (e.g. new Circle(radius) ) and add to the dynamic array of the specific type.<sub>   </sub>

Initially the size of each Array will be 1 and it will point to NULL. After creating a new circle add it to 2DShape Array by increasing the capacity of the circle Array by 1. The last index will always point to Null indicating to the end of the Array.




<strong>Question 2:</strong> <strong> </strong>

In this question, you need to write a host of classes, and place them in a reasonable hierarchy as shown below:<sub>       </sub>




<strong>Description</strong>:




Design a class ALU which include the following attributes:

<ul>

 <li>NoOfAdders: a int</li>

 <li>NoOfSubtractor: a int</li>

 <li>NoOfRegisters: a int</li>

 <li>sizeOfRegisters: a int</li>

</ul>




The class has the following member functions.

<ol>

 <li>A constructor initializing the number with default parameters.</li>

 <li>A constructor initializing the number with Overloaded Constructors.</li>

 <li>Getters and Setters of the class data members.</li>

</ol>




Design a class C ontrolUnit which includes the following:

<ul>

 <li>clock: a float</li>

</ul>




The class has the following me mber functions.

<ol>

 <li>A constructor initializing the number with default parameters.</li>

 <li>A constructor initializing the number with Overloaded Constructors.</li>

 <li>Getters and Setters of the class data member as given below.</li>

</ol>







Design a class CPU which is composed of ALU a nd CU. Data member are:

<ul>

 <li>alu: a ALU</li>

 <li>cu: a ControlUnit</li>

</ul>




The class has the following member functions.<sub>         </sub>

<ol>

 <li>A constructor initializing the number with default parameters.</li>

 <li>A constructor initializing the number with Overloaded Constructors.</li>

 <li>Getters and Setters of the class data members.</li>

</ol>










Design a class MainMemory which includes the following:        <sub> </sub> capacity: an int

<ul>

 <li>technologyType: a string (Possible values :Semiconductor, Silicon)</li>

</ul>

The class has the following member functions.<sub>         </sub>

<ol>

 <li>A constructor initializing the number with default parameters.</li>

 <li>A constructor initializing the number with Overloaded Constructors.</li>

 <li>Getters and Setters of the class data member.</li>

</ol>




Design a class Port which includes the following:

<ul>

 <li>type: a string (Possible values : VGI Port,I/O Port,USB Port,HDMI Port etc)  baud_rate: an int</li>

</ul>




The class has the following member functions.<sub>         </sub>

<ol>

 <li>A constructor initializing the number with default parameters.</li>

 <li>A constructor initializing the number with Overloaded Constructors.</li>

 <li>Getters and Setters of the class data member.</li>

</ol>




Design a class MotherBoard which is composed of Ports (IO ports, VGI ports etc) and aggregated with            MainMemory:

<ul>

 <li>mm: A MainMemory</li>

 <li>ports: ports array</li>

</ul>




The class has the following member functions.

<ol>

 <li>A constructor initializing the number with default parameters.</li>

 <li>A constructor initializing the number with Overloaded Constructors.</li>

 <li>Getters and Setters of the class data members.</li>

</ol>







Design a class PhysicalMemeory which includes the following:

<ul>

 <li>capacity: an int</li>

</ul>




The class has the following member functio ns.

<ol>

 <li>A constructor initializing the number with default parameters.</li>

 <li>A constructor initializing the number with Overloaded Constructors.</li>

 <li>Getters and Setters of the class data member.</li>

</ol>




Design a class Computer which is aggregated of PhysicalMemory, CPU and MotherBoard includes the following:

<ul>

 <li>pm: A PhysicalMemory <sub> </sub> mb: A MotherBoard</li>

 <li>cpu: A CPU</li>

</ul>




The class has the following member functions.<sub>         </sub>

<ol>

 <li>A constructor initializing the number with default parameters.</li>

 <li>A constructor initializing the number with Overloaded Constructors.</li>

 <li>Getters and Setters of the class data member.</li>

</ol>




To check the scenario, create a Shop class which manufacture and sell the Computers. In Shop class write a function manufactureComputer() which create a new Computer Object by taking all necessary specifications from user and add it to a Dynamic Array of Computers. After Successful Computer Object Creation add it to the List by adjusting the capacity of Array. The User can view List of Computers created.










<strong>Question 3: </strong>




In this Question you will design an automated management system for a Walk-through Restaurant where customers can place their orders and pay the bill to receive ordered items. Read the case study carefully and identify all the classes necessary to develop the system and put them in a reasonabl<sub>            </sub>e hierarchy.

The system enable the user to view the orders placed by Customers. For each order the system stores customer information, Date and Time at which the order was placed, Total bill and status ( pending, in-progress, Ready).For each Order 5% Tax is included in the grand total.

Customers can put orders by selecting items from the list of available items, for this, the restaurant must use customer’s name and phone number. User can Place Order and make Payment in the system. The restaurant menu is organized in categories (Main course, Beverages, and Desserts) of menu items. Each menu item has an id, name, and price in Rs.<sub>       </sub>

The Main Course Menu includes Sandwiches, Pizzas and a further sub<sub>         </sub>-category of Fried Items. For each main course item customer can provide a description (Special Instructions) .Sandwich can be specified by its filling (Smoked Chicken, BBQ Chicken, Chicken Jalapeno, Vegetable) and type (Grilled/Plain).The restaurant offers Pizza in four different sizes (small, medium, large, extra-large) with three different crust options (Fresh pan, Stuffed and Hand-tossed) and many topping options (Pepperoni, Mushrooms, Onions, Extra cheese and Black olives).<sub>              </sub>

The Fried items sub-category include Nuggets, Fries and Burgers. Each Fried Item is available with many sauce options to choose from. The restaurant offers three different types of nuggets (Chicken Nuggets, Tempura Nuggets and Crispy Chicken Nuggets) in three different shapes (circle, star and heart) with dipping Sauces (Sweet and Sour, Honey Mustard, Sweet Chili and

Hot Mustard) .Two types of fries are available: curly and plain in three different servings (Small, Regular, Jumbo) with different sauces (Garlic-Mayo, Chocolate and Cheddar Cheese). To order a Burger a customer can select from different options available for Patties (Beef, Crispy Chicken, Grilled Chicken and fish) and Bun Type (plain and sesame seed).The Burger Sauces (Jalapeno cheese sauce, Classic burger sauce, cheese mayo and Truffle mayo).<sub>            </sub>

The restaurant offers Beverages of different flavors in three different servings (Small, Regular, Large) and in two different temperature levels ( i.e. Room temperature, Chill).Beverages category is further divided in two sub categories (Carbonated Drinks, Fresh Juices).

Carbonated Drinks (Sprite, 7up, Pepsi, Coke, Red Bull and Fanta) can be specified by name and whether or not the drink is sugar free. Fresh Juices have two types (Fresh/Pre Packed) and can further be specified whether or not <sub>               </sub>it’s seasonal.

Dessert menu contains a variety of flavors of Ice Creams and Cookies. The System stores Price per scoop for all available ice creams. Ice Cream Price is calculated with Numbers of scoops and Customer can choose from two types to toppings (Wafers and Peanuts).Cookies are available in Different Flavors (Chocolate chip, Peanut, Coconut). The System Store price per gram for each Cookie type. The price of the Cookies is calculated by price per gram and is also available as Sugar free. Cookies are Available in Different shapes (Round, Square).

The System take user order by Displaying the Menu to User. Each order can be composed of multiple items and the system generate and display the total bill to the user. User can then proceed with the order or cancel the order. If user choose to proceed with the order the system display the Bill. User can then pick the order from the restaurant by paying bill. System should be able to display all the cancelled Orders and Ready Orders.




<strong>Note: </strong>Create a polymorphic array of Items inside the Order Class and dynamically increase the capacity of the array as you have done in first question inside shape Factory Class.<sub>   </sub>

Payment is handled manually outside the system. System will only Display the grand Total to the Customer. When the User Successfully complete an order the system change the status to ready immediately and Displays a Success Message to customer.

PART 2

<h1>Question 1: Clash of the Titans</h1>

<em>In this exercise, you are going to have dragons and hydras fight each other. </em>




Hydra                                                                            Dragon




The provided main program simulates a Fight between a dragon and a hydra. The hierarchies of classes that model the creatures of this game are missing and you are asked to provide them.




<strong><em><u>The class Creature</u></em></strong><strong><u>:</u></strong>

A creature is characterized by;

<ul>

 <li>its <strong>name</strong> (a constant string);</li>

 <li>its <strong>level</strong> (an integer);</li>

 <li>its number of health <strong>points</strong> (health status; an integer);</li>

 <li>its <strong>force</strong> (an integer);</li>

 <li>its <strong>position</strong> (position , also an integer; for simplicity, our game takes place in 1D; Can be 2D as well an object of Point class).</li>

 <li>a <strong>constructor</strong> allowing the initialization of the name, level, health points, force and position of the creature using the values passed as parameters, in this order; the constructor accepts <strong>zero</strong> as <strong>default</strong> <strong>value</strong> for the position;</li>

 <li>a method <strong>bool alive( )</strong> returning true if the creature is alive (number of health points greater than zero) or false otherwise;</li>

 <li>a method <strong>int AttackPoints</strong> returning the number of attack points that can be incited by the creature to others; the value is computed as the level multiplied by the force if the creature is alive, or zero otherwise;</li>

 <li>a method <strong>void Move(int),</strong> which does not return anything and adds the integer passed as parameter to the position of the creature;</li>

 <li>a method <strong>void GoodBye( )</strong> which does not return anything and displays the message <strong>( &lt;name&gt; is no more!)</strong>: using strictly this format. Here <strong>&lt;name&gt;</strong> is the name of the creature;</li>

 <li>a method <strong>void Weak</strong> <strong>(int x)</strong>, which does not return anything and subtracts the number of points passed as parameter from the number of health points of the creature, if it is alive; and if the creature dies, its number of health points is set to zero and the method <strong>GoodBye</strong> is called;</li>

 <li>a method <strong>void Display( )</strong>, which does not return anything and displays information about the creature, using strictly the following format:</li>

</ul>

<strong>&lt;name&gt;, level: &lt;level&gt;, health_status: &lt;points&gt;, force: &lt;force&gt;,    Attacking Points: &lt;attack&gt;, position: &lt;position&gt; </strong>

<strong>&lt;name&gt;</strong> is the name of the creature, <strong>&lt;level&gt;</strong> is its level,<strong> &lt;points&gt;</strong> is its number of health points, <strong>&lt;force&gt; </strong>is its force,<strong> &lt;attack&gt; </strong>is its number of attack points and <strong>&lt;position&gt; </strong>is its position.

<strong><em><u>The class Dragon:</u>              </em></strong>

A Dragon is a Creature. It has a specific characteristic the range of its flame (<strong>flamerange</strong> an integer). Its specific methods are:

<ul>

 <li>a <strong>constructor</strong> which initializes its name, level, number of health points, the force, the range of the flame and the position of the dragon using the values passed as parameters, in this order; the constructor accepts <strong>zero</strong> as <strong>default</strong> <strong>value</strong> for the position</li>

 <li>a method <strong>void Fly(int pos)</strong> which does not return anything and allows the dragon to move to the given position.</li>

 <li>a method <strong>void BlowFlame(Creature&amp; )</strong> which does not return anything and simulates what happens when the dragon blows its flame towards another Creature:

  <ol>

   <li>if the dragon and the creature are both alive and if the creature is in range of its flame, the dragon inflicts its attack points as damage to the creature; the creature weakens by the number of attack points; The dragon also weakens; it loses of ‘ health points, with of ‘ being the distance between the dragon and the creature (the further the dragon has to blow, the more it weakens, <em>the function to calculate the distance will be provided to you);</em></li>

   <li>if after this epic fight the dragon is still alive and the creature dies, the dragon increases in level by one unit;</li>

  </ol></li>

 <li>The creature is in the range of the flame of the dragon if the distance between them is smaller or equal to the range of the flame (<em>you should use the function distance we provide</em>).</li>

</ul>




<strong><em><u>The class Hydra:</u></em></strong>

A Hydra is a Creature. It has special characteristics the length of its neck (<strong>neckLength,</strong> an integer) and the dose of poison it can inject in an attack (<strong>poisonDose,</strong> an integer).

Its special methods are:

<ul>

 <li>a <strong>constructor</strong> which initializes its name, level, number of health points, force, the length of its neck, the poison dose and the position using the values passed as parameters, in this order; the constructor accepts <strong>zero</strong> as <strong>default</strong> <strong>value</strong> for the position;</li>

 <li>a method <strong>void InjectPoison(Creature&amp; )</strong> which does not return anything and simulates what happens when the hydra poisons another Creature:

  <ol>

   <li>if the hydra and the creature are alive and the creature is in range of the head of the hydra, then the hydra inflicts damage to the creature; the creature weakens by the number of attack points of the hydra plus its dose of poison;</li>

   <li>if at the end of the fight the creature is no longer alive, the hydra increases in level by one unit; <em>* The creature is in range of the head of the hydra” if the distance the creature and the hydra is smaller or equal to the length of the neck of the hydra. </em></li>

  </ol></li>

</ul>

The function <strong>void Fight (fight)</strong> takes as parameters a dragon and a hydra. It allows:              The hydra to poison the dragon

<ul>

 <li>The dragon to blow on the hydra.</li>

</ul>

Execution examples

The example of output below corresponds to the provided program.

<table width="623">

 <tbody>

  <tr>

   <td width="623"><strong>Dragon red</strong>, level: 2, health_status: 10, force: 3, points of attack: 6, position: 0 is preparing for fight with:<strong>Hydra evil</strong>, level: 2, health_status: 10, force: 1, points of attack: 2, position: 42 <strong>1st Fight:</strong>The creatures are not within range, so cannot Attack.<strong>After the Fight: </strong><strong>Dragon red</strong>, level: 2, health_status: 10, force: 3, points of attack: 6, position: 0 <strong>Hydra evil</strong>, level: 2, health_status: 10, force: 1, points of attack: 2, position: 42 Dragon has flown close to Hydra:<strong>Dragon red</strong>, level: 2, health_status: 10, force: 3, points of attack: 6, position: 41 <strong>Hydra</strong> moves :<strong>Hydra evil</strong>, level: 2, health_status: 10, force: 1, points of attack: 2, position: 43 <strong>2nd Fight : </strong>+ <strong>Hydra</strong> inflicts a 3-point attack on dragon[ level (2) * force (1) + poison (1) = 3 ] ;+ <strong>Dragon</strong> inflicts a 6-point attack on Hydra</td>

  </tr>

  <tr>

   <td width="623">[ level (2) * force (3) = 6 ] ;+ during his attack, dragon loses two additional points[Corresponding to the distance between dragon and hydra: 43 – 41 = 2].<strong>After the Fight: </strong><strong>Dragon red</strong>, level: 2, health_status: 5, force: 3, points of attack: 6, position: 41<strong>Hydra evil</strong>, level: 2, health_status: 4, force: 1, points of attack: 2, position: 43 </td>

  </tr>

 </tbody>

</table>




<strong><em> </em></strong>