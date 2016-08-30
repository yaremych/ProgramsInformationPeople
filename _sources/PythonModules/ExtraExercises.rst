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

1. The module called ``keyword`` has an attribute called kwlist that is a list of all Python keywords. Import the ``keyword`` module and assign this list to the variable ``kws``. Then, produce a list of all three-letter keywords and assign it to the variable ``kw3``. 

.. activecode:: ee_mod_01
   :tags: PythonModules/intro-ModulesandGettingHelp.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testA(self):
         self.assertEqual(kws, ['and', 'as', 'assert', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'exec', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'not', 'or', 'pass', 'print', 'raise', 'return', 'try', 'while', 'with', 'yield'], "Testing that kws was created correctly.")
      def testB(self):
         self.assertEqual(kw3, ['and', 'def', 'del', 'for', 'not', 'try'], "Testing that kw3 was created correctly.")

   myTests().main()


2. The ``operator`` module contains functions that correspond to mathematical operations (such as .add and .sub). Import the ``operator`` module and use the .pow method, which takes two numbers as input and returns the first number raised to the second number, on the variables ``a`` and ``b``. Assign the output to the variable ``c``. Then, use the .div method, which takes two numbers as input and returns the first number divided by the second number, to find ``c`` divided by ``d``. Save this output to the variable ``e``. 

.. activecode:: ee_mod_02
   :tags: PythonModules/intro-ModulesandGettingHelp.rst

   a = 5
   b = 8
   d = 125

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testA(self):
         self.assertEqual(c, 390625, "Testing that c has the correct value.")
      def testB(self):
         self.assertEqual(e, 3125, "Testing that e has the correct value.")

   myTests().main()


3. The ``math`` module contains mathematical functions, including trigonemetric ones. Import the ``math`` module and use the .sin, .cos, and .tan methods to prove that sin(0.6)/cos(0.6) = tan(0.6). Save sin(0.6) to the variable ``s``, save cos(0.6) to the variable ``c``, and save tan(0.6) to the variable ``t``. Test whether the two values are equal, and save the result - which will be a Boolean - to the variable ``test``. 

.. activecode:: ee_mod_03
   :tags: PythonModules/intro-ModulesandGettingHelp.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(test, True, "Testing that test has the correct value.")

   myTests().main()


4. The ``string`` module provides sequences of various types of Python characters. It has an attribute called digits that produces the string '0123456789'. Import the module and assign this string to the variable ``nums``. Below, we have provided a list of characters called ``chars``. Using ``nums`` and ``chars``, produce a list called ``is_num`` that consists of tuples. The first element of each tuple should be the character from ``chars``, and the second element should be a Boolean that reflects whether or not it is a Python digit. 

.. activecode:: ee_mod_04
   :tags: PythonModules/intro-ModulesandGettingHelp.rst

   chars = ['h', '1', 'C', 'i', '9', 'True', '3.1', '8', 'F', '4', 'j']

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(is_num, [('h', False), ('1', True), ('C', False), ('i', False), ('9', True), ('True', False), ('3.1', False), ('8', True), ('F', False), ('4', True), ('j', False)], "Testing that is_num was created correctly.")

   myTests().main()








