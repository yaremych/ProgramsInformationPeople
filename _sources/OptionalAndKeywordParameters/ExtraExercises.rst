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

1. Define a function called ``multiply``. It should have one required parameter, a string. It should also have one optional parameter, an integer, named ``mult_int``, with a default value of 10. The function should return the string multiplied by the integer. (i.e.: Given inputs "Hello", mult_int=3, the function should return "HelloHelloHello")

.. activecode:: ee_optparams_01
   :tags: OptionalAndKeywordParameters/OptionalParameters.rst

   def multiply():

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(multiply("Hello", mult_int = 3), "HelloHelloHello", "Testing the function multiply on inputs 'Hello', 3.")
         self.assertEqual(multiply("Goodbye"), "GoodbyeGoodbyeGoodbyeGoodbyeGoodbyeGoodbyeGoodbyeGoodbyeGoodbyeGoodbye", "Testing the function mulitply on input 'Goodbye'.")

   myTests().main()



2. Below is a function, ``sum``, that does not work. Change the function definition so the code works. The function should still have a required parameter, intx, and an optional parameter, intz with a defualt value of 5. 

.. activecode:: ee_optparams_02
   :tags: OptionalAndKeywordParameters/OptionalParameters.rst

   def sum(intz=5, intx):
       return intz + intx

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sum(8, intz = 2), 10, "Testing the function sum on inputs 8, 2.")
         self.assertEqual(sum(12), 17, "Testing the function sum on input 12.")

   myTests().main()


3. Define a function called ``nums`` that has three parameters. The first parameter, an integer, should be required. A second parameter named ``mult_int`` should be optional with a default value of 5. The final parameter, ``switch``, should also be optional with a default value of False. The function should multiply the two integers together, and if switch is True, should change the sign of the product before returning it. 

.. activecode:: ee_optparams_03
   :tags: OptionalAndKeywordParameters/KeywordParameters.rst

   def nums():

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(nums(5), 25, "Testing the function nums on input 5.")
         self.assertEqual(nums(2, mult_int = 4), 8, "Testing the function nums on inputs 2, mult_int = 4.")
         self.assertEqual(nums(3, switch = True), -15, "Testing the function nums on inputs 3, switch = True.")
         self.assertEqual(nums(4, mult_int = 3, switch = True), -12, "Testing the function nums on inputs 4, mult_int = 3, switch = True.")
         self.assertEqual(nums(0, switch = True), 0, "Testing the function nums on inputs 0, switch = True.")

   myTests().main()  


4. Define a function called ``connect`` that takes two inputs. The first, a required parameter, should be a list of strings. The second, an optional parameter named ``connector``, should have a default value of "_" but can take any string as input. The function should return one long string that contains all the original strings concatenated together, joined by the connector string.

.. activecode:: ee_optparams_04
   :tags: OptionalAndKeywordParameters/OptionalParameters.rst

   def connect():

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(connect(["hi", "bye", "yo"]), "hi_bye_yo", "Testing the function connect on input ['hi', 'bye', 'yo'].")
         self.assertEqual(connect(["a", "b", "c"], connector = "--"), "a--b--c", "Testing the function connect on inputs ['a', 'b', 'c'], connector = '--'.")
         self.assertEqual(connect(["x", "y", "z"], connector = "1234"), "x1234y1234z", "Testing the function connect on inputs ['x', 'y', 'z'], connector = '1234'.")
         self.assertEqual(connect([]), '', "Testing the function connect on input [].")
         self.assertEqual(connect(["solo"]), "solo", "Testing the function connect on input ['solo'].")


   myTests().main()    


5. Below, we've provided the function ``nums`` that you previously defined. You must pass the correct inputs into the function so that it returns the values listed in the ActiveCode window. **Note:** You should only pass positive integers into the function (i.e.: If asked to produce a negative output, do so by using the switch argument!)

.. activecode:: ee_optparams_05
   :tags: OptionalAndKeywordParameters/KeywordParameters.rst

   def nums(int1, mult_int=5, switch=False):
       if switch == False: 
           return int1 * mult_int
       if switch == True: 
           return (int1 * mult_int) * -1

   # Below, make the function return the value 10, and save it to the variable name output1


   # Below, make the function return the value -12, and save it to the variable name output2


   # Below, make the function return the value -25, and save it to the variable name output3


   # Below, make the function return the value -5, and save it to the variable name output4


   # Below, make the function return the value 56, and save it to the variable name output5


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(output1, 10, "Testing that output1 was assigned correctly.")
         self.assertEqual(output2, -12, "Testing that output2 was assigned correctly.")
         self.assertEqual(output3, -25, "Testing that output3 was assigned correctly.")
         self.assertEqual(output4, -5, "Testing that output4 was assigned correctly.")
         self.assertEqual(output5, 56, "Testing that output5 was assigned correctly.")

   myTests().main() 



