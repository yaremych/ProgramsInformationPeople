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

1. Create a dictionary that keeps track of the USA's Olympic medal count. Each key of the dictionary should be the type of medal (gold, silver, bronze) and the value should be the number of medals. Currently, the USA has 33 gold medals, 17 silver, and 12 bronze. Create a dictionary named ``medals`` that reflect this. 

.. activecode:: ee_ch12_01
   :tags: Dictionaries/intro-Dictionaries.rst



   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sorted(medals.items()), sorted([("gold", 33), ("silver", 17), ("bronze", 12)]), "Testing that medals is correct.")

   myTests().main()



2. Every four years, the summer Olympics are held in a different country. Add a key-value pair to the dictionary ``places`` that reflects that the 2016 Olympics were held in Brazil. Do not rewrite the entire dictionary to do this! 

.. activecode:: ee_ch12_02
   :tags: Dictionaries/intro-Dictionaries.rst

   places = {"Australia":2000, "Greece":2004, "China":2008, "England":2012}

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sorted(places.items()), sorted([("Australia", 2000), ("Greece", 2004), ("China", 2008), ("England", 2012), ("Brazil", 2016)]), "Testing that places has been updated correctly.")

   myTests().main()


3. The dictionary ``golds`` contains information about how many gold medals each country won in the 2016 Olympics. Today, Spain won 2 more gold medals. Update ``golds`` to reflect this information. 

.. activecode:: ee_ch12_03
   :tags: Dictionaries/Dictionaryoperations.rst

   golds = {"Italy": 12, "USA": 33, "Brazil": 15, "China": 27, "Spain": 19, "Canada": 22, "Argentina": 8, "England": 29}


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sorted(golds.items()), sorted([("Italy", 12), ("USA", 33), ("Brazil", 15), ("China", 27), ("Spain", 21), ("Canada", 22), ("Argentina", 8), ("England", 29)]), "Testing that golds has been updated correctly.")

   myTests().main()



4. Create a list of the countries that are in the dictionary ``golds``, and assign it to the variable name ``countries``. Do not hard code this. 

.. activecode:: ee_ch12_04
   :tags: Dictionaries/Dictionarymethods.rst

   golds = {"Italy": 12, "USA": 33, "Brazil": 15, "China": 27, "Spain": 19, "Canada": 22, "Argentina": 8, "England": 29}

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sorted(countries), sorted(["Italy", "USA", "Brazil", "China", "Spain", "Canada", "Argentina", "England"]), "Testing that countries has been created correctly.")

   myTests().main()



5. The dictionary ``total_golds`` contains the total number of gold medals that countries have won over the course of history. Use a dictionary method to find the number of golds Chile has won, and assign that number to the variable name ``chile_golds``. Do not hard code this!  

.. activecode:: ee_ch12_05
   :tags: Dictionaries/Dictionarymethods.rst

   total_golds = {"Italy": 114, "Germany": 782, "Pakistan": 10, "Sweden": 627, "USA": 2681, "Zimbabwe": 8, "Greece": 111, "Mongolia": 24, "Brazil": 108, "Croatia": 34, "Algeria": 15, "Switzerland": 323, "Yugoslavia": 87, "China": 526, "Egypt": 26, "Norway": 477, "Spain": 133, "Australia": 480, "Slovakia": 29, "Canada": 22, "New Zealand": 100, "Denmark": 180, "Chile": 13, "Argentina": 70, "Thailand": 24, "Cuba": 209, "Uganda": 7,  "England": 806, "Denmark": 180, "Ukraine": 122, "Bahamas": 12}

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(chile_golds, 13, "Testing that chile_golds has been set correctly.")

   myTests().main()



6. **Challenge Problem:** The list ``current`` contains some of the sports that were played in the 2016 Olympics. The dictionary ``sport_counts`` contains some of the sports that have been played in prior Olympic meets, and how many Olympic meets they were played in. Iterate through each sport in the dictionary ``sport_counts`` and update its value by 1 if it was played in 2016 (if it was not played in 2016, its value should not be changed).

.. activecode:: ee_ch12_06
   :tags: Dictionaries/Dictionaryoperations.rst

   current = ["basketball", "soccer", "volleyball", "gymnastics", "wrestling", "golf", "equestrian", "swimming", "diving"]

   sport_counts = {"equestrian": 30, "tug of war": 3, "soccer": 15, "basketball": 8, "polo": 20, "swimming": 32, "gymnastics": 20, "diving": 24, "cricket": 12, "volleyball": 11, "croquet": 9}

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sorted(sport_counts.items()), sorted([("equestrian", 31), ("tug of war", 3), ("soccer", 16), ("basketball", 9), ("polo", 20), ("swimming", 33), ("gymnastics", 21), ("diving", 25), ("cricket", 12), ("volleyball", 12), ("croquet", 9)]), "Testing that sport_counts has been updated correctly.")

   myTests().main()











