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
	
* 4. Repetition Token #3 (4-repetition_token_3.rb)
	* Find the regular expression that will match the above cases
	* Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method
	* Your regex should not contain square brackets
	
* 5. Not quite HBTN yet (5-beginning_and_end.rb)
	* The regular expression must be exactly matching a string that starts with h ends with n and can have any single character in between
	* Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method
```
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x06-regular_expressions$ ./5-beginning_and_end.rb 'hn' | cat -e
$
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x06-regular_expressions$ ./5-beginning_and_end.rb 'hbn' | cat -e
hbn$
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x06-regular_expressions$ ./5-beginning_and_end.rb 'hbtn' | cat -e
$
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x06-regular_expressions$ ./5-beginning_and_end.rb 'h8n' | cat -e
h8n$
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x06-regular_expressions$ ./5-beginning_and_end.rb 'haaaaaan' | cat -e
$
```
	* Only works when it starts with 'h', ends in 'n' and has exactly one char in between.

* 6. Call me maybe (6-phone_number.rb)
	* The regular expression must match a 10 digit phone number
```
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x06-regular_expressions$  ./6-phone_number.rb 4155049898 | cat -e
4155049898$
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x06-regular_expressions$  ./6-phone_number.rb " 4155049898" | cat -e
$
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x06-regular_expressions$ ./6-phone_number.rb "415 504 9898" | cat -e
$
```
