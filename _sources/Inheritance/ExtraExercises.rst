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

1. The class ``Pokemon`` is provided below and describes a Pokemon and its leveling and evolving characteristics. An instance of the class is one pokemon that you create. ``GrassPokemon`` is a subclass that inherits from ``Pokemon`` but changes some characteristics such as boost values. For the subclass ``GrassPokemon``, add another method called ``action`` that returns the string "[name of pokemon] knows a lot of different moves!". Create an instance of the GrassPokemon class with the name as "Timmy". Assign this instance to the variable ``pok1``.

.. activecode:: ee_inheritance_01
   :tags:Inheritance/inheritVarsAndMethods.rst

   class Pokemon():
       attack = 12
       defense = 10
       health = 15
    
       def __init__(self, name, level = 5):
           self.name = name
           self.p_type = "Normal"
           self.level = level
       
       def train(self):
           self.update()
           self.attack_up()
           self.defense_up()
           self.health_up()
           self.level = self.level + 1
           if self.level%self.evolve == 0:
               return self.level, "Evolved!"
           else:
               return self.level
    
       def attack_up(self):
           self.attack = self.attack + self.attack_boost
           return self.attack
    
       def defense_up(self):
           self.defense = self.defense + self.defense_boost
           return self.defense
    
       def health_up(self):
           self.health = self.health + self.health_boost
           return self.health

       def update(self):
           self.health_boost = 5
           self.attack_boost = 3
           self.defense_boost = 2
           self.evolve = 10
        
       def __str__(self):
           self.update()
           return "Pokemon name: {}, Type: {}, Level: {}".format(self.name, self.p_type, self.level)

   class GrassPokemon(Pokemon):
       attack = 15
       defense = 14
       health = 12
    
       def update(self):
           self.health_boost = 6
           self.attack_boost = 2
           self.defense_boost = 3
           self.evolve = 12
        
       def moves(self):
           self.p_moves = ["razor leaf", "synthesis", "petal dance"]


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(pok1.action(), "Timmy knows a lot of different moves!", "Testing that the action method is correct and that pok1 was created correctly.")
      
   myTests().main()  


2. Write code to modify the GrassPokemon class so that when an instance is created, its default level is 8. (The default level for the Pokemon class should remain the same.) Create an instance of the GrassPokemon class whose name is 'Carl'.

.. activecode:: ee_inheritance_02
   :tags:Inheritance/inheritVarsAndMethods.rst,Inheritance/OverrideMethods.rst

   class Pokemon():
       attack = 12
       defense = 10
       health = 15
    
       def __init__(self, name, level = 5):
           self.name = name
           self.p_type = "Normal"
           self.level = level
       
       def train(self):
           self.update()
           self.attack_up()
           self.defense_up()
           self.health_up()
           self.level = self.level + 1
           if self.level%self.evolve == 0:
               return self.level, "Evolved!"
           else:
               return self.level
    
       def attack_up(self):
           self.attack = self.attack + self.attack_boost
           return self.attack
    
       def defense_up(self):
           self.defense = self.defense + self.defense_boost
           return self.defense
    
       def health_up(self):
           self.health = self.health + self.health_boost
           return self.health

       def update(self):
           self.health_boost = 5
           self.attack_boost = 3
           self.defense_boost = 2
           self.evolve = 10
        
       def __str__(self):
           return "Pokemon name: {}, Type: {}, Level: {}".format(self.name, self.p_type, self.level)

   class GrassPokemon(Pokemon):
       attack = 15
       defense = 14
       health = 12
    
       def update(self):
           self.health_boost = 6
           self.attack_boost = 2
           self.defense_boost = 3
           self.evolve = 12
           self.p_type = "Grass"
        
       def moves(self):
           self.p_moves = ["razor leaf", "synthesis", "petal dance"]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(pok2.__str__(), "Pokemon name: Carl, Type: Grass, Level: 8", "Testing that pok2 was created correctly.")
      
   myTests().main()


