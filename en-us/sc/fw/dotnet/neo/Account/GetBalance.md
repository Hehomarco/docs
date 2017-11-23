# Account.GetBalance Method (byte[])

Obtain the balance of specified assets in the account through the asset ID.
Erhalte den Wert eines angegebenen Vermögenswert in einem Account anhand der Asset ID.
 
Namespace: [Neo.SmartContract.Framework.Services.Neo](../../neo.md)

Assembly: Neo.SmartContract.Framework

## Syntax

```c#
public extern long GetBalance (byte[] asset_id)
```

Parameter: Asset ID, die Transaktions ID des RegisterTransaction wenn der Vermögenswert registriert wurde. Die Transaktions ID besteht aus einem 32 langen Byte Arry.

Zurückgegebener Wert: Der Wert eines Vermögenswertes ist so lange wie der aktuelle Wert multipliziert mit 100,000,000.

## Beispiel

```c#
public class Contract1: FunctionCode
{
    public static void Main()
    {
        byte[] scriptHash = {36, 23, 241, 177, 228, 54, 109, 223, 27, 237, 139, 54, 207, 38, 132, 101, 172, 3, 10, 73};
        Account account = Blockchain.GetAccount(scriptHash);
        // Take NEO shares as an example
        byte[] asset = {197, 111, 51, 252, 110, 207, 205, 12, 34, 92, 74, 179, 86, 254, 229, 147, 144, 175, 133, 96, 190, 147, 15, 174, 190, 116, 166, 218, 255, 124, 155};
        long balance = account.GetBalance(asset);
    }
}
```



[Back](../Account.md)
