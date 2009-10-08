!SLIDE cover

# <span style="font-family:'Bitstream Vera Serif', serif;font-size:80%"><span style="color:#a40800">Ruby on Rails</span> Course <span style="color:#8B8B8B">2009</span></span>
## Ruby: Basics

!SLIDE irb

# Interactive Ruby (irb)

Irb is an interactive interface to Ruby

* Mainly used for testing small snippets of code.
* Run by executing **irb** in a terminal
* Online version at <http://tryruby.sophrinix.com>

!SLIDE datatypes

# Datatypes

Almost everything in Ruby is an object. Try the following in irb:

@@@ ruby
    123.class
    999999999999999999999999999999999999999999999.class
    nil.class
    true.class
    "hello world".class
    :symbol.class
@@@

!SLIDE constants

# Constants

* Constants always start with capital letters
* You can change constants in Ruby, but you shouldn't

@@@ ruby
    Constant = 5    # This is a constant
    constant = 5    # This is not
@@@

!SLIDE symbols

# Symbols

Every time you type a string, Ruby makes a new object:

@@@ ruby
    irb> "live long and prosper".object_id
    => -606662268
    irb> "live long and prosper".object_id
    => -606666538
@@@

Notice that the object ID returned by irb is different even for the same two strings.

!SLIDE symbols

To save memory Ruby has provided "symbols"

@@@ ruby
    irb> :live_long_and_prosper.object_id
    => 150808
    irb> :live_long_and_prosper.object_id
    => 150808
@@@

Symbols are often used as hash keys.

!SLIDE hashes

# Hashes

* Hashes are like dictionaries
* You have a key, a reference, and you look it up to find the associated object, the definition.

@@@ ruby
    hash = { :leia => "Princess from Alderaan", 
             :han => "Rebel without a cause",
             :luke => "Farmboy turned Jedi" }
@@@

!SLIDE arrays

# Arrays

Arrays are a lot like hashes, but the keys are always consecutive numbers. 

@@@ ruby
    array = ["This", "is", "an array"]
    puts array[0] # => "This"
    puts array[3] # => nil
@@@

Using an out of range index will return nil.

!SLIDE strings

# Strings

* String literals
* Single quotes
* Double quotes
* Escape sequences
* Very long strings

!SLIDE literals

# String Literals

@@@ ruby
    puts 'Hello world'
    puts "Hello world"

    puts "Betty's pie shop"
    puts 'Betty\'s pie shop'
@@@

!SLIDE singlequotes

# Single Quotes

Single quotes only support two escape sequences:

@@@
    \' - single quote
    \\ - single backslash
@@@

!SLIDE doublequotes

# Double Quotes

* Double quotes allow for many more escape sequences than single quotes.
* You can also embed Ruby code inside of a String literal (interpolation)

@@@ ruby
    name = "bob"
    puts "Your name is #{name.capitalize}"
@@@

!SLIDE escape

# Escape Sequences

@@@
    \" - double quote
    \\ - single backslash
    \a - bell/alert
    \b - backspace
    \r - carriage return
    \n - newline
    \s - space
    \t - tab
@@@
