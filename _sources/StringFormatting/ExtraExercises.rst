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

1. Below, we have provided a list of words. Use string formatting to produce the following string: "My favorite animals are elephants, giraffes, and zebras." Save this string to the variable name ``animal_string``. 

.. activecode:: ee_interpolation_01
   :tags: StringFormatting/Interpolation.rst

   animals = ['elephants', 'giraffes', 'zebras']

   animal_string = 

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(animal_string, "My favorite animals are elephants, giraffes, and zebras.", "Testing that animal_string is correct.")

   myTests().main()


2. Below, we have created the variables ``course`` and ``school``. Use string formatting to produce the following string: "I'm enrolled in SI 106 here at University of Michigan." Save this string to the variable name ``final``. 

.. activecode:: ee_interpolation_02
   :tags: StringFormatting/Interpolation.rst

   course = "SI 106"
   school = "University of Michigan"

   final = 

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(final, "I'm enrolled in SI 106 here at University of Michigan.", "Testing that final is correct.")

   myTests().main() 


3. Below, we have provided a list of tuples that contain information about summer Olympic meets. Create a new list called ``olympics_info`` using these tuples so that if the tuple is ('2016', 'Rio de Janeiro, Brazil'), then what is added to ``olympics_info`` is the string: "The 2016 Olympics were held in Rio de Janeiro, Brazil." Do this by using string interpolation. 

.. activecode:: ee_interpolation_03
   :tags: StringFormatting/Interpolation.rst

   tups = [('2016', 'Rio de Janeiro, Brazil'), ('2012', 'London, Great Britain'), ('2008', 'Beijing, China'), ('2004', 'Athens, Greece'), ('2000', 'Sydney, Australia'), ('1996', 'Atlanta, Georgia, USA'), ('1992', 'Barcelona, Spain'), ('1988', 'Seoul, Korea')]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(olympics_info, ['The 2016 Olympics were held in Rio de Janeiro, Brazil.', 'The 2012 Olympics were held in London, Great Britain.', 'The 2008 Olympics were held in Beijing, China.', 'The 2004 Olympics were held in Athens, Greece.', 'The 2000 Olympics were held in Sydney, Australia.', 'The 1996 Olympics were held in Atlanta, Georgia, USA.', 'The 1992 Olympics were held in Barcelona, Spain.', 'The 1988 Olympics were held in Seoul, Korea.'], "Testing that olympics_info is correct.")

   myTests().main()   


4. Write a function called ``grades`` that takes in a list with two elements, the first being a string (a person's name) and the second being an integer (their grade on a test). If the grade is greater than or equal to 70, the function should return: "Congrats, [name], you passed the test with a [grade]!" If the grade is lower than 70, the function should return: "Sorry, [name], you failed the test with a [grade]."

.. activecode:: ee_interpolation_04
   :tags: StringFormatting/Interpolation.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(grades(["Jenny", 90]), "Congrats, Jenny, you passed the test with a 90!", "Testing the function grades on input ['Jenny', 90].")
         self.assertEqual(grades(["Tina", 70]), "Congrats, Tina, you passed the test with a 70!", "Testing the function grades on input ['Tina', 70].")
         self.assertEqual(grades(["Betty", 45]), "Sorry, Betty, you failed the test with a 45.", "Testing the function grades on input ['Betty', 45].")

   myTests().main()    


5. Below, we have provided a list of tuples that contain information about customers' product reviews on Amazon: the product, its rating, and customer name. Write a function called ``feedback`` that takes a tuple as input and returns a message to the customer based on their review. If the customer rated their product as an 8 or higher, ``feedback`` should return the following string: "[name], we're happy to hear that you gave your new [product] a [rating] rating!" If the rating was below 8, ``feedback`` should return: "[name], we're sorry to hear that your new [product] was not excellent." Create a list called ``feedback_messages`` that contains a response to each customer below. 

.. activecode:: ee_interpolation_05
   :tags: StringFormatting/Interpolation.rst

   tups = [("Dyson vacuum", 9.1, "Sandy"), ("Keurig", 5.0, "Timmy"), ("SleepComfort mattress", 8.0, "Sam"), ("Michael Kors vest", 6.9, "Kate"), ("LG Dishwasher", 10.0, "Charles")]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(feedback_messages, ["Sandy, we're happy to hear that you gave your new Dyson vacuum a 9.1 rating!", "Timmy, we're sorry to hear that your new Keurig was not excellent.", "Sam, we're happy to hear that you gave your new SleepComfort mattress a 8 rating!", "Kate, we're sorry to hear that your new Michael Kors vest was not excellent.", "Charles, we're happy to hear that you gave your new LG Dishwasher a 10 rating!"], "Testing that feedback_messages is correct.")

   myTests().main()   








