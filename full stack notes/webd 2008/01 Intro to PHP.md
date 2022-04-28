---
class: webd 2008
module: module one
date: 2022-01-09
tags: webd-2008, web-development, php, pdo, term-2
---
# Intro to PHP

**PHP**

- Invented by Rasmus Lerdorf in 1994, originally called Personal Home Page but now PHP Hypertext Processor
- PHP is a server side programming language: completely run on a web server
- Common component of all AMP stacks
    - Apache, MySQL, and PHP are AMP stacks
    - LAMP: Linux AMP
    - WAMP: Windows AMP
    - We will use XAMPP: comes with an installer

**Syntax**

- **[php.net](http://php.net) has all of the resources you need RE: functions**
- Begins with <? php | ends with ?>
- Declare a variable with a $ in front
- **Constants:** define(”NAME”, value);
- Putting a variable into a string: {$variable}
- Concatenate with . instead of +
- Finding the number of characters in a string: **strlen**($stringvariable)

**Arrays**

- Converting a string to an array:
    - **explode();**
    - parametres: delimiter, stringvariable
        - ex: explode(”,”, $numbers);
        - the comma is the delimiter and $numbers is the string variable
- print_r(array); will show the contents of the array with the corresponding numbers
    - Array ( [0] => 4 [1] => 8 [2] => 15 [3] => 16 [4] => 23 [5] => 42 )
- **Loop to print out arrays:** foreach($array_variable as $array_value){ echo “Now press {$array_value}”}
    - For every iteration of the loop, it stores an array value into the second variable.

**Functions**

- Writing a function is the same as Javascript
    - ***function*** say_good_day($name){
    **echo** "<p>A fine day indeed, {$name}!";
    }
    - call the function like any other: **say_good_day(”Tiana”);**
    - this function will print the string: “A fine day indeed, Tiana!”

**Hashes - Associative Arrays**

- Instead of using integers, we use strings: keys in JSON
- $actors = ['Patrick Stuart' => 'Jean-Luc Picard',
'Kate Mulgrew' => 'Katheryn Janeway',
'William Shatner' => 'James Kirk'];
    - echo “The best Star Trek captain was {$actors[’Patrick Stewart’]}.”
    - Patrick Stewart will call Jean-Luc Picard and so on

**Traversing Hashes**

- **foreach($actors as $actor => $captain)**{
echo "<p>{$actor} played the role of Captain {$captain}.</p>";
}
    - using a for each loop, you can access the keys and values
    - in this instance, keys and values are stored in other variables: keys as $actor and values as $captain

**Array of Hashes**

- Hashes can be stored inside an array
    - **$employees** = [
                             ['name' => 'Jyn Erso',
                              'position' => 'Rebel scum'],
                             ['name' => 'Tiana',
                              'position' => 'Student scum']
    ];
        - In this array, there are two hashes with two keys and two values each
    - **echo "<p>{$employees[1]['name']} is {$employees[1]['position']}</p>”**
    - This will access array index 1 and the keys and values associated with it
- Using a foreach loop, you can print out each value in the hash
    - **foreach($employees as $employee){**
    echo "<p>{$employee['name']} is {$employee['position']}.</p>";
    **}**

**Embedding HTML with PHP**

- Within the HTML, you must use *Alternative Syntax*
- Using a foreach loop to create an ordered list:
    - Code the array at the top of the HTML markup with a php statement
    - Within the markup, use Alternative Syntax to insert the php
    - <ol>
    **<?php foreach($animals as $animal): ?>**
    <li>**<?= $animal ?>**</li> 
    **<?php endforeach ?>**
    </ol>
        - This code creates an ordered list and populates the list items using the php array
        - *Alternative Syntax* used here: colon instead of curly braces, **?=** for a short echo statement, **endforeach** to close the loop
- Can have separate php files for common code encapsulation: header, footer, etc