3. Create a new subclass called ``SocialPokemon`` that inherits from the Pokemon class. It should keep the same attack, defense, and health stats, but it should have an additional stat called ``friends`` that should be initialized at 3 and boosted by 1 whenever the Pokemon is trained. Accomplish this by writing a ``friend_up`` method that resembles the defense_up and health_up methods. These pokemon should be the type "Social". Additionally, you should add a "Friends: {}" component to the string that is displayed when a SocialPokemon instance is printed. Create an instance of the SocialPokemon class whose name is 'Tina' and assign it to the variable ``pok3``. Train your pokemon twice.

.. activecode:: ee_inheritance_03
   :tags:Inheritance/inheritVarsAndMethods.rst,Inheritance/OverrideMethods.rst

   class Pokemon():
       attack = 12
       defense = 10
       health = 15
    
       def __init__(self, name, level = 5):
           self.name = name
           self.p_type = "Normal"
           self.level = level
       
       def train(self):
           self.update()
           self.attack_up()
           self.defense_up()
           self.health_up()
           self.level = self.level + 1
           if self.level%self.evolve == 0:
               return self.level, "Evolved!"
           else:
               return self.level
    
       def attack_up(self):
           self.attack = self.attack + self.attack_boost
           return self.attack
    
       def defense_up(self):
           self.defense = self.defense + self.defense_boost
           return self.defense
    
       def health_up(self):
           self.health = self.health + self.health_boost
           return self.health

       def update(self):
           self.health_boost = 5
           self.attack_boost = 3
           self.defense_boost = 2
           self.evolve = 10
        
       def __str__(self):
           return "Pokemon name: {}, Type: {}, Level: {}".format(self.name, self.p_type, self.level)

   class GrassPokemon(Pokemon):
       attack = 15
       defense = 14
       health = 12
    
       def update(self):
           self.health_boost = 6
           self.attack_boost = 2
           self.defense_boost = 3
           self.evolve = 12
           self.p_type = "Grass"
        
       def moves(self):
           self.p_moves = ["razor leaf", "synthesis", "petal dance"]


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testA(self):
         self.assertEqual(pok3.p_type, "Social", "Testing that pok3 has the type 'Social'.")
      def testB(self):
         self.assertEqual(pok3.friends, 5, "Testing that pok3 has the correct number of friends.")
      def testC(self):
         self.assertEqual(pok3.__str__(), "Pokemon name: Tina, Type: Social, Level: 7, Friends: 5", "Testing that pok3 prints correctly.")
      
   myTests().main() 



4. Create another subclass called SocialGrassPokemon that inherits from the GrassPokemon class. The new type should be 'Social/Grass'. This class should have a new method called ``strategies`` that returns a list of social strategies that the Pokemon may employ. The strategies should be 'friendship', 'teamwork', 'togetherness', and 'support'. Create an instance of the SocialGrassPokemon class whose name is 'Alfred' and save it to the variable ``pok4``. 

.. activecode:: ee_inheritance_04
   :tags: Inheritance/inheritVarsAndMethods.rst,Inheritance/OverrideMethods.rst

   class Pokemon():
       attack = 12
       defense = 10
       health = 15
    
       def __init__(self, name, level = 5):
           self.name = name
           self.p_type = "Normal"
           self.level = level
       
       def train(self):
           self.update()
           self.attack_up()
           self.defense_up()
           self.health_up()
           self.level = self.level + 1
           if self.level%self.evolve == 0:
               return self.level, "Evolved!"
           else:
               return self.level
    
       def attack_up(self):
           self.attack = self.attack + self.attack_boost
           return self.attack
    
       def defense_up(self):
           self.defense = self.defense + self.defense_boost
           return self.defense
    
       def health_up(self):
           self.health = self.health + self.health_boost
           return self.health

       def update(self):
           self.health_boost = 5
           self.attack_boost = 3
           self.defense_boost = 2
           self.evolve = 10
        
       def __str__(self):
           return "Pokemon name: {}, Type: {}, Level: {}".format(self.name, self.p_type, self.level)

   class GrassPokemon(Pokemon):
       attack = 15
       defense = 14
       health = 12
    
       def update(self):
           self.health_boost = 6
           self.attack_boost = 2
           self.defense_boost = 3
           self.evolve = 12
           self.p_type = "Grass"
        
       def moves(self):
           self.p_moves = ["razor leaf", "synthesis", "petal dance"]

   ====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(pok4.p_type, "Social/Grass", "Testing that the attribute p_type is now 'Social/Grass'.")
         self.assertEqual(sorted(pok4.strategies()), sorted(['friendship', 'teamwork', 'togetherness', 'support']), "Testing that pok4's strategies were created properly")
         self.assertEqual(pok4.__str__(), "Pokemon name: Alfred, Type: Social/Grass, Level: 5", "Testing that pok4 prints correctly.")

   myTests().main()



