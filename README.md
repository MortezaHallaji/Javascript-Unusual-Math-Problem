# Javascript-Unusual-Math-Problem(solved)

I solved bug javascript to calculate unusual numbers

## Minus

```javascript
function safe_minus(number1, number2) {
  let num_digit1 = number1.toString();
  num_digit1 = num_digit1.split(".");
  let num_digit2 = number2.toString();
  num_digit2 = num_digit2.split(".");
  let digit_after_ziro1 = typeof num_digit1[1] == "undefined" ? 0 : num_digit1[1].length;
  let digit_after_ziro2 = typeof num_digit2[1] == "undefined" ? 0 : num_digit2[1].length;
  let digit_multy = Math.max(digit_after_ziro1, digit_after_ziro2);
  digit_multy = Math.pow(10, digit_multy);
  return (number1 * digit_multy - number2 * digit_multy) / digit_multy;
}
```

##### Calculate normaly by javascript
```javascript

0.2 - 0.00057
# returns '0.19943000000000002'
```

##### Calculate by safe_minus function
```javascript

0.2 - 0.00057
# returns '0.19943'
```


## Plus

```javascript
function safe_plus(number1, number2) {
  let num_digit1 = number1.toString();
  num_digit1 = num_digit1.split(".");
  let num_digit2 = number2.toString();
  num_digit2 = num_digit2.split(".");
  let digit_after_ziro1 = typeof num_digit1[1] == "undefined" ? 0 : num_digit1[1].length;
  let digit_after_ziro2 = typeof num_digit2[1] == "undefined" ? 0 : num_digit2[1].length;
  let digit_multy = Math.max(digit_after_ziro1, digit_after_ziro2);
  digit_multy = Math.pow(10, digit_multy);
  return (number1 * digit_multy + number2 * digit_multy) / digit_multy;
}
```

##### I hope you enjoy it
