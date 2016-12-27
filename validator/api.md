
#Validators

####one(pred, fail, required)
The one validator expects a predicate condition as well as a failure message or function.  It can also take in a required string to identify if the validator is required.

####all([])
The all validator allows you to have multiple validators for a given property.  It expects an array of one type validators.  This function curries its arguments.


#Validation types

####required(target, fail)
Ensures that the property exists.

####eq(target, fail)
Ensures that the property value is equal to the target.

####min(target, fail)
Ensures that the property value is greater than the target.

####max(target, fail)
Ensures that the property value is less than the target.

####eqLen(target, fail)
Ensures that the property value length is equal to the target.

####minLen(target, fail)
Ensures that the property value length is greater than the target.

####maxLen(target, fail)
Ensures that the property value length is less than the target.

####within(target, fail)
Ensures that the property value is contained within the target array values.

####regex(target, fail)
Ensures that the property value satisfies the regular expression represented in the target.

####isNotNil(target, fail)
Ensures that the property value is not `null` or `undefined`.

####isNotEmpty(target, fail)
Ensures that the property value does not represent the type's empty value. 

####isNumber(target, fail)
Ensures that the property value is a Number.

####isString(target, fail)
Ensures that the property value is a String.

####isObject(target, fail)
Ensures that the property value is an Object.

####isFunction(target, fail)
Ensures that the property value is a Function.

####phone(target, fail)
Ensures that the property value is valid phone number.

####email(target, fail)
Ensure that the property value is a valid email address.

####url(target, fail)
Ensures that the property value is a valid url address.

