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

1. Using a while loop, create a list called ``L`` that contains the numbers 0 to 10. (i.e.: Your while loop should initialize a counter variable to 0. On each iteration, the loop should append the current value of the counter variable to ``L`` and then increase the counter by 1. The while loop should stop once the counter variable is greater than 10.)

.. activecode:: ee_ch7_01 
   :tags: IndefiniteIteration/ThewhileStatement.rst


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(L, [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10], "Testing that L was created correctly.")

   myTests().main()


2. Use a while loop to iterate through the numbers 0 through 35. If a number is divisible by 3, it should be appended to a list called ``three_nums``. 

.. activecode:: ee_ch7_02
   :tags: IndefiniteIteration/ThewhileStatement.rst


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(three_nums, [0, 3, 6, 9, 12, 15, 18, 21, 24, 27, 30, 33], "Testing that three_nums was created correctly.")

   myTests().main()


3. Write a function called ``stop_at_four`` that iterates through a list of numbers. Using a while loop, append each number to a new list until the number 4 appears. The function should return the new list. 

.. activecode:: ee_ch7_03
   :tags: IndefiniteIteration/listenerLoop.rst

   def stop_at_four():



   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(stop_at_four([0, 9, 4.5, 1, 7, 4, 8, 9, 3]), [0, 9, 4.5, 1, 7], "Testing the function stop_at_four on the input [0, 9, 4.5, 1, 7, 4, 8, 9, 3].")
         self.assertEqual(stop_at_four([4, 1, 2, 8]), [], "Testing the function stop_at_four on the input [4, 1, 2, 8].")
         self.assertEqual(stop_at_four([4]), [], "Testing the function stop_at_four on the input [4].")

   myTests().main()  



4. Write a function called ``stop_at_z`` that iterates through a list of strings. Using a while loop, append each letter to a new list until the string that appears is "z". The function should return the new list. 

.. activecode:: ee_ch7_04
   :tags: IndefiniteIteration/listenerLoop.rst

   def stop_at_z():



   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(stop_at_z(['c', 'b', 'd', 'zebra', 'h', 'r', 'z', 'm', 'a', 'k']), ['c', 'b', 'd', 'zebra', 'h', 'r'], "Testing the function stop_at_z on the input ['c', 'b', 'd', 'zebra', 'h', 'r', 'z', 'm', 'a', 'k'].")
         self.assertEqual(stop_at_z(['zoo', 'zika', 'ozzie', 'pizzazz', 'z', 'pizza', 'zap', 'haze']), ['zoo', 'zika', 'ozzie', 'pizzazz'], "Testing the function stop_at_four on the input ['zoo', 'zika', 'ozzie', 'pizzazz', 'z', 'pizza', 'zap', 'haze'].")
         self.assertEqual(stop_at_z(['z']), [], "Testing the function stop_at_four on the input ['z'].")

   myTests().main()  


5. Below, we've provided a for loop that sums all the elements of ``list1``. Write code that accomplishes the same task, but instead uses a while loop. Assign the accumulator variable to the name ``accum``. 

.. activecode:: ee_ch7_05
   :tags: IndefiniteIteration/ThewhileStatement.rst

   list1 = [8, 3, 4, 5, 6, 7, 9]

   tot = 0
   for elem in list1: 
       tot = tot + elem

   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(accum, 42, "Testing that accum has the correct value.")

   myTests().main()   




6. **Ultra Challenge:** Write a function called ``too_big`` that takes a list of numbers as input and produces a new list of numbers as output. Using a while loop, the function should output a list of only even numbers from the list that is passed in. It should stop once there are 5 elements in the new list, OR once the sum of all the numbers in the new list is greater than 30 - whichever comes first. 

.. activecode:: ee_ch7_06
   :tags: IndefiniteIteration/listenerLoop.rst

   def too_big(): 

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(too_big([12, 19, 5, 10, 10, 13, 4, 16]), [12, 10, 10], "Testing the function too_big on the input [12, 19, 5, 10, 10, 13, 4, 16].")
         self.assertEqual(too_big([2, 3, 4, 5, 2, 2, 7, 2, 4, 19, 6, 5, 4, 2, 2]), [2, 4, 2, 2, 2], "Testing the function too_big on the input [2, 3, 4, 5, 2, 2, 7, 2, 4, 19, 6, 5, 4, 2, 2].")



   myTests().main()   





















