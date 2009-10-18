!SLIDE cover

# <span style="font-family:'Bitstream Vera Serif', serif;font-size:80%"><span style="color:#a40800">Ruby on Rails</span> Course <span style="color:#8B8B8B">2009</span></span>
## Ruby: Overview

!SLIDE facts

# Quick Facts

* First released in **1995** by Yukihiro Matsumoto ("Matz")
* Comes preinstalled in most major Linux distributions and OS X
* Available for Windows
* Influenced by Perl, Smalltalk, Eiffel, Ada, Lisp, and Python

!SLIDE oo

# Object Oriented

* **Every value in Ruby is an object**
* nil is an object
* true is an object
* 12131 is an object

!SLIDE mixins

# Mixins

In addition to classes, Ruby has modules. 

* A module has methods, just like a class, but it has **no instances**
* Instead, a module can be included, or "mixed in", to a class, which adds the methods of that module to the class
* Like inheritence, but more flexible
* A class can include many modules
* Helps with code reusability


!SLIDE dynamic

# Dynamic

* **Ruby is very dynamic**
* Ruby programs aren't compiled
* A program can modify its own definitions while it's running ("monkey patching")
* Variables in Ruby are dynamically typed ("duck typing")

!SLIDE variables

# Variables and Scope

The name of a variable automatically determines its scope.

* x is local variable (or something besides a variable)
* $x is a global variable
* @x is an instance variable
* @@x is a class variable

!SLIDE blocks

# Blocks

Blocks are one of Ruby's most unique and most loved features.

@@@ ruby
    cities.each do |city|
      city.upcase!
    end
@@@

!SLIDE editors

# Editors

Almost any text editor will do.

* Komodo Edit
* Vim
* TextMate
* NetBeans
* Aptana Studio

