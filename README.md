Download Link: https://assignmentchef.com/product/solved-csi235-assignment3-data-manipulations
<br>
<h2>Task 1  Data manipulations</h2>

Download and unzip a file solution1.zip. You should get a file solution1.js. The file contains the specifications of the following 5 data manipulation operations on a collection tpchr.

<ul>

 <li>Remove information about an address from a description of a customer who submitted an order with an order key 1031. Next list a complete description of a customer who submitted an order with an order key 1031.</li>

 <li>Rename a key “shipped” to “shipped by” in the parts that have a retail price less than 902. Next, display all information about parts that have a retail price less than 902.</li>

 <li>Increase an account balance of all suppliers from Japan by 50% of the present value. Next, display a supplier name, nation and balance of all suppliers from Japan in a pretty format.</li>

 <li>Append to all parts that belong to a brand Brand#54 the following information about a new shipment:</li>

</ul>

“partsupp_id” : “5_1”,

“availqty” : 100,

“supplycost” : 17, “ref supplier” : “1”.

Next list all information about all parts that belong to a brand Brand#54 in a pretty format.




<ul>

 <li>Remove information about an order that has a key 1031 submitted by a customer whose key is 8. Next, list all information about all orders submitted by a customer whose key is 8.</li>

</ul>

Implement the data manipulations listed above in a data manipulation language of MongoDB. Write your solutions into the empty slots following a specification of each data manipulation in a file solution1.js. Do not remove the specifications of the data manipulations and semicolons following the specifications.

Implementation of each data manipulation is worth 1.5 mark.

When ready create a report from processing of the data manipulations in the following way.

Use gedit editor to open a file solution1.js with the specifications and implementations of the data manipulations.

Select the entire contents of the file and Copy it into a buffer.

Open a new Terminal window and start mongo client in the following way.

mongo –port 4000

Paste the contents of the buffer copied earlier from gedit window in front of &gt; prompt of mongo client. You may have to press Enter key to process the last data manipulation in a case when it is not followed by a newline control character.

Select the entire contents of the Terminal window and Copy&amp;Paste it into a file solution1.lst. Save a file solution1.lst.

<h2>deliverables</h2>

A file solution1.lst with a report from processing of MongoDB script solution1.js with the implementation of the data manipulations listed above.




And again, please remember that:

<ul>

 <li>a report without the specifications of the data manipulations and listings of the processed data manipulations scores no marks,</li>

 <li>a report that contains any kind of processing errors scores no marks.</li>

</ul>

<h2>Task 2 Query processing and data transformation with aggregation framework</h2>




Drop a collection tpchr in the following way.

db.tpchr.drop();

To re-create a collection tpchr and to load the documents into the collection, process the scripts customer.js, part.js, and supplier.js. at &gt; prompt of mongo client in the following way.

load(“customer.js”); load(“part.js”); load(“supplier.js”);

Download and unzip a file solution2.zip. You should get a file solution2.js. The file contains the comments with the specifications of the following 5 queries and data transformations.

<ul>

 <li>Save information about a customer key, name, and nation of all customers from SUDAN or ROMANIA or CANADA into a collection SUROCAN. Display in a pretty format without document identifiers the contents of a collection SUROCAN.</li>

 <li>Save all information about the supply costs (supplycost)of a part with a name floral moccasin royal powder burnished into a collection supplycosts that consists of the documents like {“supply cost”: avalue-of-supply-cost}. Display in a pretty format without document identifiers all documents in a collection supplycosts.</li>

 <li>Find the total number of part shipments of the parts of type LARGE BURNISHED STEEL or SMALL BURNISHED STEEL. Display a result in a format    {“total number  of shipments”:integer-value}.</li>

 <li>Find the total number of shipments per each part. List the results in a format</li>

</ul>

{“total number of shipments”:integer-value,     “part key”:integer-value”}.

<ul>

 <li>Find 5 largest extended prices (extended price) from all orders. List the results in a format</li>

