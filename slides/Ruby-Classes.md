!SLIDE cover

# <span style="font-family:'Bitstream Vera Serif', serif;font-size:80%"><span style="color:#a40800">Ruby on Rails</span> Course <span style="color:#8B8B8B">2009</span></span>
## Ruby: Classes

!SLIDE definition

# Class definition

@@@ ruby
	class SomeClass
		def some_method
		end
	end
@@@

!SLIDE variables

# Instance variables

@@@ ruby
	class Person
		@name = "Bob"
		
		def greet
			"Welcome " + @name + "!"
		end
		
		def change_to_fred
			@name = "Fred"
		end
	end
@@@

!SLIDE usage

# Using the previous class

@@@ ruby
	person = Person.new
	puts person.greet # => "Welcome Bob!"
	person.change_to_fred
	puts person.greet # => "Welcome Fred!"
@@@

!SLIDE instantiation

# Instantiation

* The **.initialize** method is called when a new instance is created.
* Parameters passed to **.new** will be passed to the **.initialize** method.

@@@ ruby
	class Person
		def initialize(name)
			@name = name
		end
	end
	
	person = Person.new("Joe")
@@@

!SLIDE access

# Accessing instance variables

@@@ ruby
	class Person
	  def name
	    @name
	  end

	  def name=(name)
	    @name = name
	  end
	end
@@@

!SLIDE attraccessor

# Attribute accessors

The previous example could have been written like this:

@@@ ruby
	class Person
	  attr_accessor :name
	end
@@@

!SLIDE accessors

# Available accessors

* **attr_accessor** will give you get/set functionality
* **attr_reader** will give only getter
* **attr_writer** will give only setter

!SLIDE inheritance

# Inheritance

* Methods and variables can be inherited from another class.
* No multiple inheritance!

@@@ ruby
	class Person
	  attr_accessor :name
	end

	class Employee < Person
	  attr_accessor :position
	end
@@@

!SLIDE accesscontrol

# Access control

## Default:
* **public** methods are accessible by anyone

## Others:
* **protected** methods are accessible also to child objects
* **private** methods are accessible only to the class that defines them

!SLIDE accesscontrolexamples

# Access control example

@@@ ruby
	class Person
	  def name
	    @name
	  end

	  protected
	    def name=(name)
	      @name = name
	    end

	  private
	    def change_to_bob
	      @name = "Bob"
	    end
	end
@@@