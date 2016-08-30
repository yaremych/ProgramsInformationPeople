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

1. Sort the list below, ``animals``, into alphabetical order. Save the new list as ``animals_sorted``. 

.. activecode:: ee_sort_01
   :tags: Sort/intro-SortingwithSortandSorted.rst

   animals = ['elephant', 'cat', 'moose', 'antelope', 'elk', 'rabbit', 'zebra', 'yak', 'salamander', 'deer', 'otter', 'minx', 'giraffe', 'goat', 'cow', 'tiger', 'bear']

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(animals_sorted, ['antelope', 'bear', 'cat', 'cow', 'deer', 'elephant', 'elk', 'giraffe', 'goat', 'minx', 'moose', 'otter', 'rabbit', 'salamander', 'tiger', 'yak', 'zebra'], "Testing that animals_sorted was created correctly.")

   myTests().main()


2. Below, we have provided the dictionary ``groceries``, whose keys are grocery items, and values are the number of each item that you need to buy at the store. Sort the dictionary's keys into alphabetical order, and save them as a list called ``grocery_keys_sorted``. 

.. activecode:: ee_sort_02
   :tags: Sort/intro-SortingwithSortandSorted.rst, Sort/SortingaDictionary.rst

   groceries = {'apples': 5, 'pasta': 3, 'carrots': 12, 'orange juice': 2, 'bananas': 8, 'popcorn': 1, 'salsa': 3, 'cereal': 4, 'coffee': 5, 'granola bars': 15, 'onions': 7, 'rice': 1, 'peanut butter': 2, 'spinach': 9}

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(grocery_keys_sorted, ['apples', 'bananas', 'carrots', 'cereal', 'coffee', 'granola bars', 'onions', 'orange juice', 'pasta', 'peanut butter', 'popcorn', 'rice', 'salsa', 'spinach'], "Testing that grocery_keys_sorted was created correctly.")

   myTests().main()  


3. Once again, we have provided the dictionary ``groceries``. Once again, you should return a list of its keys, but this time they should be sorted by their values, from highest to lowest. Save the new list as ``most_needed``. 

.. activecode:: ee_sort_03
   :tags: Sort/intro-SortingwithSortandSorted.rst, Sort/SortingaDictionary.rst, Sort/Optionalreverseparameter.rst, Sort/Optionalkeyparameter.rst
 
   groceries = {'apples': 5, 'pasta': 3, 'carrots': 12, 'orange juice': 2, 'bananas': 8, 'popcorn': 1, 'salsa': 3, 'cereal': 4, 'coffee': 5, 'granola bars': 15, 'onions': 7, 'rice': 1, 'peanut butter': 2, 'spinach': 9}

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(most_needed, ['granola bars', 'carrots', 'spinach', 'bananas', 'onions', 'coffee', 'apples', 'cereal', 'salsa', 'pasta', 'peanut butter', 'orange juice', 'rice', 'popcorn'], "Testing that most_needed was created correctly.")

   myTests().main() 



4. Below, we have provided a list of strings called ``nums``. Write a function called ``last_char`` that takes a string as input, and returns only its last character. Use this function to sort the list ``nums`` by the last digit of each number, from highest to lowest, and save this as a new list called ``nums_sorted``. 

.. activecode:: ee_sort_04
   :tags: Sort/intro-SortingwithSortandSorted.rst, Sort/Optionalreverseparameter.rst, Sort/Optionalkeyparameter.rst

   nums = ['1450', '33', '871', '19', '14378', '32', '1005', '44', '8907', '16']

   def last_char(): 

   nums_sorted = 

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testA(self):
         self.assertEqual(nums_sorted, ['19', '14378', '8907', '16', '1005', '44', '33', '32', '871', '1450'], "Testing that nums_sorted was created correctly.")
      def testB(self): 
         self.assertEqual(last_char('pants'), 's', "Testing the function last_char on input 'pants'.")


   myTests().main() 


5. Once again, sort the list ``nums`` based on the last digit of each number from highest to lowest. However, now you should do so by writing a lambda function. Save the new list as ``nums_sorted_lambda``. 

.. activecode:: ee_sort_05
   :tags: Sort/intro-SortingwithSortandSorted.rst, Sort/Anonymousfunctionswithlambdaexpressions.rst, Sort/Optionalreverseparameter.rst

   nums = ['1450', '33', '871', '19', '14378', '32', '1005', '44', '8907', '16']

   nums_sorted_lambda = 

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testA(self):
         self.assertEqual(nums_sorted_lambda, ['19', '14378', '8907', '16', '1005', '44', '33', '32', '871', '1450'], "Testing that nums_sorted_lambda was created correctly.")


   myTests().main() 


6. **Challenge:** Below, we have provided the nested dictionary ``medals`` that describes how many medals the USA won in various sports at the Rio Olympics. Write code to sort the sports in ``medals`` based on the total number of medals that were won, from highest to lowest. Save the list of sorted sports as ``sorted_sports``. Save the sport with the most medals as ``most_medals`` and the sport with the least medals as ``least_medals``. 

.. activecode:: ee_sort_06
   :tags: Sort/intro-SortingwithSortandSorted.rst, Sort/Optionalreverseparameter.rst, Sort/Optionalkeyparameter.rst, Sort/Anonymousfunctionswithlambdaexpressions.rst, Sort/SortingaDictionary.rst

   medals = {'gymnastics': {'gold': 4, 'silver': 6, 'bronze': 2}, 'basketball': {'gold': 2, 'silver': 0, 'bronze': 0}, 'fencing': {'gold': 0, 'silver': 2, 'bronze': 2}, 'swimming': {'gold': 16, 'silver': 8, 'bronze': 9}, 'wrestling': {'gold': 2, 'silver': 0, 'bronze': 1}, 'volleyball': {'gold': 0, 'silver': 0, 'bronze': 2}, 'track & field': {'gold': 13, 'silver': 10, 'bronze': 9}, 'boxing': {'gold': 1, 'silver': 1, 'bronze': 1}, 'diving': {'gold': 0, 'silver': 2, 'bronze': 1}, 'water polo': {'gold': 1, 'silver': 0, 'bronze': 0}}

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testA(self):
         self.assertEqual(sorted_sports, ['swimming', 'track & field', 'gymnastics', 'fencing', 'diving', 'boxing', 'wrestling', 'volleyball', 'basketball', 'water polo'], "Testing that sorted_sports was created correctly.")
      def testB(self): 
         self.assertEqual(most_medals, 'swimming', "Testing that most_medals was assigned correctly.")
      def testC(self): 
         self.assertEqual(least_medals, 'water polo', "Testing that least_medals was asigned correctly.")


   myTests().main()  






