# MongoDB $inc Operator with String Value

This example demonstrates an uncommon error that can occur when using the `$inc` operator in MongoDB update queries. The `$inc` operator is used to increment a numeric field by a specified value. However, if a string value is provided instead of a number, MongoDB will not perform the increment operation correctly, potentially leading to unexpected behavior or errors.

**Bug:**
The bug lies in the incorrect usage of the `$inc` operator. The example code attempts to increment the `age` field by a string value ('1'), which is not a valid numeric value for the `$inc` operator. This will result in either a failure to increment the age or an unexpected value being assigned to the `age` field.

**Solution:**
To fix the bug, ensure that you provide a numeric value to the `$inc` operator. The corrected code should use a number (1) instead of the string ('1').