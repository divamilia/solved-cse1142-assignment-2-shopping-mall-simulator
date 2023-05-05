Download Link: https://assignmentchef.com/product/solved-cse1142-assignment-2-shopping-mall-simulator
<br>
In this homework, you will implement a shopping mall simulator program with an object-oriented approach. The class hierarchy of the program will be as following:

<ol>

 <li>Implement a Vegan interface with the following UML diagram.</li>

</ol>

<table width="312">

 <tbody>

  <tr>

   <td width="26"> </td>

   <td width="286">&lt;&lt;interface&gt;&gt; <em>Vegan </em></td>

  </tr>

  <tr>

   <td width="26"> </td>

   <td width="286"> </td>

  </tr>

  <tr>

   <td width="26">+</td>

   <td width="286"><em>madeOf():void </em></td>

  </tr>

 </tbody>

</table>




<ul>

 <li>The Vegan interface represents the property of not having any animal product.</li>

 <li>The madeOf abstract method will be implemented in the classes that implements <em>Vegan</em> interface to show what the item is made of.</li>

</ul>

<ol start="2">

 <li>Implement a Washable interface with the following UML diagram.</li>

</ol>

<table width="312">

 <tbody>

  <tr>

   <td width="26"> </td>

   <td width="286">&lt;&lt;interface&gt;&gt; <em>Washable </em></td>

  </tr>

  <tr>

   <td width="26"> </td>

   <td width="286"> </td>

  </tr>

  <tr>

   <td width="26">+</td>

   <td width="286"><em>howToWash():void </em></td>

  </tr>

 </tbody>

</table>




<ul>

 <li>The Washable interface represents the property of being washable.</li>

 <li>The howToWash abstract method will be implemented in the classes that implements Washable interface to show the instructions on how to wash an item.</li>

</ul>

<ol start="3">

 <li>Implement an Item abstract class with the following UML diagram.</li>

</ol>

<table width="245">

 <tbody>

  <tr>

   <td width="26"> </td>

   <td width="219"><em>Item </em></td>

  </tr>

  <tr>

   <td width="26">––</td>

   <td width="219">vat:double basePrice:double</td>

  </tr>

  <tr>

   <td width="26">+++++</td>

   <td width="219">getVat():double setVat(vat:double):void getBasePrice():double setBasePrice(price:double):void <em>calculatePrice():double </em></td>

  </tr>

 </tbody>

</table>

<ul>

 <li>The Item class represents anything that is being sold at the shopping mall.</li>

 <li>The data field vat represents value added tax for each item.</li>

 <li>The data field basePrice represents the price of the item when there is no taxes or profit added.</li>

 <li>getVat and setVat methods are accessor methods for vat data field.</li>

 <li>getBasePrice and setBasePrice methods are accessor methods for basePricedata</li>

 <li>calculatePriceabstract method will be implemented in subclasses to calculate the final price of the item.</li>

</ul>

<ol start="4">

 <li>Implement a Clothing abstract class with the following UML diagram.</li>

</ol>




<table width="244">

 <tbody>

  <tr>

   <td width="26"> </td>

   <td width="217"><em>Clothing </em></td>

  </tr>

  <tr>

   <td width="26"> </td>

   <td width="217"> </td>

  </tr>

  <tr>

   <td width="26">+</td>

   <td width="217">Clothing();</td>

  </tr>

 </tbody>

</table>







<ul>

 <li>The Clothing class represents any piece of clothing.</li>

 <li>You have to implement the constructor to set vat data field to 0.18.</li>

 <li>Clothing class should extend Item class and implement Washable interface.</li>

</ul>

<ol start="5">

 <li>Implement a Food abstract class with the following UML diagram.</li>

</ol>

<table width="244">

 <tbody>

  <tr>

   <td width="26"> </td>

   <td width="81"> </td>

   <td width="136"><em>Food </em></td>

  </tr>

  <tr>

   <td width="26"> </td>

   <td width="81"> </td>

   <td width="136"> </td>

  </tr>

  <tr>

   <td width="26">+</td>

   <td width="81">Food();</td>

   <td width="136"> </td>

  </tr>

 </tbody>

</table>




<ul>

 <li>The Food class represents any kind of food.</li>

 <li>You have to implement the constructor to set vatdata field to 0.08.</li>

 <li>Food class should extend Item class</li>

</ul>

<ol start="6">

 <li>Implement a Dairy class with the following UML diagram.</li>

