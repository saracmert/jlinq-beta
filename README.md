# jLinq Next Generation

jLinq is a 100% JavaScript library that allows you to perform complex queries on arrays of JSON data. Instead of using for loops and if statements, you can write fluent queries to filter, sort and select the information you need.

Plus jLinq extensible so you can create your own functions and plug them straight into the library.

# How Does jLinq Work?

jLinq is used for working with arrays of objects within Javascript. If you needed to collect a list of people with first names starting with a you could write a query similar to the one below.

```javascript
//select records
jlinq.from(data.source)
  .starts('first', 'a')
  .select();
 
//complex queries - no need to repeat names
//when querying the same field
jlinq.from(data.source)
    .starts('first', 'a')
    .or('b')
    .or('c')
    .sort('last')
    .select();
 
//sorting - multiple field
jlinq.from(data.source)
  .greater('age', 40)
  .sort('age', 'name');
  .select();
```
