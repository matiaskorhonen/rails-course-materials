!SLIDE cover

# <span style="font-family:'Bitstream Vera Serif', serif;font-size:80%"><span style="color:#a40800">Ruby on Rails</span> Course <span style="color:#8B8B8B">2009</span></span>
## Ruby: Conditionals and Flow Control

!SLIDE if

# if, elsif, else

@@@ ruby
	a = 3
	if a == 4
	  a = 7
	elsif a < 0
	  a = 0
	else
	  a = 5
	end
	print a # => 5
@@@

!SLIDE shortif

# Short if

When you need a single if statement and the block has only one line of code.

@@@ ruby
	a = 5
	a = 7 if a == 4
	print a # => 5
@@@

!SLIDE unless

# Unless

* The **opposite of if** (executed when false)
* More expressive than an if statement with a negated variable

@@@ ruby
	my_city = "Helsinki"
	unless my_city == "Helsinki"
	  print "I don't live in Helsinki"
	end
@@@

or 

@@@ ruby
	my_city = "Helsinki"
	print "I don't live in Helsinki" unless my_city == "Helsinki"
@@@

!SLIDE case

# Case

@@@ ruby
	case n
	  when 0 
	    puts 'You typed zero'
	  when 1, 9 
	    puts 'n is a perfect square'
	  when 2 
	    puts 'n is a prime number'
	    puts 'n is an even number'
	  when 3, 5, 7 
	    puts 'n is a prime number'
	  when 4, 6, 8 
	    puts 'n is an even number'
	  else              
	    puts 'Only single-digit numbers are allowed'
	end
@@@

!SLIDE ternary

# Ternary operator

Instead of:

@@@ ruby
	customer = "Bob"
	if customer == "Bob"
	  puts "Hello Bob!"
	else
	  puts "You're not Bob!"
	end
@@@

You can have:

@@@ ruby
	customer = "Bob"
	puts customer == "Bob" ? "Hello Bob!" : "You're not Bob!"
@@@

!SLIDE while

# While

@@@ ruby
	while <expression>
	  <...code block...>
	end
@@@

The code block will be executed again and again, as long as the expression evaluates to **true**.

!SLIDE until

# Until

Unlike the while statement, the code block for the until loop will execute as long as the expression evaluates to false.

@@@ ruby
	until <expression>
	  <...code block...>
	end
@@@

!SLIDE for

# For

@@@ ruby
	for article in articles do
	  puts article.title
	end
@@@

!SLIDE times

# Times

@@@ ruby
	# Display 'Hello' 10 times
	10.times do
	  puts "Hello"
	end

	# Display powers of two
	10.times do |i|
	  puts 2**i
	end
@@@

!SLIDE return

# Return

Causes the method in which it appears to exit at that point and return the value specified. Just calling return without supplying an argument will return nil.
