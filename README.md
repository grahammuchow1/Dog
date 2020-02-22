# Dog

Dog challenge

using System;
namespace DogTest
{
    //Create an enum Gender
    public enum Gender { Male,Female};
    //Create a class Dog
    class Dog
    {
        //Instance variables
        private string name;
        private string owner;
        private int age;
        private Gender gender;
        //Constructor
        public Dog(string name,string owner,int age,Gender gender)
        {
            this.name = name;
            this.owner = owner;
            this.age = age;
            this.gender = gender;
        }
        //Method bark used to print the bark sound
        public void Bark(int times)
        {
            for(int i = 0; i < times; i++)
            {
                Console.Write("Woof!");
            }
            Console.WriteLine();
        }
        //Method to get a dog went missing, means tag generator for dog
        public string GetTag()
        {
            string tag = "If lost, call "+owner+". ";
            if (gender == 0)
            {
                tag += "His name is " + name + " he is " + age.ToString();
            }
            else
            {
                tag += "Her name is " + name + " she is " + age.ToString();
            }
            if (age > 1)
            {
                tag += " years old.";
            }
            else
            {
                tag += " year old.";
            }
            return tag;
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            //Class Dog Test
            Dog puppy = new Dog("Orion", "Shawn", 1, Gender.Male); // create object instance
            puppy.Bark(3); // output: Woof!Woof!Woof!
            Console.WriteLine(puppy.GetTag()); // output: If lost, call Shawn. His name is Orion and he is 1 year old.

            Dog myDog =new Dog("Lileu", "Dale", 4, Gender.Female); // create object instance
            myDog.Bark(1); // output: Woof!
            Console.WriteLine(myDog.GetTag()); // output: If lost, call Dale. Her name is Lileu and she is 4 years old.
        }
    }
}