5. Provided is the Pokemon class along with four subclasses: Grass, Happy, Sad, and Confident. Create a method in the Parent class called ``display_mood`` that returns the following string: "[pokemon name] is feeling [mood attribute]." If the method is called on an instance that does not have the mood attribute (i.e.: Pokemon and GrassPokemon), the mood displayed should be 'normal'. Create an instance of Pokemon called ``p1`` named 'Aggron', an instance of GrassPokemon called ``g1`` named 'Bellsprout', an instance of HappyPokemon called ``h1`` named 'Charmander', an instance of SadPokemon called ``s1`` named 'Ditto', and an instance of ConfidentPokemon called ``c1`` named 'Eevee'. 

.. activecode:: ee_inheritance_05
   :tags: Inheritance/inheritVarsAndMethods.rst

   class Pokemon():
       attack = 12
       defense = 10
       health = 15
    
       def __init__(self, name, level = 5):
           self.name = name
           self.p_type = "Normal"
           self.level = level
       
       def train(self):
           self.update()
           self.attack_up()
           self.defense_up()
           self.health_up()
           self.level = self.level + 1
           if self.level%self.evolve == 0:
               return self.level, "Evolved!"
           else:
               return self.level
    
       def attack_up(self):
           self.attack = self.attack + self.attack_boost
           return self.attack
    
       def defense_up(self):
           self.defense = self.defense + self.defense_boost
           return self.defense
    
       def health_up(self):
           self.health = self.health + self.health_boost
           return self.health

       def update(self):
           self.health_boost = 5
           self.attack_boost = 3
           self.defense_boost = 2
           self.evolve = 10
        
       def __str__(self):
           return "Pokemon name: {}, Type: {}, Level: {}".format(self.name, self.p_type, self.level)

   class GrassPokemon(Pokemon):
       attack = 15
       defense = 14
       health = 12

       def update(self):
           self.health_boost = 6
           self.attack_boost = 2
           self.defense_boost = 3
           self.evolve = 12
           self.p_type = "Grass"
        
       def moves(self):
           self.p_moves = ["razor leaf", "synthesis", "petal dance"]

   class HappyPokemon(Pokemon):
       mood = 'happy'

       def update(self):
           Pokemon.update(self)
           self.p_type = "Happy"

   class SadPokemon(Pokemon):
       mood = 'sad'

       def update(self):
           Pokemon.update(self)
           self.p_type = "Sad"

   class ConfidentPokemon(Pokemon):
       mood = 'confident'

       def update(self):
           Pokemon.update(self)
           self.p_type = 'Confident'

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):
      p1.update()
      g1.update()
      h1.update()
      s1.update()
      c1.update()

      def testA(self):
         self.assertEqual(p1.display_mood(), 'Aggron is feeling normal.', "Testing the method display_mood on p1.")
      def testB(self):
         self.assertEqual(g1.display_mood(), 'Bellsprout is feeling normal.', "Testing the method display_mood on g1.")
      def testC(self):
         self.assertEqual(h1.display_mood(), 'Charmander is feeling happy.', "Testing the method display_mood on h1.")
      def testD(self):
         self.assertEqual(s1.display_mood(), 'Ditto is feeling sad.', "Testing the method display_mood on s1.")
      def testE(self):
         self.assertEqual(c1.display_mood(), 'Eevee is feeling confident.', "Testing the method display_mood on c1.")
         

   myTests().main()





