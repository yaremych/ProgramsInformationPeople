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

.. datafile:: emotion_words.txt
   :hide: 

   Sad upset blue down melancholy somber bitter troubled
   Angry mad enraged irate irritable wrathful outraged infuriated
   Happy cheerful content elated joyous delighted lively glad
   Confused disoriented puzzled perplexed dazed befuddled
   Excited eager thrilled delighted
   Scared afraid fearful panicked terrified petrified startled
   Nervous anxious jittery jumpy tense uneasy apprehensive



1. We have provided a file called ``emotion_words.txt`` that contains lines of words that describe emotions. Find the total number of words in the file and assign this value to the variable ``num_words``. 

.. activecode:: ee_files_01
   :tags: Files/intro-WorkingwithDataFiles.rst, Files/Iteratingoverlinesinafile.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(num_words, 48, "Testing that num_words was assigned to the correct value.")

   myTests().main()


2. Write code to find out how many lines are in the file ``emotion_words.txt``. Save this value to the variable ``num_lines``. 

.. activecode:: ee_files_02
   :tags: Files/intro-WorkingwithDataFiles.rst, Files/Iteratingoverlinesinafile.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(num_lines, 7, "Testing that num_lines was assigned to the correct value.")

   myTests().main() 


3. Create a string called ``first_forty`` that is comprised of the first 40 characters of ``emotion_words.txt``. 

.. activecode:: ee_files_03 
   :tags: Files/intro-WorkingwithDataFiles.rst 

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(first_forty, 'Sad upset blue down melancholy somber bit', "Testing that first_forty was created correctly.")
   myTests().main()    


4. **Challenge:** Create a list called ``emotions`` that contains the first word of every line in ``emotion_words.txt``. 

.. activecode:: ee_files_04
   :tags: Files/intro-WorkingwithDataFiles.rst, Files/Iteratingoverlinesinafile.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(emotions, ['Sad', 'Angry', 'Happy', 'Confused', 'Excited', 'Scared', 'Nervous'], "Testing that emotions was created correctly.")

   myTests().main() 


5. **Challenge:** Create a list called ``j_emotions`` that contains every word in ``emotion_words.txt`` that begins with the letter "j". 

.. activecode:: ee_files_05
   :tags: Files/intro-WorkingwithDataFiles.rst, 

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(j_emotions, ['joyous', 'jittery', 'jumpy'], "Testing that j_emotions was created correctly.")

   myTests().main() 





