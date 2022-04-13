using System;
using System.Text;

namespace PasswordGenerator
{
    class Progmram
    {
        static void Main()
        {
            //Console.WriteLine("Какой ждины будет пароль?");
            //GeneratorPw.Lenght = Int32.Parse(Console.ReadLine());
            Console.Clear();
            Console.WriteLine("Пароль: {0}",GeneratorPw.PasswdGetSet());
            Console.ReadLine();
        }
    }
    class GeneratorPw
    {
        //static public int Lenght {get;set;}
        static public string PasswdGetSet()
        {
            Random rnd = new Random();
            StringBuilder Passwd = new StringBuilder ();
            for (int i = 0; i< 8; i++)
            {
                Passwd.Append((char)rnd.Next(50,100));
            }
            return Passwd.ToString();
        }
    }
}

