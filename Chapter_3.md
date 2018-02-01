## Chapter 3

In this chapter we will start coding and talking about how the various portions of the Java language work.

### How do we convert our flow charts to code?

We have been using three things in our flowcharts:

#### Statements:
~~~
+---------------------------+
| Decrease the counter by 1 |
+---------------------------+
~~~
~~~
+---------------+
| Print "Hello" |
+---------------+
~~~
If they are simple, these will generally translate into a sngle line of code:
~~~
counter = counter -1;

system.out.print("Hello");
~~~
If they are complex, then we need to break them down further.  As an example think of the statements in my algorithm where I asked does everyone know about the meeting.

#### Conditionals:
~~~
          |
          |
          v
         / \
        /   \       Yes
   if our counter \-----------+
      equals 5    /           |
        \   /                 v
         \ /          +---------------+
          |           | Statement 1   |
       No |           +---------------+
          v                   |
+-----------------+           v
| Statement 3     |   +---------------+
+-----------------+   | Statement 2   |
          |           +---------------+
          |                   |
          +-------------------+
          |
          v
~~~

This translates into the code:
~~~
if( counter == 5 )
{
   Statement 1
   Statement 2
}
else
{
   Statement 3
}
~~~

#### loops

Any time we have an edge going back to a previous step, we have a loop.  Thi is an indication that we want to do some steps multiple times.

When we have a loop either it has a conditional in it somewhere that has oneoption tht leaves the loop, or we have a never ending, infinate loop.  We don't want infinate loops, so I'm going to assume that you have such a conditional in the sequence of steps that is repeated, similar to below:
~~~
          |
          v
  +---------------+
  | Statement 5   |
  +---------------+
          |
+-------->|
|         |
|         v
| +---------------+
| | Statement 6   |
| +---------------+
|         |
|         v
|        / \
|       /   \          Yes      +---------------+
|   if temp is less \ --------->| Statement 9   |
|      than 50      /           +---------------+
|       \   /                           |
|        \ /                            |
|         | No                          |
|         v                             |
| +---------------+                     |
| | Statement 7   |                     |
| +---------------+                     |
|         |                             |
|         v                             |
| +---------------+                     |
+-| Statement 8   |                     |
  +---------------+                     |
                                        v
  ~~~

For this we will wait to start the loop until we get to the conditional, then we will create a loop with the exit condition:

~~~
Statement 5
Statement 6
while( temp >= 50 )
{
   Statement 7
   Statement 8
   Statement 6
}
Statement 9
~~~

Note that with this condition we had to invert it, as the written test in the flowchart tested to exit the loop, not stay in it.

#### Tests
How can we test things in conditionals and loops?

When we test something we want the result to be true or false.  We know of some of these and use them regularly:
* <  less than
* >  greater than
* == is equal to
* <= less than or equal to
* >= greater than or equal to

What if we need something to not be one of these things?  For that we have a not opperator: 
* !

it can be used with the is equal to opperator to modifyit:
* != is not equal to

or it can be used with any test:
* !( 5 > 8 )

note the parenthesis here to indicate what we want the oppisite truth value of (parenthesis still evaluate before the not opperator.)

