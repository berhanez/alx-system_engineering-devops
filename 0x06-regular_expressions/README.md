# 0x06. Regular expression

## Introduction

* A regular expression, commonly called a “regexp”, is a sequence of characters that define a search pattern.  It is mainly for use in pattern matching with strings, or string matching (i.e. it operates like a “find and replace” command). While it is a very powerful tool, it is also very dangerous because of its complexity.

## Project Background Context

* For this project, you have to build your regular expression using Oniguruma, a regular expression library that which is used by Ruby by default. Note that other regular expression libraries sometimes have different properties.

* USE: Replace the regexp part in between //
``` 
#!/usr/bin/env ruby
puts ARGV[0].scan(/127.0.0.[0-9]/).join 
```
Whatever is put in beterrn '//' is chars to match. The Find in Find and Replace.

## REUIREMENTS

* Install Ruby  ``` sudo apt install ruby```

## TASKS

* 0.  Simply matching School (0-simply_match_school.rb)
```
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x06-regular_expressions$ ./0-simply_match_school.rb School | cat -e
School$
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x06-regular_expressions$ ./0-simply_match_school.rb "Best School" | cat -e
School$
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x06-regular_expressions$  ./0-simply_match_school.rb "School Best School" | cat -e
SchoolSchool$
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x06-regular_expressions$ ./0-simply_match_school.rb "Grace Hopper" | cat -e
$
```

* 1. Repetition Token #0
	* Find the regular expression that will match the above cases
	* Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

* 2. Repetition Token #1 (2-repetition_token_1.rb)
	* Find the regular expression that will match the above cases
	* Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method
	
* 3. Repetition Token #2 (3-repetition_token_2.rb)
	* Find the regular expression that will match the above cases
	* Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method
	
