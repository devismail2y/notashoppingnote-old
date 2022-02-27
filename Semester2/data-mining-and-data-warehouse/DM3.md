# MongoDB

## Schema Design
![](attachments/Pasted%20image%2020220227153702.png)

### Embedding and Linking
In order to implement relationship between documents in MongoDB.
- Embedding
- Linking (indexed, normalized, and referenced)


![](attachments/Pasted%20image%2020220227154343.png)


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

