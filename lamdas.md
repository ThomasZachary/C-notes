`using System;
namespace ConsoleApp1
{
  class Program
  {
		// define the delegates
		public delegate string MyD(string s);

    // define the static methods that have the same parameter pattern as the delegate
    static string D_1(string s)
    {
      return s + " D1";
    }

    static string D_2(string s)
    {
      return s + " D2";
    }

    static string D_3(string s)
    {
      return s + " D3";
    }

    static void Main(string[] args)
    {
      // create an instance of the delegate
      // notice, I'm not using the "new" command
      MyD _md1 = D_1;
      Console.WriteLine(_md1("passed"));

      // now dynamically re-assign the same delegate to a different method
      _md1 = D_2;
      Console.WriteLine(_md1("passed"));

      // and again
      _md1 = D_3;
      Console.WriteLine(_md1("passed"));

      Console.ReadLine();
    }
  }
}`
