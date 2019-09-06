# Streams-

Streams are abstraction.Data doesnt exist in a stream.

Functions belonging to stream

List<Integer> numbers =Arrays.asList(1,2,3,4,5,6,7,8,9,10);

filter : used to select specific values in a stream eg selecting even numbers from list number
numbers.stream().filter(e->e%2==0);

map : used to transform values eg doubling elements
numbers.stream().map(e->e*2)

reduce : it takes an intial value 0.0 as state below performs an operation and set it as the intial value for the next value on the stream eg to calcualte sum of values
numbers.stream().reduce(0.0,(carry,e) -> carry + e));

Specialised reduce functions

.sum is a specialised reduce function used to sum eg.
numbers.stream().sum());
.collect used to input values into a list:
.collect(toList()):  //list
.collect(toSet()):   //set
.collect(toMap()):   //map with first function passed to the toMap function is the key value

groupingBy
.collect(groupingBy()); //used to group similar values

Characteristics of Streams
Sized: If the stream is bounded
Ordered: If the stream element starts from first to last
Distinct: If no duplicate available   // .distinct(): used to remove duplicates in a stream
Sorted: If is ascending or descending // .sorted(): used to sort a stream
Infinite Stream: Not bounded  // Steam.iterate(k,e-> e+1) : used to create an infinite stream, starting from k.
