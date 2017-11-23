# Blockchain.GetBlock Methode (uint)

Returns a block from the blockchain given a block height.
Gibt ein Block auf der Blockchain anhand der Block height zurück.

Namensraum: [Neo.SmartContract.Framework.Services.Neo](../../neo.md)

Assembly: Neo.SmartContract.Framework

## Syntax

```c#
public static extern Neo.SmartContract.Framework.Services.Neo.Block GetBlock(uint height)
```

Parameter: Block Height (block index) als einen Unsigned Integer.

Rückgabewert: [Block](../Block.md).

## Beispiel

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         Block bl = Blockchain.GetBlock(997027);
     }
}
```



[Back](../Blockchain.md)