</ol>

<table width="498">

 <tbody>

  <tr>

   <td width="26"> </td>

   <td width="472">Dairy</td>

  </tr>

  <tr>

   <td width="26"> </td>

   <td width="472"> </td>

  </tr>

  <tr>

   <td width="26">++</td>

   <td width="472">Dairy()Dairy(basePrice:double)</td>

  </tr>

 </tbody>

</table>




<ul>

 <li>A Dairy object represents a dairy product.</li>

 <li>It extends Food</li>

 <li>The no-arg constructor calls other constructor with the value 8.0.</li>

 <li>Argumented construtor sets basePrice to the given value.</li>

 <li>This class has to implement calculatePrice method as well. The method has to return the retail price of the dairy product. You have to calculate retail price by adding 30% profit to the taxed price</li>

</ul>

<ol start="7">

 <li>Implement a Fruit class with the following UML diagram.</li>

</ol>




<table width="498">

 <tbody>

  <tr>

   <td width="26"> </td>

   <td width="472">Fruit</td>

  </tr>

  <tr>

   <td width="26"> </td>

   <td width="472"> </td>

  </tr>

  <tr>

   <td width="26">++</td>

   <td width="472">Fruit()Fruit(basePrice:double)</td>

  </tr>

 </tbody>

</table>




<ul>

 <li>A Fruit object represents a real-life fruit</li>

 <li>It extends Food class and implements Vegan and Washable</li>

 <li>The no-arg constructor calls other constructor with the value 6.0.</li>

 <li>Argumented construtor sets basePrice to the given value.</li>

</ul>

This class has to implement calculatePrice method as well. The method has to return the retail price of the fruit. You have to calculate retail price by adding 20% profit to the taxed price.

<ul>

 <li>This class has to implement howToWash method as well. The method has to print “Wash Fruit with cold water.” on the screen.</li>

 <li>This class has to implement madeOf method as well. The method has to print “It is made only of fruits.” on the screen.</li>

</ul>

<ol start="8">

 <li>Implement a Top class with the following UML diagram.</li>

</ol>

<table width="498">

 <tbody>

  <tr>

   <td width="26"> </td>

   <td width="195"> </td>

   <td width="276">Top</td>

  </tr>

  <tr>

   <td width="26"> </td>

   <td width="195"> </td>

   <td width="276"> </td>

  </tr>

  <tr>

   <td width="26">++</td>

   <td width="195">Top()Top(basePrice:double)</td>

   <td width="276"> </td>

  </tr>

 </tbody>

</table>




<ul>

 <li>A Top object represents a real-life top clothing.</li>

 <li>It extends Clothing</li>

 <li>The no-arg constructor calls other constructor with the value 20.0.</li>

 <li>Argumented construtor sets basePrice to the given value.</li>

 <li>This class has to implement calculatePrice method as well. The method has to return the retail price of the top product. You have to calculate retail price by adding 20% profit to the taxed price.</li>

 <li>This class has to implement howToWash method as well. The method has to print “Wash Top at 40 degrees.” on the screen.</li>

</ul>







<ol start="9">

 <li>Implement a Trousers class with the following UML diagram.</li>

</ol>




<table width="498">

 <tbody>

  <tr>

   <td width="26"> </td>

   <td width="472">Trousers</td>

  </tr>

  <tr>

   <td width="26"> </td>

   <td width="472"> </td>

  </tr>

  <tr>

   <td width="26">++</td>

   <td width="472">Trousers()Trousers(basePrice:double)</td>

  </tr>

 </tbody>

</table>




<ul>

 <li>A Top object represents a real-life trousers.</li>

 <li>It extends Clothing</li>

 <li>The no-arg constructor calls other constructor with the value 4 0.</li>

 <li>Argumented construtor sets basePrice to the given value.</li>

</ul>

This class has to implement calculatePrice method as well. The method has to return the retail price of the trousers. You have to calculate retail price by adding 20% profit to the taxed price.

<ul>

 <li>This class has to implement howToWash method as well. The method has to print “Wash Trousers at 30 degrees.” on the screen.</li>

</ul>







<ol start="10">

 <li>Implement an Underware class with the following UML diagram.</li>

</ol>




<table width="498">

 <tbody>

  <tr>

   <td width="26"> </td>

   <td width="472">Underware</td>

  </tr>

  <tr>

   <td width="26"> </td>

   <td width="472"> </td>

  </tr>

  <tr>

   <td width="26">++</td>

   <td width="472">Underware()Underware(basePrice:double)</td>

  </tr>

 </tbody>

