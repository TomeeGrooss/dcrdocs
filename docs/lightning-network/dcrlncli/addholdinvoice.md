`dcrlncli addholdinvoice` - Add a new hold invoice.

### Usage
```
   dcrlncli addholdinvoice [command options] hash [amt]
```

### Description
   
  Add a new invoice, expressing intent for a future payment.

  Invoices without an amount can be created by not supplying any
  parameters or providing an amount of 0. These invoices allow the payee
  to specify the amount of atoms they wish to send.

### Options
|Option|Info|
|--|--|
|`--memo value`|              A description of the payment to attach along with the invoice (default="")|
|`--amt value`|               The amt of atoms in this invoice (default: 0)|
|`--description_hash value`|  SHA-256 hash of the description of the payment. Used if the purpose of payment cannot naturally fit within the memo. If provided this will be used instead of the description(memo) field in the encoded invoice.|
|`--fallback_addr value`|     Fallback on-chain address that can be used in case the lightning payment fails|
|`--expiry value`|            The invoice's expiry time in seconds. If not specified, an expiry of 3600 seconds (1 hour) is implied. (default: 0)|
|`--private`|                 Encode routing hints in the invoice with private channels in order to assist the payer in reaching you|
   
