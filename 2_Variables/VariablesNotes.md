# Variables

Generally, a *variable* is a name chosen by a programmer to represent a value
The name can be referred to as a *data name*. It can be anything, as long as it is:

1. Under 30 characters long
2. Does not content any spaces
3. It is made by only letter, digits and/or hashes
4. It is NOT a reserved word

Examples of good variable name can be `balance`, `inventory12345` or `northAmericanSalesIn2020-FINAL` (that's exactly 30 characters)
Examples of naes that are not good, are `top5%*`or `phone number`

While we create a variable, we also have to consider what type of data we are going to store in it because we need
to declare it at the variable's creation. We also have to let `COBOL` know how many letters or numbers we are going
to be using. All this is necessary because `COBOL` is a very efficient programming language and for it to continue
working efficiently, it needs to know all this information about the data it is going to use right from the beginning.
We set this up in the **Picture clause** or simply `PIC` for short. It sets the length and the data type of the variable
we are declaring. An example can be *PIC 9*. Here, we declare a **numeric** variable with length **one**, because no legth was
actually specified. 9 does not mean legth of 9 but it just means that the variable will be a numeric one. For specified length,
we can write `PIC 9(4)`. This means that we are specifying a variable of numeric type and length of 4.

`PIC A` means that we will have a simple alphabetic character (again, no length specified, hence the length is 1).
`PIC X(8)` gives us 8 alphanumeric characters. *X* means alphanumeric and the 8 represents the length.
The maximun length of a numeric variable is 18 and an alphabetic one can be up to 255.

There are many more picture clauses but for now we are going to use these and get to know the others when we need them.

Picture clauses can be used to represent symbols in a value. For example, `PIC 9(4)V99` means that we are going to have
four digits, then a decimal part of two digits. Example: 1547.36. `V` represents the decimal position.

We can also do something like `PIC $9,999V99`, which means that we can represent $1,6987.85. The dollar sign and comma carry
through and the `V` represents the decimal area. 

When we think 'variable', we think of something that changes. `COBOL` also has variables that they cannot change, named
**Literals**. We make literals for things that we are going to use on many parts of our program but we do not want them
to change. 

`COBOL` has its own literals out of the box that can be used when needed. Some examples are:
1. ZERO / ZEROES
2. SPACE / SPACES
3. LOW-VALUE
4. HIGH-VALUE
5. NULL / NULLS

Notice that for some of these there is both plural and singular.