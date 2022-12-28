# `advancedCalculator`

Write a program called advanced_calculator. It should have a main loop that receives data from the user and displays the result, for example, for `5 % 3` it should return the result `2`. All calculator commands should be stored in a map that uses a char key to refer to a specific command (e.g. `+` -> add, `%` -> modulo) and a `std::function<>` value that is a wrapper for lambda expressions that perform a specific calculation.

The program should also return the appropriate error code if the user provides incorrect data, such as dividing by `0` or trying to add `ala + 5`.

* Input: `5 + 5` -> operation of adding two numbers `5` and `5` -> output: `10`.
* Input: `5 ^ 2` -> power operation -> output `25`.
* Input: `125 $ 3` -> cube root operation (sqrt is too long), cube root of `125` -> output: `5`.

___

### Calculator Functions

* Addition, multiplication, division, subtraction (`+`, `*`, `/`, `-`)
* Modulo (`%`)
* Calculating factorial (`!`)
* Raising a number to a power (`^`)
*Calculating square root (`$`)

___

### Error code

* `Ok`
* `BadCharacter` - Char different than number
* `BadFormat` - Bad command format -> eg. `+5 4`, should be `5 + 4`
* `DivideBy0` - Divide by `0`
* `SqrtOfNegativeNumber` - Square root of a negative number
* `ModuleOfNonIntegerValue` - Attempting to calculate `%` on a non-integer

___

### Function, that will be tested

```cpp
ErrorCode process(std::string input, double* out)
```

* The function should receive data from the user and perform the correct calculation
* If the data is correct, it should return `ErrorCode:Ok` and save the output in a variable called `out`
* If any errors occur, the function should return the error and not save anything in `out`

___
