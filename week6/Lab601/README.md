# Lab601: Identify the design pattern and participants from the program (group of 2 students)

In this lab, each group of 2 students has to identify a design pattern and all participants 
from the provided C# source code. 

## Submission: a written report which contains

1. A class diagram of the original source code
	= http://www.uppic.biz/images/2015/10/02/Lab601.png
2. Detail explaination about the identified pattern and all the parcipants
	= �� Abstract Factory Medthod ����
		- class ContinentFactory �� AbstractFactory
		- class AmericaFactory ��� AfricaFactory �� ConcreteFactory
		- class AnimalWorld �� Client
		- class Herbivore ��� Carnivore �� AbstractProduct
		- class Wildebeest,Bison,Wolf,Lion �� Product
3. Explain how to include "an asian herbivore and an asian carnivore" to the program: 
  - Show the class diagram of the program after including the new requirment.
	= http://www.uppic.biz/images/2015/10/02/Lab601(Edit).png
  - Test the new requirment by modifying the main function and show the result.
	= http://www.uppic.biz/images/2015/10/02/Result_Lab601.jpg
  - Show the main function and snippet of C# code that is related to the process.
	
	class MainApp
  {
    public static void Main()
    {
      ContinentFactory africa = new AfricaFactory();
      AnimalWorld world = new AnimalWorld(africa);
      world.RunFoodChain();
 
      ContinentFactory america = new AmericaFactory();
      world = new AnimalWorld(america);
      world.RunFoodChain();

      ContinentFactory asia = new AsiaFactory();
      world = new AnimalWorld(asia);
      world.RunFoodChain();
            // Wait for user input
      Console.ReadKey();
    }

