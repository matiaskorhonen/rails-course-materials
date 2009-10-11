!SLIDE cover

# <span style="font-family:'Bitstream Vera Serif', serif;font-size:80%"><span style="color:#a40800">Ruby on Rails</span> Course <span style="color:#8B8B8B">2009</span></span>
## Ruby: Methods

!SLIDE calls

Normal method call:
@@@ ruby
	method_name(parameter1, parameter2)
@@@

Sometimes there is no need for parentheses:
@@@ ruby
	method_name
	results = method_name parameter1, parameter2
@@@

And sometimes you really need them:
@@@ ruby
	results = method_name(parameter1, parameter2).reverse
@@@

!SLIDE definitions

# Defining a method

@@@ ruby
	def output_something(value)
		puts value
	end
@@@

!SLIDE return

# Return values

Methods return the value of the last statement executed. The following code returns the value **x+y**.

@@@ ruby
	def sum(x, y)
		x + y
	end
@@@

!SLIDE explicit

# Explicit return

An explicit return statement can also be used to return from a function, if necessary:

@@@ ruby
	def authenticate(username)
		return unless username == "bob"
		puts "Welcome, Bob!"
	end
@@@

!SLIDE default

# Default values

Default parameter values are used when the parameter is not specified, or is nil.

@@@ ruby
	def greet(username="anonymous")
		puts "Hello " + username + "!"
	end
@@@