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

// 3

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
            int[] clases = { 0, 0, 0, 0,0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,0,0 };
            int inasistencias = 0;


            for (int i = 0; i < clases.Length; i++)
            {
                Console.WriteLine("Asistencias de [ALUMNO]:" + (contador + 1));
                Console.WriteLine("Escriba Presente/Aunsente (1/0)");
                clases[contador] = Convert.ToInt32(Console.ReadLine());
                if(clases[contador] != 1)
                {

                    inasistencias += 1;
              
                }
                contador += 1;
            }
            Console.WriteLine("[ALUMNO] falto :" + inasistencias + " veces");
            if (inasistencias>=6)
            {
                Console.WriteLine("[ALUMNO] [LIBRE POR FALTAS] ");
            }
            else
            {
                Console.WriteLine("[ALUMNO] [REGULAR]");
            }
          

        }
    }
}

// 4

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
            int[] productos = { 100, 200, 300, 400, 500, 666, 777, 800 };

            Console.WriteLine("Introduzca un monto de dinero");
            int monto = Convert.ToInt32(Console.ReadLine());
            //500
         
            for (int i = 0; i < productos.Length; i++)
            {
                Console.WriteLine("PRODUCTO:" + (contador + 1));

                if(productos[contador] <= monto)
                {
                    Console.WriteLine("Disponible");
                }
                else
                {
                    Console.WriteLine("Too expensive");
                }
                contador += 1;
            }

        }
    }
}

// 5

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
            int[] productos = { 0,1,2,3,4,5,6,7,8,9,10,11,12,13,14 };
            bool vendido = false;
            Console.WriteLine("Introduzca un numero para la rifa");
            int numero = Convert.ToInt32(Console.ReadLine());
            
            for (int i = 0; i < productos.Length; i++)
            {

                if(productos[contador] == numero)
                {
                    vendido = true;                  
                }
                
                contador += 1;
            }
            if(vendido==true)
            {
                Console.WriteLine("El numero ya esta vendido");
            }
            else
            {
                Console.WriteLine("El numero esta disponible");
            }


        }
    }
}

// 6

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
            int contador = 0, acumulador = 0, acumuladorDos = 0;
            int[] sucursal1 = { 0,1,2,3,4 };
            int[] sucursal2 = { 0, 1, 2, 3, 4 };                   
            for (int i = 0; i < sucursal1.Length; i++)
            {
                Console.WriteLine("Ventas de Sucursal, dia 1" + (contador + 1));
                sucursal1[contador] = int.Parse(Console.ReadLine());
                Console.WriteLine("Ventas de Sucursal 2, dia " + (contador + 1));
                sucursal2[contador] = int.Parse(Console.ReadLine());
                acumulador += sucursal1[contador];
                acumuladorDos += sucursal2[contador];
                if(sucursal1[contador] > sucursal2[contador])
                {
                    Console.WriteLine("La sucursal 1 vendio mas hoy.");
                }
                else
                {
                    Console.WriteLine("La sucursal 2 vendio mas hoy.");
                }
                contador += 1;
            }
            if(acumulador > acumuladorDos)
            {
                Console.WriteLine("La SUCURSAL 1 recaudo MAS en la semana: "+acumulador);
            }
            else
            {
                Console.WriteLine("La SUCURSAL 2 recaudo MAS en la semana: " + acumuladorDos);
            }

        }
    }
}

// 7 

