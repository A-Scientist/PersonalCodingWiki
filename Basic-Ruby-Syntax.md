[\<\-Back](http://euclid.nmu.edu:3000/ovoisine/CS326/wiki/Ruby)

# Basic Ruby Syntax
Ruby is newline terminated language with no indentation requirements, although they should be used to comply with best practice and readability. Whitespace or brackets can be used to separate syntax pieces. For example, `puts ("hello")` is the same as `puts "hello"`<br>

## Fundamental Structures
Ruby is an dynamically typed language. Type does not need to be given when declaring.<br>
`__ = ___` or variable name = value<br>
Variable types can be forced by including a type (with capitalized first letter) in front of brackets holding the variable in question.<br>
`Integer(age)`

To pint a message to the terminal.<br>
`puts ___`<br>

Variables can be inserted into a string by use of the `#{}` structure.<br>
`greeting = "Hello #{name}, how are you?"`<br>

Comments are tagged using a hash and can be inserted after working code withing the same line.<br>
`puts "How are you?" # asks question`<br>
Multi line comments are defined by using the \= sign in front of the keywords `begin` and `end`.<br>
```
puts "hello"
=begin
comment
another comment
=end
puts "good bye"
``` 
    
## Blocks, Ruby's Container
A container is defined by use of curly brackets `{ }` as used for single line and code blocks with an starting syntax of `begin` and an ending syntax of `end` used for multi-lines. This container in Ruby is known as a code block. All blocks described below have what is essentially an invisible, implicit `begin`, although there are reasons why you would want to declare a `begin` explicitly as described below.<br>
Due to this, assume all blocks described below include are initialized as described, then have lines of code that are executed next and are indented for good practice, and then are closed with the `end` keyword on the same level as the initializing keyword.<br>
For example<br>
```
begin
	puts "Hello World!"
end
```
<br>

**\_\_\_ do |\_\_\_|**<br>
The `do` structure can be thought of like an opening curly bracket in a more readable form. A `do` can be used on its own, although it doesn't do anything significant in this form besides ensure that the code runs inside a block just like `begin`. When it is preceded by something like `anArray.each` or `aNumber.times` it will run that code like a foreach or for loop respectively would in others languages. There are other ways to use do as well. Any following arguments given are wrapped in vertical bars sometimes known as pipes, `|`. Here is an example of a simple but fully utilized do block.<br>
```
['a','b','c'].each do |letter|
	puts letter
end
```
<br>

**if \_\_\_ then**<br>
While the conditional evaluates to true, the following code block will be executed.<br>

**while \_\_\_**<br>
While the conditional evaluates to true, the following code block will execute and then loop back to the top until the condition is no longer true.<br>
While inside a loop, the `break` keyword can be used to exit the loop immediately.<br>

**def \_\_(\_\_\_,)**<br>
Defines a block of code that can be referenced by name and be given arguments. The value that is returned from this block can be set using `return \_\_\_`, but if not explicitly set, will be the last value referenced by the block. Therefore, putting `return varableName` before your code block ends is the same as just putting `varableName` before your code block ends. Return can still be used to exit a code block early.<br>

**rescue**<br>
The `rescue` keyword can be used as part of a block in the case where it may not be possible for the code to perform such an action in order to prevent code outside the block from crashing and instead use a different action. Single line and multi-line applications shown below. For example, in the case where name cannot be converted into an int, size will be set to 0 instead.<br>
`size = Integer(name) rescue size = 0`<br>
```
begin
	size = Integer(name)
rescue
	size = 0
end
```
<br>

**ensure**<br>
The `ensure` can be used as part of a block in the case where, regardless if other code inside the block failed or not, lines included after an `ensure` will always run. Single line use cases exist, but will be more useful in multi-line blocks as shown below. For example, regardless whether name can or cannot be converted into an int, size will be set to 0 afterwards.<br>
```
begin
	size = Integer(name)
ensure
	size = 0
end
```






