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

1. Below, we have provided a list of strings called ``abbrevs``. Use map to produce a new list called ``abbrevs_upper`` that contains all the same strings in upper case. 

.. activecode:: ee_listcomp_01
   :tags: AdvancedAccumulation/map.rst

   abbrevs = ["usa", "esp", "chn", "jpn", "mex", "can", "rus", "rsa", "jam"]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(abbrevs_upper, ["USA", "ESP", "CHN", "JPN", "MEX", "CAN", "RUS", "RSA", "JAM"], "Testing that abbrevs_upper is correct.")

   myTests().main()


2. Below, we have provided a list of strings called ``countries``. Use filter to produce a list called ``b_countries`` that only contains the strings from ``countries`` that begin with B. 

.. activecode:: ee_listcomp_02
   :tags: AdvancedAccumulation/filter.rst

   countries = ['Canada', 'Mexico', 'Brazil', 'Chile', 'Denmark', 'Botswana', 'Spain', 'Britain', 'Portugal', 'Russia', 'Thailand', 'Bangladesh', 'Nigeria', 'Argentina', 'Belarus', 'Laos', 'Australia', 'Panama', 'Egypt', 'Morocco', 'Switzerland', 'Belgium']

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(b_countries, ['Brazil', 'Botswana', 'Britain', 'Bangladesh', 'Belarus', 'Belgium'], "Testing that b_countries is correct.")

   myTests().main()  


3. Below, we have provided a list of integers called ``nums``. Use reduce to produce a variable, ``product``, that is all of the integers in ``nums`` multiplied together. 

.. activecode:: ee_listcomp_03
   :tags: AdvancedAccumulation/reduce.rst

   nums = [5, 2, 3, 4, 8, 7, 6]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(product, 40320, "Testing that product is correct.")

   myTests().main()  


4. Below, we have provided a list of tuples that contain the names of Game of Thrones characters. Using list comprehension, create a list of strings called ``first_names`` that contains only the first names of everyone in the original list. 

.. activecode:: ee_listcomp_04
   :tags: AdvancedAccumulation/listcomp.rst

   people = [('Snow', 'Jon'), ('Lannister', 'Cersei'), ('Stark', 'Arya'), ('Stark', 'Robb'), ('Lannister', 'Jamie'), ('Targaryen', 'Daenerys'), ('Stark', 'Sansa'), ('Tyrell', 'Margaery'), ('Stark', 'Eddard'), ('Lannister', 'Tyrion'), ('Baratheon', 'Joffrey'), ('Bolton', 'Ramsey'), ('Baelish', 'Peter')]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(first_names, ['Jon', 'Cersei', 'Arya', 'Robb', 'Jamie', 'Daenerys', 'Sansa', 'Margaery', 'Eddard', 'Tyrion', 'Joffrey', 'Ramsey', 'Peter'], "Testing that first_names is correct.")

   myTests().main() 


5. Below, we have provided a list of tuples that contain students' names and their final grades in PYTHON 101. Using list comprehension, create a new list ``passed`` that contains the names of students who passed the class (had a final grade of 70 or greater). 

.. activecode:: ee_listcomp_05
   :tags: AdvancedAccumulation/listcomp.rst

   students = [('Tommy', 95), ('Linda', 63), ('Carl', 70), ('Bob', 100), ('Raymond', 50), ('Sue', 75)]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(passed, ['Tommy', 'Carl', 'Bob', 'Sue'], "Testing that passed is correct.")

   myTests().main()    


6. Below, we have provided a ``species`` list and a ``population`` list. Use zip to combine these lists into one list of tuples called ``pop_info``. From this list, create a new list called ``endangered`` that contains the names of species whose populations are below 2500. 

.. activecode:: ee_listcomp_06
   :tags: AdvancedAccumulation/zip.rst, AdvancedAccumulation/filter.rst

   species = ['golden retriever', 'white tailed deer', 'black rhino', 'brown squirrel', 'field mouse', 'orangutan', 'sumatran elephant', 'rainbow trout', 'black bear', 'blue whale', 'water moccasin', 'giant panda', 'green turtle', 'blue jay', 'japanese beetle']

   population = [10000, 90000, 1000, 2000000, 500000, 500, 1200, 8000, 12000, 2300, 7500, 100, 1800, 9500, 125000]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(pop_info, [('golden retriever', 10000), ('white tailed deer', 90000), ('black rhino', 1000), ('brown squirrel', 2000000), ('field mouse', 500000), ('orangutan', 500), ('sumatran elephant', 1200), ('rainbow trout', 8000), ('black bear', 12000), ('blue whale', 2300), ('water moccasin', 7500), ('giant panda', 100), ('green turtle', 1800), ('blue jay', 9500), ('japanese beetle', 125000)], "Testing that pop_info was created correctly.")
      def testTwo(self): 
         self.assertEqual(endangered, ['black rhino', 'orangutan', 'sumatran elephant', 'blue whale', 'giant panda', 'green turtle'], "Testing that endangered was created correctly.")

   myTests().main()   


7. **Challenge:** Below, we have provided a list of lists that contain numbers. Using list comprehension, create a new list ``threes`` that contains all the numbers from the original list that are divisible by 3. This can be accomplished in one line of code. 

.. activecode:: ee_listcomp_07
   :tags: AdvancedAccumulation/listcomp.rst, AdvancedAccumulation/filter.rst

   nums = [[4, 3, 12, 10], [8, 7, 6], [5, 18, 15, 7, 11], [9, 4], [24, 20, 17], [3, 5]]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(threes, [3, 12, 6, 18, 15, 9, 24, 3], "Testing that threes was created correctly.")

   myTests().main() 









