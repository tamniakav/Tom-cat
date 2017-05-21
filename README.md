using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Tom_cat
{
    class Program
    {
        static void Main(string[] args)
        {
            int dayOff = int.Parse(Console.ReadLine());

            int workDays = 365 - dayOff;

            int playTime = (dayOff * 127) + (workDays * 63);

            int diferenceTime = 30000 - playTime;

            int dT = Math.Abs(diferenceTime);

            int H = dT / 60;
            int M = dT % 60;

            if (playTime > 30000)
            {
                Console.WriteLine("Tom will run away");
                Console.WriteLine($"{H} hours and {M} minutes more for play");
            }
            else
            {
                Console.WriteLine("Tom sleeps well");
                Console.WriteLine($"{H} hours and {M} minutes less for play");
            }
        }
    }
}
