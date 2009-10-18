!SLIDE cover

# <span style="font-family:'Bitstream Vera Serif', serif;font-size:80%"><span style="color:#a40800">Ruby on Rails</span> Course <span style="color:#8B8B8B">2009</span></span>
## Ruby: Operators

!SLIDE assignment

# Assignment

Assignment in Ruby is done using the equals sign (=).

@@@ ruby
	colour = "red"
	other_colour = String.new("blue")
	number = 123
@@@

!SLIDE self

# Self Assignment

@@@ ruby
	x = 1           # => 1
	x += x          # => 2
	x -= x          # => 0
	x += 4          # => 4
	x *= x          # => 16
	x **= x         # => 18446744073709551616 # Raise to the power
	x /= x          # => 1
@@@

There are no increment/decrement operators in Ruby.

!SLIDE multiple

# Multiple Assignment

You can assign values to multiple variables on one line.

@@@ ruby
	colour1, colour2, colour3 = "red", "blue", "green"
	colours, city = ["red", "blue", "green"], "Helsinki"
@@@

!SLIDE conditional

# Conditional Assignment

The operator ||= checks whether a variable is nil (or inexistent) and assigns an object to it if it is.

@@@ ruby
	configuration ||= "default value"
@@@

!SLIDE comparison

# Comparison Operators

<table cellspacing="0">
	<tr>
		<th style="padding-right: 40px;">Operator</th>
		<th>Description</th>
	</tr>
	
	<tr>
		<td>==</td>
		<td>Equivalency</td>
	</tr>
	
	<tr>
		<td>!=</td>
		<td>Inequality</td>
	</tr>
	
	<tr>
		<td>&lt;</td>
		<td>Less than</td>
	</tr>
	
	<tr>
		<td>&gt;</td>
		<td>Greater than</td>
	</tr>
	
	<tr>
		<td>&gt;=</td>
		<td>Greater than or equal to</td>
	</tr>
	
	<tr>
		<td>&lt;=</td>
		<td>Less than or equal to</td>
	</tr>
	
	<tr>
		<td>&lt;=&gt;</td>
		<td>
			Combined comparison operator. Returns:
			<ul>
				<li>0 if the values are equal</li>
				<li>-1 if the second is greater than the first</li>
				<li>1 if the first is greater than the second</li>
			</ul>
		</td>
	</tr>
</table>

!SLIDE comparisonexamples

# Comparison Operators

## Examples

@@@ ruby
	5 == 5      # => true
	5 != 4      # => true
	4 > 5       # => false
	4 < 5       # => true
	5 <=> 5     # => 0
	5 <=> 2     # => 1
	5 <=> 6     # => -1
@@@

!SLIDE andornot

# And (&&), Or (||), Not (!)

@@@ ruby
	x = false
	y = true

	x && y    # => false
	x || y    # => true
	!x        # => true
	!y        # => false
@@@
