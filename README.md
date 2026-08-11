# GU-A-DE-TRABAJO-PR-CTICO-N-4-Arrays-y-Vectores


// 1
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            int contador = 0;
            double total = 0;
            double[] temperaturas = { 0, 0, 0, 0, 0, 0, 0 };
            double mayor = temperaturas[0], menor = temperaturas[6];


            for (int i = 0; i < temperaturas.Length; i++)
            {

                Console.WriteLine("Temperatura dia " + contador);
                temperaturas[contador] = Convert.ToDouble(Console.ReadLine());
                contador += 1;
            }

            mayor = temperaturas[0];
            menor = temperaturas[0];
            for (int i = 0; i < temperaturas.Length; i++)
            {

                total += temperaturas[i];
                if (temperaturas[i] > mayor)
                {
                    mayor = temperaturas[i];
                }
                else if (temperaturas[i] < menor)
                {
                    menor = temperaturas[i];
                }
            }

            double promedio = total / temperaturas.Length;
            Console.Write("MAYOR:" + mayor);
            Console.Write("MENOR: " + menor);
            Console.Write("PROMEDIO: " + promedio);

        }
    }
}


//2

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            int contador = 0;
            double total = 0;
            double[] notas = { 0,0,0,0,0,0,0,0,0,0 };
            double aprovado = 0, desaprovado = 0;


            for(int i = 0; i < notas.Length; i++)
            {

                Console.WriteLine("Calificacion (1-10) Alumno:" + (contador+1));
                notas[contador] = Convert.ToDouble(Console.ReadLine());
                contador += 1;
            }

           
            for (int i = 0; i < notas.Length; i++)
            {

                total += notas[i];
                if (notas[i] >= 6)
                {
                    aprovado += 1;
                }
                else if (notas[i] < 6)
                {
                    desaprovado += 1;
                }
            }


            double promedio = total / notas.Length;
            Console.Write("APRVADOS:"+aprovado);
            Console.Write("DESAPROVADOS: "+desaprovado);
            Console.Write("PROMEDIO: " + promedio);

        }
    }
}
