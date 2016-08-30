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

1. Below, we have provided a list of lists. Use indexing to assign the element 'horse' to the variable name ``idx1``. 

.. activecode:: ee_nested_data_01
   :tags: NestedData/ListswithComplexItems.rst

   animals = [['cat', 'dog', 'mouse'], ['horse', 'cow', 'goat'], ['cheetah', 'giraffe', 'rhino']]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(idx1, 'horse', "Testing that idx1 was assigned correctly.")

   myTests().main()



2. Below, we've provided a list of lists. Use in statements to create variables with Boolean values - see the ActiveCode window for further directions. 

.. activecode:: ee_nested_data_02
   :tags: NestedData/ListswithComplexItems.rst

   L = [[5, 8, 7], ['hello', 'hi', 'hola'], [6.6, 1.54, 3.99], ['small', 'large']]

   # Test if 'hola' is in the list L. Save to variable name test1

   # Test if [5, 8, 7] is in the list L. Save to variable name test2

   # Test if 6.6 is in the third element of list L. Save to variable name test3

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testA(self):
         self.assertEqual(test1, False, "Testing that test1 has the correct value.")
      def testB(self):
         self.assertEqual(test2, True, "Testing that test2 has the correct value.")
      def testC(self):
         self.assertEqual(test3, True, "Testing that test3 has the correct value.")

   myTests().main()  


3. Below, we have provided a nested dictionary. Index into the dictionary to create variables that we have listed in the ActiveCode window. 

.. activecode:: ee_nested_data_03
   :tags: NestedData/NestedDictionaries.rst

   sports = {'swimming': ['butterfly', 'breaststroke', 'backstroke', 'freestyle'], 'diving': ['springboard', 'platform', 'synchronized'], 'track': ['sprint', 'distance', 'jumps', 'throws'], 'gymnastics': {'women':['vault', 'floor', 'uneven bars', 'balance beam'], 'men': ['vault', 'parallel bars', 'floor', 'rings']}}

   # Assign the string 'platform' to the name v1

   # Assign the string 'backstroke' to the name v2

   # Assign the list ['vault', 'floor', 'uneven bars', 'balance beam'] to the name v3

   # Assign the string 'rings' to the name v4

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testA(self):
         self.assertEqual(v1, 'platform', "Testing that v1 was created correctly.")
      def testB(self):
         self.assertEqual(v2, 'backstroke', "Testing that v2 was created correctly.")
      def testC(self):
         self.assertEqual(v3, ['vault', 'floor', 'uneven bars', 'balance beam'], "Testing that v3 was created correctly.")
      def testD(self):
         self.assertEqual(v4, 'rings', "Testing that v4 was created correctly.")

   myTests().main() 


4. Below, we have provided a list of lists that contain information about people. Write code to create a new list that contains every person's last name, and save that list as ``last_names``. 

.. activecode:: ee_nested_data_04
   :tags: NestedData/ListswithComplexItems.rst

   info = [['Tina', 'Turner', 1939, 'singer'], ['Matt', 'Damon', 1970, 'actor'], ['Kristen', 'Wiig', 1973, 'comedian'], ['Michael', 'Phelps', 1985, 'swimmer'], ['Barack', 'Obama', 1961, 'president']]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(last_names, ['Turner', 'Damon', 'Wiig', 'Phelps', 'Obama'], "Testing that last_names was created correctly.")

   myTests().main()



5. Below, we have provided a list of lists named ``L``. Use nested iteration to save every string containing "b" into a new list named ``b_strings``. 

.. activecode:: ee_nested_data_05
   :tags: NestedData/NestedIteration.rst

   L = [['apples', 'bananas', 'oranges', 'blueberries', 'lemons'], ['carrots', 'peas', 'cucumbers', 'green beans'], ['root beer', 'smoothies', 'cranberry juice']]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(b_strings, ['bananas', 'blueberries', 'cucumbers', 'green beans', 'root beer', 'cranberry juice'], "Testing that b_strings was created correctly.")

   myTests().main() 


6. **Challenge:** Below, we have provided a nested list called ``big_list``. Use nested iteration to create a dictionary, ``word_counts``, that contains all the words in ``big_list`` as keys, and the number of times they occur as values. 

.. activecode:: ee_nested_data_06
   :tags: NestedData/NestedIteration.rst

   big_list = [[['one', 'two'], ['seven', 'eight']], [['nine', 'four'], ['three', 'one']], [['two', 'eight'], ['seven', 'four']], [['five', 'one'], ['four', 'two']], [['six', 'eight'], ['two', 'seven']], [['three', 'five'], ['one', 'six']], [['nine', 'eight'], ['five', 'four']], [['six', 'three'], ['four', 'seven']]]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sorted(word_counts.items()), sorted([('eight', 4), ('five', 3), ('four', 5), ('nine', 2), ('one', 4), ('seven', 4), ('six', 3), ('three', 3), ('two', 4)]), "Testing that word_counts was created correctly.")

   myTests().main() 














