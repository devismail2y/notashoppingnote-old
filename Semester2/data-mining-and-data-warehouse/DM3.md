# MongoDB

## Schema Design
![](attachments/Pasted%20image%2020220227153702.png)

### Embedding and Linking
In order to implement relationship between documents in MongoDB.
![](attachments/Pasted%20image%2020220227154704.png)

**Embedded** (denormalized model), capture relationship between data by storing related data in a single document structure. This is the default and primary relationship model. Because No-SQL document database means to eliminates Joins by De-normalizing data and provide efficient mechanism. Benefits of embedding: fewer queries and updates to complete common operations. Generally, use this if:
- You have contains relationship between entities.
- You have one-to-many relationship between entities

![](attachments/Pasted%20image%2020220227185433.png)

**Linked** (indexed, normalized, and referenced), describe relationships using references between documents.  Use this if:
- When embedding would result in duplication of data but would not provide sufficient read performance advantages to outweigh the implications of the duplication
- To represent more complex many-to-many relationships.
- To model large hierarchical data sets.
![](attachments/Pasted%20image%2020220227185631.png)




### One to One Relationship

For example this patron and address relationship, the address belongs to patron. In the normalized data model, the address document contains a reference to the patron document.
```json
// patron document
{
   _id: "joe",
   name: "Joe Bookreader"
}

// address document
{
   patron_id: "joe", // reference to patron document
   street: "123 Fake Street",
   city: "Faketon",
   state: "MA",
   zip: "12345"
}
```

If the address data is frequently retrieved with the name information, then with referencing, your application needs to issue multiple queries to resolve the reference. This is data model that embed address data in the patron data.
```json
{
   _id: "joe",
   name: "Joe Bookreader",
   address: {
              street: "123 Fake Street",
              city: "Faketon",
              state: "MA",
              zip: "12345"
            }
}
```


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

