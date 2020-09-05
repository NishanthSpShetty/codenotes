## Code and Design smells.
 Late 1990 -> kend beck.

#### code smells are not
1. bugs
2. compiler errors
3. dead code/non functioning code.

## Code smell 
- Warning or signposts pointing to inefficiencies and potential weekness.
- Can be ignored without breaking the project, but leaving them will be disadvantage to you and preject.
- Can lead to brittle program and end up leaving cascading bugs.
      
> duplicate code 
> 
> Solution:
>           Separate them into helper funciton and centralize code duplicate.
>           Limits code changes to single location.

   ---

## Design smells   

> Design smells are the odors of rotting software - R.C Martin

Deals with architectural issue  such as 

- Improper abstraction.
- Modularization
- Unhealthy dependencies. 

### Code smells
1. Method level 
	- Identifier naming
  	- Bloated method -> too many action acting in a single funciton
  	- Excessive parameter -> long list of parameters.
  	- Excessive returns (not supported in all language)
  	- God line -> lomg funciton call

2. Class level smells
	- Goldilocks zone
		- Oversized classes
		- Undersized classes
    - feature envy
		* When class is uses a method excessively from another class.
		* Leads dependencies and brittle code.
		* Need look closely at the class dependencies
		* Consider transferring code to dependent class or refactoring  to share class members.
	- inappropriate intimacy
		* When the class is dependent on implementation of others. class referring to another class private member.
		* [Soulution] Refactoring code or creating a shared implementation key.
	- Literal usage.
		* Hard coded values. -> Make it offsite, resource file or database.
	- Data clumping.
		Passing around primitive values, can be made into separate class.
3. Application smells.
	
	- Shotgun surgery
		* Too many duplicate of code.
		* Update requires a repeated code blocks in multiple location to be modified.
		* [Solution] both can be avoided by refactoring into separate code blocks.
	- contrived complexity
		* unnecessarily complex implementation.


### Design smell categories.

1. Abstraction
    -  Missing abstraction - data clumping.
    -  multifaceted abstraction - class doing a lot of work, reading and encoding data from file and writing back.
    -  Duplicate abstraction
    -  incomplete abstraction - class or interface doesnt implementate its responsibility fully. extending these class should implemenet all of its said responsibility.

2. Encapsulartion
		(Protection of abstraction or member)
    -  Deficient encapsulation.
    -  Unrestrained encapsulation.
    -  Unexploited encapuslation. -> checking type using if/switch rather than depending on exploiting type variant.

3. Modularization
		(incorrect modularization)
    -  Insufficient modularization
    -  Broken modularization
    -  Cyclically dependent modularization
			Use of dependency injection.

4. Hierarchy.
		how abstractions are structured.
    -  Polygon hierarchy
	```
	A<- B <-c  	==>		A<-C
	 \ <-D -/     
	```
	streamline hierarchy removing unecessory dependency.
    -  Broken hierarchy
    -  Cyclic hierarchy

More
1. [Sharpen your sense of (code) smells. By jetbrains](https://blog.jetbrains.com/dotnet/2018/06/18/sharpen-sense-code-smell/)
