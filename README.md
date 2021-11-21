
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.IO;

namespace laba1
{
    class Pro
    {
        static void Main(string[] args)
        {
            StreamWriter p = new StreamWriter("rez.txt");
            float a, x, y;
            p.WriteLine("Результат");
            for (a = 1; a <= 2; a += 0.5f)
            {
                p.WriteLine("a=" + a);
                for (x = 1; x <= 7; x += 0.25f)
                {
                    y = (float)(1 / Math.Sqrt(Math.Pow(1 - x * x, 1 / 2) + 4 * a * a * x * x));
                    p.WriteLine(" x= " + x + '\t' + " y= " + y);
                    p.Close();
                }
            }
        }        
    }
}
