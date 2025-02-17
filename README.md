# Incorrect Usage of $inc Operator in MongoDB
This example demonstrates an uncommon error in MongoDB update operations, specifically involving the $inc operator. The $inc operator is used to increment or decrement a numeric field by a specified value. A common mistake is to provide a string value instead of a numeric value to the $inc operator.  This will likely result in an error or unexpected results.

## Bug Description:
Incorrectly using a string value ('1') instead of a number (1) in the `$inc` operation causes the update to fail, or potentially modify the field in an unexpected manner.  MongoDB expects numerical increments.

## Bug Solution:
The solution is to ensure the value provided to the `$inc` operator is always a numeric type (integer or double).