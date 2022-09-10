using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.IO;

namespace RetrieveStudentData
{
   
        internal class Program
        {
            static void Main(string[] args)
            {
            // File.Create("StudentData.txt");
                FileStream fs = new FileStream("StudentData.txt", FileMode.Open, FileAccess.Read);
            StreamReader sr = new StreamReader(fs);
            while (true)
            {
                string ans  = sr.ReadLine();
                if(ans == null)
                {
                    Console.WriteLine("Last Data...");
                    break;
                }
                Console.WriteLine("Student Name : " + ans);
            }



            }
        }
    }


