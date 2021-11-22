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
            for (a = 0.2f; a <= 0.4; a += 0.1f)
            {
                p.WriteLine("a=" + a);
                for (x = 0; x <= 2; x += 0.05f)
                {
                    y = (float)(1 / Math.Sqrt(Math.Pow(1 - x * x, 1 / 2) + 4 * a * a * x * x));
                    p.WriteLine(" x= " + x + '\t' + " y= " + y);
                   
                }
            }
            p.Close();
        }
    }
}
