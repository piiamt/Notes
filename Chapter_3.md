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
