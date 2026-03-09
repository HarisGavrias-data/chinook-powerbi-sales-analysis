# DAX Measures

## Revenue

revenue =
SUMX(
    'chinook invoiceline',
    'chinook invoiceline'[UnitPrice] * 'chinook invoiceline'[Quantity]
)

## Total Tracks Sold

Total Tracks Sold =
SUM('chinook invoiceline'[Quantity])

## Total Customers

total customers =
DISTINCTCOUNT('chinook invoice'[CustomerId])