</ul>

{“customer key”: integer-value,

“order key”:integer-value,

“line number”:integer-value,  “price”:floating-point-value}}.




Use the methods aggregate() and pretty() to implement all the queries and data transformations and to display the results. Note, that you may need two or more statements to implement a single task.

Implementation of each query/data transformation is worth 1.5 mark.

When ready create MongoDB script file solution2.js with the implementations of your queries and create a report from processing of the data manipulations in the following way.

Use gedit editor to open a file solution2.js with the specifications and implementations of the data manipulations.

Select the entire contents of the file and Copy it into a buffer.

Open a new Terminal window and start mongo client in the following way.

mongo –port 4000

Paste the contents of the buffer copied earlier from gedit window in front of &gt; prompt of mongo client. You may have to press Enter key to process the last data manipulation in a case when it is not followed by a newline control character.

Select the entire contents of the Terminal window and Copy&amp;Paste it into a file solution2.lst. Save a file solution2.lst.




<h2>Deliverables</h2>

A file solution2.lst with a report from processing of MongoDB script solution2.js with the implementation of the data manipulations listed above.




Please remember that:

<ul>

 <li>a report without the specifications of the queries and data manipulations and listings of the processed queries and data manipulations scores no marks,</li>

 <li>a report that contains any kind of processing errors scores no marks.</li>

</ul>

<h2>Task 3</h2>

<strong>Implementation of indexing </strong>

Download and unzip a file solution2.zip. You should get a file solution2.js.

Consider the documents included in a collection tpchr and the queries consistent with the following query templates.

<ul>

 <li>Find all parts that belongs to a given brand.</li>

 <li>Find all parts that has a retail price greater than a given value.</li>

 <li>Find the names of all suppliers.</li>

 <li>Find the brands and types of all parts.</li>

 <li>Find the names of customers who submitted at least one order.</li>

</ul>

Repeat the implementations of the following four steps for each one of the query patterns listed above.

<strong>Step 1</strong> Create an index that speeds up processing of a query consistent with a pattern.

<strong>Step 2</strong> Apply a method getIndexes() to list all existing indexes, for example db.collection.getIndexes().

<strong>Step 3</strong> Apply a method explain() to verify whether the system plans to use the indexes created for processing of a query consistent with a pattern, for example

db.tpchr.find({“CUSTOMER.nation”:”KENYA”}).explain();

The constants used in a query are up to you.

<strong>Step 4</strong> Drop an index created in Step 1 with a method dropIndex(), e.g. db.collection.dropIndex(“index_name”).

You can find a name given to an index by the system from the results of the Step 2.

Write your solutions into a file solution3.js in the empty slots following a specification of each problem. Do not remove the comments with the specifications of queries and semicolons following the comments !

Implementation of each index, displaying query processing plans and dropping an index is worth 1 mark.

When ready create a report from processing of the queries in the following way. Use gedit editor to open a file solution3.js with the specifications of the queries and implementations of the queries.

Select the entire contents of the file and Copy it into a buffer.

Open a new Terminal window and start mongo client in the following way.

mongo –port 4000

Paste the contents of the buffer copied earlier from gedit window in front of &gt; prompt of mongo client. You may have to press Enter key to process the last query in a case when it is not followed by a newline control character.

Select the entire contents of the Terminal window and Copy&amp;Paste it into a file solution3.lst. Save a file solution3.lst. Examine the contents of a file solution3.lst for possible errors.




<h2>Deliverables</h2>

A file solution3.lst with a report from processing of MongoDB script solution3.js with the implementation of indexing, listing the indexes and query processing plans, and dropping the indexes.




And again, please remember that:

<ul>

 <li>a report without the listings of applied methods and feedback messages issued by MongoDB scores no marks,</li>

 <li>a report that contains any kind of processing errors scores no marks.</li>

</ul>

<u>                                                                                              </u>