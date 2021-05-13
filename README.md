# workingWithCollections

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace workingWithCollections
{
    class Program
    {
        static void Main(string[] args)
        {

            Car car1 = new Car();
            car1.Make = "Oldsmobile";
            car1.Model = "Cutlas Supreme";

            Car car2 = new Car();
            car2.Make = "Geo";
            car2.Model = "Prism";

            Book b1 = new Book();
            b1.Author = "Robert Tabor";
            b1.Author = "Microsoft .NET XML Web Services";
            b1.ISBN = "0-000-00000-0";


            // ArrayLists are dynamically sized, and support other
            ///cool features like sorting, removing items. etc.

            /* System.Collections.ArrayList myArrayList = new System.Collections.ArrayList();
             myArrayList.Add(car1);
             myArrayList.Add(car2);
             myArrayList.Add(b1);
             myArrayList.Remove(b1);

             foreach (object o in myArrayList)
             {
                 Console.WriteLine(((Car)o).Make);
             }*/


            /*List<Car> mylist = new List<Car>();

            mylist.Add(car1);
            mylist.Add(car2);

            foreach (Car car in mylist)
            {
                Console.WriteLine(car.Model);
            }*/

            Dictionary<string, Car> myDictionary = new Dictionary<string, Car>();
            myDictionary.Add(car1.Make, car1);
            myDictionary.Add(car2.Make, car2);

            Console.WriteLine(myDictionary["Geo"].Model);


            Console.ReadLine();
        }
    }

    class Car
    { 
        public string Make { get; set; }
        public string Model { get; set; }
    }

    class Book
    {
        public string Title { get; set; }
        public string Author { get; set; }
        public string ISBN { get; set; }
    }
}
