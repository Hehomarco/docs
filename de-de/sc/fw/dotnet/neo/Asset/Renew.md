# Asset.Renew Method (byte[])

Für die Erneuerung von Assets. 

Diese Methode ist neu in Version 2.0, nach der registrierung muss man für das Asset eine Jähliche Gebühr bezhalen. Falls diese Gebühr nicht bezhalt wird wird das Asset in den frozen state versetzt.

Wenn das Asset abgelaufen ist ist es notwendig das Asset zu erneuern. Wenn das Asset sich nicht im Zustand frozen befindet und erneuert wird wird das Datum ab dem Ablaufdatum ereuert. Wenn sich das Asset im Zustand frozen befindet wird eine Erneuerung ab dem Datum des bezahlens durchgeführt. Sodass es keinen Verzug beim erneuern geben kann.

Namensraum: [Neo.SmartContract.Framework.Services.Neo](../../neo.md)

Assembly: Neo.SmartContract.Framework

## Syntax

```c#
public extern uint Renew (byte years)
```

Paratmeter: Erneuerungszeitraum, ein Jahr ist gleich 2,000,000 Blocks, Byte Type.

Rückgabewert: Die Höhe der Blocks bis wohin das Asset benutzt werden kann nachdem es erneuert wurde.

## Example

```c#
public class Contract1: FunctionCode
{
    public static void Main()
    {
        // Taking NEO shares as an example
        byte[] asset = {197, 111, 51, 252, 110, 207, 205, 12, 34, 92, 74, 179, 86, 254, 229, 147, 144, 175, 133, 96, 190, 147, 15, 174, 190, 116, 166, 218, 255, 124, 155};
        Asset ass = Blockchain.GetAsset(asset);
        Uint blockIndex = ass.Renew (1);
    }
}
```



[Back](../Asset.md)