# checkTelefono

Ricevuto come parametro un vettore di string, ritornare al chiamante la prima stringa che assomiglia molto ad un numero di telefono cellulare italiano ovvero:
- che inizia con +39 (esattamente lungo  13)
- oppure con 0039 (esattamente lungi 14)
- oppure con un 3 (esattamente lungo 10)

Se il numero non viene trovato fa tornare una strunga vuota ""



```c#


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

            }else{
                continue;
            }

        }
        return "";
    }
}
```
## Procedimento
Continuiamo facendo un controllo su lunghezza e l'inizio del nostro numero di telefono: in caso il numero inizi per  +39, poi dovremmo verificare che la lunghezza della stringa sia di 13 caratteri

```c#
    for(int i = 0; i < input.Length; i++){
}
```

Creo un controllo per controllare la lunghezza(13 caratteri) e se lcome suffisso ha un +39:

```c#
for(int i = 0; i < input.Length; i++){
            if(input[i][0] == '+' && input[i][1] == '3' && input[i][2] == '9' && input[i].Length == 13);
            {
                return input[i];
            }
```

Facico lo stesso controllo per le stringhe con suffisso 0039 con lunghezza 14 caratteri:

```c
if(input[i][0] == '0' && input[i][1] == '0' && input[i][2] == '3' && input[i][3] == '9' && input[i].Length == 14);
            {

                return input[i];
            }

```

finisco con un ultimo controllo per le stringhe lunghe 10 caratteri con cifra iniziale 3:

```c#
    if(input[i][0]== '3' && input[i].Length == 10);
            {
                return input[i];

            }
```


<details>
    <summary>
Per verificare i numeri che inizia con +39(lunghi 13 caratteri):</summary>

```c#



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
</details>

<details>
    <summary>
    Per verificari i numeri che iniziano con 0039 (lunghi 14):</summary>
    
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
</details>


<details>
    <summary>
    Per verificarev i numeri che iniziano con un 3(lunghi 10 cifre):</summary>
    
```c#
    

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
</details>


