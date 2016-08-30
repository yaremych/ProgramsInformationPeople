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

1. Below, we have provided a list of tuples that consist of student names, final exam scores, and whether or not they will pass the class. For some students, the tuple does not have a third element because it is unknown whether or not they will pass. Currently, the for loop does not work. Add a try/except clause so the code runs without an error - if there is no third element in the tuple, no changes should be made to the dictionary.

.. activecode:: ee_exceptions_01
   :tags: Exceptions/intro-exceptions.rst

   students = [('Timmy', 95, 'Will pass'), ('Martha', 70), ('Betty', 82, 'Will pass'), ('Stewart', 50, 'Will not pass'), ('Ashley', 68), ('Natalie', 99, 'Will pass'), ('Archie', 71), ('Carl', 45, 'Will not pass')]

   passing = {'Will pass': 0, 'Will not pass': 0}
   for tup in students:
       if tup[2] == 'Will pass':
           passing['Will pass'] += 1
       elif tup[2] == 'Will not pass':
           passing['Will not pass'] += 1

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(passing, {'Will pass': 3, 'Will not pass': 2}, "Testing that passing is created correctly.")

   myTests().main()


2. Below, we have provided code that does not run. Add a try/except clause so the code runs without errors. If an element is not able to undergo the addition operation, the string 'Error' should be appended to plus_four. 

.. activecode:: ee_exceptions_02
   :tags: Exceptions/intro-exceptions.rst

   nums = [5, 9, '4', 3, 2, 1, 6, 5, '7', 4, 3, 2, 6, 7, 8, '0', 3, 4, 0, 6, 5, '3', 5, 6, 7, 8, '3', '1', 5, 6, 7, 9, 3, 2, 5, 6, '9', 2, 3, 4, 5, 1]

   plus_four = []

   for num in nums: 
       plus_four.append(num+4)


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(plus_four, [9, 13, 'Error', 7, 6, 5, 10, 9, 'Error', 8, 7, 6, 10, 11, 12, 'Error', 7, 8, 4, 10, 9, 'Error', 9, 10, 11, 12, 'Error', 'Error', 9, 10, 11, 13, 7, 6, 9, 10, 'Error', 6, 7, 8, 9, 5], "Testing that plus_four is created correctly.")

   myTests().main()


3. The following code tries to append the third element of each list in ``conts`` to the new list ``third_countries``. Currently, the code does not work. Add a try/except clause so the code runs without errors, and the string 'Continent does not have 3 countries' is appended to ``countries`` instead of producing an error.

.. activecode:: ee_exceptions_03
   :tags: Exceptions/intro-exceptions.rst

   conts = [['Spain', 'France', 'Greece', 'Portugal', 'Romania', 'Germany'], ['USA', 'Mexico', 'Canada'], ['Japan', 'China', 'Korea', 'Vietnam', 'Cambodia'], ['Argentina', 'Chile', 'Brazil', 'Ecuador', 'Uruguay', 'Venezuela'], ['Australia'], ['Zimbabwe', 'Morocco', 'Kenya', 'Ethiopa', 'South Africa'], ['Antarctica']]

   third_countries = []

   for c in conts: 
       third_countries.append(c[2])


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(third_countries, ['Greece', 'Canada', 'Korea', 'Brazil', 'Continent does not have 3 countries', 'Kenya', 'Continent does not have 3 countries'], "Testing that third_countries is created correctly.")

   myTests().main()   


4. Below, we have provided buggy code. Add a try/except clause so the code runs without errors. If a blog post didn't get any likes, a 'Likes' key should be added to that dictionary with a value of 0.

.. activecode:: ee_exceptions_04
   :tags: Exceptions/intro-exceptions.rst

   blog_posts = [{'Photos': 3, 'Likes': 21, 'Comments': 2}, {'Likes': 13, 'Comments': 2, 'Shares': 1}, {'Photos': 5, 'Likes': 33, 'Comments': 8, 'Shares': 3}, {'Comments': 4, 'Shares': 2}, {'Photos': 8, 'Comments': 1, 'Shares': 1}, {'Photos': 3, 'Likes': 19, 'Comments': 3}]

   total_likes = 0

   for post in blog_posts: 
       total_likes = total_likes + post['Likes']

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testA(self):
         self.assertEqual(total_likes, 86, "Testing that total_likes has the correct value.")
      def testB(self):
         accum = 0
         for d in blog_posts: 
            if 'Likes' in d:
               accum +=1
         self.assertEqual(accum, 6, "Testing that blog_post dictionaries all have a 'Likes' key.")   

   myTests().main()  






