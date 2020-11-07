
/*
Fazil Basri
1908107010032
*/

public class BandingAkar
{
    public static double fa(double x)
    {
        return (x*x*x) - (3*x) + 1;
    }
    public static double faTurunan(double x)
    {
        return 3*(x*x) - 3;
    }
    public static double fb(double x)
    {
        return (x*x*x) - (2 * Math.sin(x));
    }
    public static double fbTurunan(double x)
    {
        return 3*(x*x) - (2 * Math.cos(x));
    }

    public static void main(String[] args) {
        System.out.println("\n**PENYELESAIAN A  x^3 - 3x + 1; dimana x0 = 2  \n");
        SecantA(NewtonA());

        System.out.println("\n**PENYELESAIAN B  x^3 - 2sinx ; dimana x0 = 1/2 \n");
        SecantB(NewtonB());
    }


    //penyelesaian untuk soal a

    public static double NewtonA()  // penyelesaian metode newton a
    {
        boolean i = true;
        double hasil = 0.0;
        double x = 2.0;
        double e = 0.0;
        double y1 = fa(x);
        double y2 = faTurunan(x);
        double x1;
        System.out.println("\n1.  Methode Newton Raphson \n");
        while(true) {
            x1 = x - (y1/y2);
            if(i) {
                hasil = x1;
                i = false;
            }
            y1 = fa(x1);
            y2 = faTurunan(x1);
            if(Math.abs(x-x1) == 0) {
                break;
            }
            x = x1;
            System.out.println("Akarx = " + x1 + "\t\tF(x)= " + y1 + "\n\n");
        }
        System.out.println("Akar terletak di x = " + x + "\t\tF(x)= " + y1 + "\n");
        return hasil;
    }
    public static void SecantA(double a)
    {
        double x0 = 2.0;
        double x1 = a;
        double y0 = fa(x0);
        double y1 = fa(x1);

        System.out.println("\n2.  Methode Secant \n");
        while(true) {
            double x2 = x1 - (y1  * (x1 - x0) / (y1 - y0));

            if(Math.abs(x2-x1) == 0) {
                break;
            }
            x0 = x1;
            x1 = x2;
            y0 = y1;
            y1 = fa(x1);
            System.out.println("Akarx = " + x1 + "\t\tF(x)= " + y1 + "\n\n");
        }
        System.out.println("Akar terletak di x = " + x1 + "\t\tF(x)= " + y1 + "\n");
    }


    //penyelesaian untuk soal b
    public static double NewtonB() // penyelesaian metode newton b
    {
        boolean i = true;
        double hasil = 0.0;
        double x = 0.5;
        double e = 0.0;
        double y1 = fb(x);
        double y2 = fbTurunan(x);
        double x1;
        System.out.println("\n1.  Methode Newton Raphson\n");
        while(true) {
            x1 = x - (y1/y2);

            if(i) {
                hasil = x1;
                i = false;
            }
            y1 = fb(x1);
            y2 = fbTurunan(x1);

            if(Math.abs(x-x1) == 0) {
                break;
            }
            x = x1;
            System.out.println("Akarx = " + x1 + "\t\tF(x)= " + y1 + "\n\n");
        }
        System.out.println("Akar terletak di x = " + x + "\t\tF(x)= " + y1 + "\n");
        return hasil;
    }
    public static void SecantB(double b)
    {
        double x0 = 0.5;
        double x1 = b;
        double y0 = fb(x0);
        double y1 = fb(x1);
        System.out.println("\n2.  Methode Secant \n");
        while(true) {
            double x2 = x1 - (y1  * (x1 - x0) / (y1 - y0));
            if(Math.abs(x2-x1)==0) {
                break;
            }
            x0 = x1;
            x1 = x2;
            y0 = y1;
            y1 = fb(x1);
            System.out.println("Akarx = " + x1 + "\t\tF(x)= " + y1 + "\n\n");
        }
        System.out.println("Akar terletak di x = " + x1 + "\t\tF(x)= " + y1 + "\n");
    }
}
