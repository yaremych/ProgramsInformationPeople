..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".


Extra Exercises
===============

1. Create a class called House that has three instance variables: color, rooms, and price. To the variable name ``houseOne``, assign an instance of House whose color is white, has 3 rooms, and costs 50000. To the variable name ``houseTwo``, assign an instance of House whose color is red, has 9 rooms, and costs 1000000. 

.. activecode:: ee_ch13_01
   :tags: Classes/ImprovingourConstructor.rst


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(houseOne.color, "white", "Testing that houseOne has the correct color assigned.")
         self.assertEqual(houseOne.rooms, 3, "Testing that houseOne was assigned the correct number of rooms.")
         self.assertEqual(houseOne.price, 50000, "Testing that houseOne was assigned the correct price.")

      def testTwo(self):
         self.assertEqual(houseTwo.color, "red", "Testing that houseTwo has the correct color assigned.")
         self.assertEqual(houseTwo.rooms, 9, "Testing that houseTwo was assigned the correct number of rooms.")
         self.assertEqual(houseTwo.price, 1000000, "Testing that houseTwo was assigned the correct price.")

   myTests().main()




2. Create a class called Animal that has two instance variables: arms and legs. Create a class method called limbs that, when called, returns the total number of limbs the animal has. To the variable name ``spider``, assign an instance of Animal that has 4 arms and 4 legs. Call the limbs method on ``spider`` and save the result to the variable name ``spidlimbs``. 

.. activecode:: ee_ch13_02
   :tags: Classes/ImprovingourConstructor.rst, Classes/AddingOtherMethodstoourClass.rs


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(spider.arms, 4, "Testing that spider was assigned the correct number of arms.")
         self.assertEqual(spider.legs, 4, "Testing that spider was assigned the correct number of legs.")
         self.assertEqual(spidlimbs, 8, "Testing that spidlimbs was assigned correctly.")

   myTests().main()    




3. Create a class called Cereal that has three instance variables: name, brand, and fiber. When an instance of Cereal is printed, the user should see the following: "[name] cereal is produced by [brand] and has [fiber] grams of fiber in every serving!" To the variable name ``c1``, assign an instance of Cereal whose name is Corn Flakes, brand is Kellogg's, and fiber is 2. To the variable name ``c2``, assign an instance of Cereal whose name is Honey Nut Cheerios, brand is General Mills, and fiber is 3. Practice printing both! 

.. activecode:: ee_ch13_03
   :tags: Classes/ImprovingourConstructor.rst, Classes/AddingOtherMethodstoourClass.rst, Classes/ConvertinganObjecttoaString.rst


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(c1.__str__(), "Corn Flakes cereal is produced by Kellogg's and has 2 grams of fiber in every serving!", "Testing that c1 prints correctly.")
      def testTwo(self): 
         self.assertEqual(c2.__str__(), "Honey Nut Cheerios cereal is produced by General Mills and has 3 grams of fiber in every serving!", "Testing that c2 prints correctly.")

   myTests().main()  


4. Create a class called Cereal that has three instance variables: name, brand, and fiber. When an instance of Cereal is printed, the user should see the following: "[name] cereal is produced by [brand] and has [fiber] grams of fiber in every serving!" Create an instance method called add_fiber that increases an instance's fiber count by 1 when it is called. To the variable name ``c1``, assign an instance of Cereal whose name is Corn Flakes, brand is Kellogg's, and fiber is 2. Call the add_fiber method until c1 has a fiber count of 5. 

.. activecode:: ee_ch13_04
   :tags: Classes/ImprovingourConstructor.rst, Classes/AddingOtherMethodstoourClass.rst, Classes/ConvertinganObjecttoaString.rst



   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(c1.__str__(), "Corn Flakes cereal is produced by Kellogg's and has 5 grams of fiber in every serving!", "Testing that c1 prints correctly and has the correct fiber count.")

   myTests().main()   


5. **Challenge:** Below, we have provided a list of tuples. Use these to create a list of instances of the House class. Each instance should have three instance variables: color, rooms, and price. When an instance is printed, the user should see: "This is a [color] house with [rooms] rooms that costs [price] dollars." Save the list of instances as the variable ``houses``. Then, sort the list based on price, highest to lowest, and save this list as ``houses_by_price``. Finally, sort the list based on number of rooms, highest to lowest, and save this last as ``houses_by_rooms``. 

.. activecode:: ee_ch13_05
   :tags: Classes/sorting_instances.rst, Classes/InstancesasReturnValues.rst

   tups = [("blue", 2, 30000), ("white", 5, 10000), ("yellow", 8, 100000), ("green", 1, 8000), ("brown", 3, 400000), ("taupe", 4, 200000), ("orange", 6, 250000)]


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui): 

      def testA(self): 
         self.assertEqual(len(houses), 7, "Testing that houses has the correct number of instances in it.")

      def testB(self): 
         self.assertEqual(houses_by_price[0].price, 400000, "Testing that houses_by_price was created correctly.")
         self.assertEqual(houses_by_price[1].price, 250000, "Testing that houses_by_price was created correctly.")
         self.assertEqual(houses_by_price[-1].price, 8000, "Testing that houses_by_price was created correctly.")

      def testC(self): 
         self.assertEqual(houses_by_rooms[0].rooms, 8, "Testing that houses_by_rooms was created correctly.")
         self.assertEqual(houses_by_rooms[1].rooms, 6, "Testing that houses_by_rooms was created correctly.")
         self.assertEqual(houses_by_rooms[-1].rooms, 1, "Testing that houses_by_rooms was created correctly.")

   myTests().main()






