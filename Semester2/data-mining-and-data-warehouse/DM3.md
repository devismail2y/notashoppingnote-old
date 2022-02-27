# MongoDB

## Schema Design
![](attachments/Pasted%20image%2020220227153702.png)

### Embedding and Linking
In order to implement relationship between documents in MongoDB.
- Embedding, the default and primary relationship model. Because No-SQL document database means to eliminates Joins by De-normalizing data and provide efficient mechanism.
- Linking (indexed, normalized, and referenced)

Example: Post can have one or more comments.

![](attachments/Pasted%20image%2020220227154704.png)

The reason of using linked relationship:
- Access linked data in an independent manner (search all comments from a specific author, regardless the post).
- Avoid repetitions, i.e. relationship between a comment and its author (it repeats several times the same value), we can map the author as a separate, referred document.
- High Frequency for access or update of linked data: accessing/updating a document without updating its parent will enhance performance.
- Privacy & Security motifs may impose to split the data into different documents
- Mongo 1.8 has 16MB limit of single document.

Negative side of linked relationship
- Lose consistency of Writings and Readings in one-to-one and one-to-many relationships.




### One to One Relationship
Konversi dari relational ke no SQL. Based on example below, the zip will be the master entity and person will be the slave, because person table is inside the zip bracket.
![](attachments/Pasted%20image%2020220227153145.png)

### One to Many Relationship
Publisher is the master, and book is the slave, because the book is the transactional data. Embedding using equal operator.
![](attachments/Pasted%20image%2020220227153908.png)

Embedding use equal (=) operator.



## Mid Test
![](attachments/Pasted%20image%2020220227152406.png)

Presentation on last meeting of the class.

- Real E-R diagram -> convert into Linking-Embedding Schemas
- Drill-down/roll-up (map) and flexible dimensional views
- Creating statistical reports (min/max value, mean ,etc)