</table>




<ul>

 <li>A Top object represents a real-life underware.</li>

 <li>It extends Clothing</li>

 <li>The no-arg constructor calls other constructor with the value 30.0.</li>

 <li>Argumented construtor sets basePrice to the given value.</li>

 <li>This class has to implement calculatePrice method as well. The method has to return the retail price of the underware. You have to calculate retail price by adding 45% profit to the taxed price.</li>

 <li>This class has to implement howToWash method as well. The method has to print “Wash Underware at 60 degrees.” on the screen.</li>

</ul>







<ol start="11">

 <li>Implement a Fruit class with the following UML diagram.</li>

</ol>




<table width="498">

 <tbody>

  <tr>

   <td width="26"> </td>

   <td width="472">Vegetable</td>

  </tr>

  <tr>

   <td width="26"> </td>

   <td width="472"> </td>

  </tr>

  <tr>

   <td width="26">++</td>

   <td width="472">Vegetable()Vegetable(basePrice:double)</td>

  </tr>

 </tbody>

</table>




<ul>

 <li>A Vegetable object represents a real-life fruit</li>

 <li>It extends Food class and implements Vegan and Washable</li>

 <li>The no-arg constructor calls other constructor with the value 10.0.</li>

 <li>Argumented construtor sets basePrice to the given value.</li>

 <li>This class has to implement calculatePrice method as well. The method has to return the retail price of the vegetable. You have to calculate retail price by adding 25% profit to the taxed price.</li>

 <li>This class has to implement howToWash method as well. The method has to print “Wash Vegetable with warm water.” on the screen.</li>

</ul>

This class has to implement madeOf method as well. The method has to print “It is made only of vegetables.” on the screen.







<ol start="12">

 <li>Implement a ShoppingMall class with the following UML diagram.</li>

</ol>




<table width="498">

 <tbody>

  <tr>

   <td width="26"> </td>

   <td width="472">ShoppingMall</td>

  </tr>

  <tr>

   <td width="26">–</td>

   <td width="472"><u>items:ArrayList&lt;Item&gt;</u></td>

  </tr>

  <tr>

   <td width="26">+++++++++</td>

   <td width="472">getItems():ArrayList&lt;Item&gt; addDairy():void addFruit():void addTop():void addTrousers():void addUnderware():void addVegetable():void addArbitrary(item:Item):void bill():double</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>A ShoppingMall object represents a shopping malls.</li>

 <li>The data field items keeps all the items in the shopping mall.</li>

 <li>getItems method is getter for items ArrayList.</li>

 <li>addDairy method adds a default Dairy object to items ArrayList.</li>

 <li>addFruit method adds a default Fruit object to items ArrayList.</li>

 <li>addTop method adds a default Top object to items ArrayList.</li>

 <li>addTrousers method adds a default Trousers object to items ArrayList.</li>

 <li>addUnderware method adds a default Underware object to items ArrayList.</li>

 <li>addVegetable method adds a default Vegetable object to items ArrayList.</li>

 <li>addArbitrary method adds the given Item object to items ArrayList.</li>

 <li>bill method iterates through the items ArrayList and calculates the total price of items in the ArrayList.</li>

</ul>




<ol start="13">

 <li>Write a test program in which the following are performed in order.

  <ol>

   <li>Create a new ShoppingMall object.</li>

   <li>Add a default Dairy, a default Fruit, a default Top, a default Trousers, a default Underware, a default Vegetable object to the ShoppingMall object.</li>

   <li>Add a Top object with basePrice = 100</li>

   <li>Create a printContent method that invokes madeOf method of the all the Vegan instances inside the ShoppingMall’s ArrayList<strong>. </strong></li>

   <li>Create a printWashingInstructions method that invokes howToWash method of the all the Washable instances inside the ShoppingMall’s ArayList</li>

  </ol></li>

</ol>




<ol>

 <li>Call these two methods inside main method.</li>

 <li>Print the bill of the ShoppingMall object.</li>

</ol>

<strong>  </strong>

<strong>This is a simple scenario to test your class implementations. There might be other test cases too. Therefore, please pay attention to use the same class, method and variable names in your implementations. You are allowed to increase the number of methods in the classes; however, you cannot decrease the number of them. </strong><em> </em>

<strong> </strong>