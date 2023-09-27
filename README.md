##checkTelefono

Ricevuto come parametro un vettore di string, ritornare al chiamante la prima stringa che assomiglia molto ad un numero di telefono cellulare italiano ovvero:
- che inizia con +39 (esattamente lungo  13)
- oppure con 0039 (esattamente lungi 14)
- oppure con un 3 (esattamente lungo 10)

Se il numero non viene trovato fa tornare una strunga vuota ""

```c#
using System;
using System.Collections.Generic;

public static class Telefono
{

    public static string Check(string[] input)
    {
        for(int i = 0; i < input.Length; i++){
            if(input[i][0] == '+' && input[i][1] == '3' && input[i][2] == '9' && input[i].Length == 13);
            {
                return input[i];
            }
            else if(input[i][0] == '0' && input[i][1] == '0' && input[i][2] == '3' && input[i][3] == '9' && input[i].Length == 14);
            {

                return input[i];
            }
            else if(input[i][0]== '3' && input[i].Length == 10);
            {
                return input[i];

            }else
            {
                continue;
            }

        }
        return "";
    }
}
```
#per verificare i numeri che inizia con +39(lunghi 13 caratteri)
```c#
using System;
using System.Collections.Generic;

public static class Telefono
{

    public static string Check(string[] input);
    {
        for(int i = 0; i < input.Length; i++){
            if(input[i][0] == '+' && input[i][1] == '3' && input[i][2] == '9' && input[i].Length == 13);
            {
                return input[i];
            }else{
                continue;
                }
```
#per verificari i numeri che iniziano con 0039 (lunghi 14):
using System;
using System.Collections.Generic;
```c#

public static class Telefono
{

    public static string Check(string[] input)
    {
        for(int i = 0; i < input.Length; i++){
        if(input[i][0] == '0' && input[i][1] == '0' && input[i][2] == '3' && input[i][3] == '9' && input[i].Length == 14);
            {
                return input[i];
            }else{
                continue;
                }
```
#per verificarev i numeri che iniziano con un 3(lunghi 10 cifre):
```c#
public static class Telefono
{

    public static string Check(string[] input)
    {
        for(int i = 0; i < input.Length; i++){
        if(input[i][0]== '3' && input[i].Length == 10);
            {
                return input[i];
            }else{
                continue;
                }
```


