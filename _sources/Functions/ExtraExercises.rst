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

1. Write a function named ``same`` that takes a string as input, and simply returns that string. 

.. activecode:: ee_functions_01
   :tags: Functions/Returningavaluefromafunction.rst, Functions/FunctionDefinitions.rst

   


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(same('hello'), 'hello', "Testing the same function on input 'hello'.")

   myTests().main()



2. Write a function called ``subtract_three`` that takes an integer or any number as input, and returns that number minus three. 

.. activecode:: ee_functions_02
   :tags: Functions/Returningavaluefromafunction.rst

   
   ===== 

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(subtract_three(9), 6, "Testing the subtract_three function on input 9.")
         self.assertEqual(subtract_three(-5), -8, "Testing the subtract_three function on input -5.")

   myTests().main()



3. Write a function named ``intro`` that takes a string as input. Given the string "Becky" as input, the function should return: "Hello, my name is Becky and I love SI 106."

.. activecode:: ee_functions_03
   :tags: Functions/Returningavaluefromafunction.rst


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(intro("Mike"), "Hello, my name is Mike and I love SI 106.", "Testing the intro function on input 'Mike'.")

   myTests().main()



4. Write a function named ``total`` that takes a list of integers as input, and returns the total value of all those integers added together. 

.. activecode:: ee_functions_04
   :tags: Functions/Returningavaluefromafunction.rst, Functions/Afunctionthataccumulates.rst



   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(total([1, 2, 3, 4, 5]), 15, "Testing the total function on input [1, 2, 3, 4, 5].")
         self.assertEqual(total([0, 0, 0, 0]), 0, "Testing the total function on input [0, 0, 0, 0].")
         self.assertEqual(total([]), 0, "Testing the total function on input [].")
         self.assertEqual(total([2]), 2, "Testing the total function on input [2].")

   myTests().main()  




5. Write a function named ``num_test`` that takes a number as input. If the number is greater than 10, the function should return "Greater than 10." If the number is less than 10, the function should return "Less than 10." If the number is equal to 10, the function should return "Equal to 10."

.. activecode:: ee_functions_05 
   :tags: Functions/Returningavaluefromafunction.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(num_test(5), "Less than 10.", "Testing the num_test function on input 5.")
         self.assertEqual(num_test(0), "Less than 10.", "Testing the num_test function on input 0.")
         self.assertEqual(num_test(12.99), "Greater than 10.", "Testing the num_test function on input 12.99.")
         self.assertEqual(num_test(10.00), "Equal to 10.", "Testing the num_test function on input 10.00.")

   myTests().main() 


6. This problem will require you to write two functions. The first function, named ``func1``, should take a number as input, and return that number multiplied by 3. The second function, named ``func2``, should take a number as input, multiply it by 3, and then add 10. You should call on ``func1`` within ``func2`` to accomplish this.

.. activecode:: ee_functions_06
   :tags: Functions/Returningavaluefromafunction.rst, Functions/Functionscancallotherfunctions.rst

   def func1():


   def func2():

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(func1(10), 30, "Testing func1 on input 10.")
         self.assertEqual(func1(0), 0, "Testing func1 on input 0.")
         self.assertEqual(func2(-2), 4, "Testing func2 on input -2.")
         self.assertEqual(func2(0), 10, "Testing func2 on input 0.")

   myTests().main() 


7. Write a function named ``add_all`` that takes two parameters. The first parameter should be a list of numbers, and the second should be an integer. The function should return a new list whose elements are all the numbers from the old list with the integer added to them (i.e.: Given the inputs [1, 2, 3], 1, the function should return [2, 3, 4]).

.. activecode:: ee_functions_07
   :tags: Functions/Returningavaluefromafunction.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(add_all([1, 2, 3], 0), [1, 2, 3], "Testing add_all on inputs [1, 2, 3], 0.")
         self.assertEqual(add_all([], 10), [], "Testing add_all on inputs [], 10.")
         self.assertEqual(add_all([5], 7), [12], "Testing add_all on inputs [5], 7.")

   myTests().main() 











