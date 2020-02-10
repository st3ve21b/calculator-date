# calculator-date
            //primera fecha
            int año11 = fecha11.Year;
            int mes11 = fecha11.Month;
            int dia11 = fecha11.Day;

            //segunda fecha
            int año22 = fecha22.Year;
            int mes22 = fecha22.Month;
            int dia22 = fecha22.Day;

            int bisiesto11 = 0;
            int bisiesto22 = 0;

            //inicializacion de dias del mes.
            int enero1 = 31, febrero1 = 0,febrero2=0, marzo1 = 31, abril1 = 30,mayo1 = 31, junio1 = 30, julio1 = 31, agosto1 =              31, septiembre1 = 30, octubre1 = 31, noviembre1 = 30, diciembre1 = 31;

            /////primera fecha//////////////
            int bisi11 = (año11 / 4);//cantidad de años bisiestos
            int normal11 = año11 - bisi11;//restamos los años bisiestos el año ingresado, separando los dos tipos de años
            int diasaños11 = (bisi11 * 366) + (normal11*365);//total de dias que hay en ese año

            /////segunda fecha//////////////
            int bisi22 = (año22 / 4);//cantidad de años bisiestos
            int normal22 = año22 - bisi22;//restamos los años bisiestos el año ingresado, separando los dos tipos de años
            int diasaños22 = (bisi22 * 366) + (normal22 * 365);//total de dias que hay en ese año

            int diasmes11 = año11 % 4;
            int diasmes22 = año22 % 4;

            int j = 0;
            int i = 0;

            int x = 0;
            int y = 0;

            /////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
            if (diasmes11 == 0)
            {
                febrero1 = 29;
                j = 366;
            }
            if (diasmes11 != 0)
            {
                febrero1 = 28;
                j = 365;
            }

            if (mes11 == 1) i = i + enero1;
            if (mes11 == 2) i = i + enero1+febrero1;
            if (mes11 == 3) i = i + enero1 + febrero1+marzo1;
            if (mes11 == 4) i = i + enero1 + febrero1 + marzo1+abril1;
            if (mes11 == 5) i = i + enero1 + febrero1 + marzo1 + abril1+mayo1;
            if (mes11 == 6) i = i + enero1 + febrero1 + marzo1 + abril1 + mayo1+junio1;
            if (mes11 == 7) i = i + enero1 + febrero1 + marzo1 + abril1 + mayo1 + junio1+julio1;
            if (mes11 == 8) i = i + enero1 + febrero1 + marzo1 + abril1 + mayo1 + junio1 + julio1+agosto1;
            if (mes11 == 9) i = i + enero1 + febrero1 + marzo1 + abril1 + mayo1 + junio1 + julio1 + agosto1+septiembre1;
            if (mes11 == 10) i = i + enero1 + febrero1 + marzo1 + abril1 + mayo1 + junio1 + julio1 + agosto1 + septiembre1+octubre1;
            if (mes11 == 11) i = i + enero1 + febrero1 + marzo1 + abril1 + mayo1 + junio1 + julio1 + agosto1 + septiembre1 + octubre1+noviembre1;
            if (mes11 == 12) i = i + enero1 + febrero1 + marzo1 + abril1 + mayo1 + junio1 + julio1 + agosto1 + septiembre1 + octubre1 + noviembre1 + diciembre1;

            int diasdelaño = j - (i - dia11);
            int totaldias1 = diasaños11 - diasdelaño;//dias completos de la fecha 1

           //////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

            if (diasmes22 == 0)
            {
                febrero2 = 29;
                x = 366;
            }
            if (diasmes22 != 0)
            {
                febrero2 = 28;
                x = 365;
            }

            if (mes22 == 1) y = y + enero1;
            if (mes22 == 2) y = y + enero1 + febrero2;
            if (mes22 == 3) y = y + enero1 + febrero2 + marzo1;
            if (mes22 == 4) y = y + enero1 + febrero2 + marzo1 + abril1;
            if (mes22 == 5) y = y + enero1 + febrero2 + marzo1 + abril1 + mayo1;
            if (mes22 == 6) y = y + enero1 + febrero2 + marzo1 + abril1 + mayo1 + junio1;
            if (mes22 == 7) y = y + enero1 + febrero2 + marzo1 + abril1 + mayo1 + junio1 + julio1;
            if (mes22 == 8) y = y + enero1 + febrero2 + marzo1 + abril1 + mayo1 + junio1 + julio1 + agosto1;
            if (mes22 == 9) y = y + enero1 + febrero2 + marzo1 + abril1 + mayo1 + junio1 + julio1 + agosto1 + septiembre1;
            if (mes22 == 10) y =y + enero1 + febrero2 + marzo1 + abril1 + mayo1 + junio1 + julio1 + agosto1 + septiembre1 + octubre1;
            if (mes22 == 11) y = y + enero1 + febrero2 + marzo1 + abril1 + mayo1 + junio1 + julio1 + agosto1 + septiembre1 + octubre1 + noviembre1;
            if (mes22 == 12) y = y + enero1 + febrero2 + marzo1 + abril1 + mayo1 + junio1 + julio1 + agosto1 + septiembre1 + octubre1 + noviembre1 + diciembre1;

            int diasdelaño2 = x - (y - dia22);
            int totaldias2 = diasaños22 - diasdelaño2;//dias completos de la fecha 2

            int resultado = totaldias2 - totaldias1;

            impresionresultado.Text = resultado.ToString();
            impresion1.Text = totaldias1.ToString();
            impresion2.Text = totaldias2.ToString();
        }
    }
}


