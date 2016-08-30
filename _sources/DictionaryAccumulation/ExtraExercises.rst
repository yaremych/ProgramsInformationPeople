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

1. The dictionary ``travel`` contains the number of countries within each continent that Jackie has traveled to. Find the total number of countries that Jackie has been to, and save this number to the variable name ``total``. Do not hard code this! 

.. activecode:: ee_ch13_01
   :tags: DictionaryAccumulation/AccumulatingResultsFromaDictionary.rst

   travel = {"North America": 2, "Europe": 8, "South America": 3, "Asia": 4, "Africa":1, "Antarctica": 0, "Australia": 1}

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(total, 19, "Testing that total is correct.")

   myTests().main()



2. Provided is a string saved to the variable name ``s1``. Create a dictionary named ``counts`` that contains each letter in ``s1`` and the number of times it occurs. 

.. activecode:: ee_ch13_02
   :tags: DictionaryAccumulation/intro-AccumulatingMultipleResultsInaDictionary.rst

   s1 = "hello"

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sorted(counts.items()), [('e', 1), ('h', 1), ('l', 2), ('o', 1)], "Testing that counts was created correctly.")

   myTests().main()




3. Provided is a string saved to the variable name ``sentence``. Split the string into a list of words, then create a dictionary that contains each word and the number of times it occurs. Save this dictionary to the variable name ``word_counts``. 

.. activecode:: ee_ch13_03
   :tags: DictionaryAccumulation/intro-AccumulatingMultipleResultsInaDictionary.rst

   sentence = "The dog chased the rabbit into the forest but the rabbit was too quick."

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sorted(word_counts.items()), sorted([('The', 1), ('dog', 1), ('chased', 1), ('the', 3), ('rabbit', 2), ('into', 1), ('forest', 1), ('but', 1), ('was', 1), ('too', 1), ('quick.', 1)]), "Testing that word_counts was created correctly.")

   myTests().main()


4. Provided is a string saved to the variable name ``str1``. Using string methods and dictionary accumulation, find the word that occurs most often. Save the word to the variable name ``most_pop_word``. 

.. activecode:: ee_ch13_04
   :tags: DictionaryAccumulation/AccumulatingtheBestKey.rst, DictionaryAccumulation/AccumulatingaMaximumValue.rst

   str1 = "There are many many seasons and I often cannot decide which is my favorite. In the fall, there are many leaves falling and I really enjoy leaping in them. In the winter, there are many snowflakes that fall everywhere. I love both seasons!"

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(most_pop_word, 'many', "Testing that most_pop_word was assigned to the correct word.")

   myTests().main()


5. Create a dictionary that contains all the letters in ``quote`` and the number of times they occur. Then, find the letter that occurs the LEAST often. Save this letter to the variable name ``unpop``. 

.. activecode:: ee_ch13_05
   :tags: DictionaryAccumulation/AccumulatingtheBestKey.rst, DictionaryAccumulation/AccumulatingaMaximumValue.rst

   quote = "bananas and berries, ribs, series"

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(unpop, 'd', "Testing that upop was assigned to the correct letter.")

   myTests().main()



6. Create a dictionary named ``letter_counts`` that contains each letter and the number of times it occurs in ``string1``. **Challenge:** Letters should not be counted separately as upper-case and lower-case. 

.. activecode:: ee_ch13_06
   :tags: DictionaryAccumulation/intro-AccumulatingMultipleResultsInaDictionary.rst

   string1 = "There is a tide in the affairs of men, Which taken at the flood, leads on to fortune. Omitted, all the voyage of their life is bound in shallows and in miseries. On such a full sea are we now afloat. And we must take the current when it serves, or lose our ventures."

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(letter_counts['t'], 19, "Testing that the letter 't' has the correct value.")

      def testTwo(self):
         self.assertEqual(letter_counts['w'], 6, "Testing that the letter 'w' has the correct value.")

      def testThree(self):
         self.assertEqual(letter_counts['o'], 17, "Testing that the letter 'o' has the correct value.")

      def testFour(self):
         self.assertEqual(letter_counts['a'], 17, "Testing that the letter 'a' has the correct value.")



   myTests().main()









