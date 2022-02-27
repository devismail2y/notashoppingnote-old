# MongoDB

## Schema Design
![](attachments/Pasted%20image%2020220227153702.png)

### Embedding and Linking
In order to implement relationship between documents in MongoDB.
![](attachments/Pasted%20image%2020220227154704.png)

### Embedded
**Embedded** (denormalized model), capture relationship between data by storing related data in a single document structure. This is the default and primary relationship model. Because No-SQL document database means to eliminates Joins by De-normalizing data and provide efficient mechanism. Benefits of embedding: fewer queries and updates to complete common operations. Generally, use this if:
- You have contains relationship between entities.
- You have one-to-many relationship between entities

![](attachments/Pasted%20image%2020220227185433.png)

#### One to One Relationship
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


#### One to Many Relationship
This example illustrates one-to-many relationship between patron address, if the patron has multiple address entity. In normalized:
```json
// patron document
{
   _id: "joe",
   name: "Joe Bookreader"
}
// address documents
{
   patron_id: "joe", // reference to patron document
   street: "123 Fake Street",
   city: "Faketon",
   state: "MA",
   zip: "12345"
}
{
   patron_id: "joe",
   street: "1 Some Other Street",
   city: "Boston",
   state: "MA",
   zip: "12345"
}
```

```json
{
   "_id": "joe",
   "name": "Joe Bookreader",
   "addresses": [
                {
                  "street": "123 Fake Street",
                  "city": "Faketon",
                  "state": "MA",
                  "zip": "12345"
                },
                {
                  "street": "1 Some Other Street",
                  "city": "Boston",
                  "state": "MA",
                  "zip": "12345"
                }
              ]
 }
```
The problem with embedded document pattern is that it can lead to large documents, especially if the embedded field is unbounded.

### Linked
**Linked** (indexed, normalized, and referenced), describe relationships using references between documents.  Use this if:
- When embedding would result in duplication of data but would not provide sufficient read performance advantages to outweigh the implications of the duplication
- To represent more complex many-to-many relationships.
- To model large hierarchical data sets.
![](attachments/Pasted%20image%2020220227185631.png)

Consider this E-Commerce site that has a list of reviews for a product
```json
{
  "_id": 1,
  "name": "Super Widget",
  "description": "This is the most useful item in your toolbox.",
  "price": { "value": NumberDecimal("119.99"), "currency": "USD" },
  "reviews": [
    {
      "review_id": 786,
      "review_author": "Kristina",
      "review_text": "This is indeed an amazing widget.",
      "published_date": ISODate("2019-02-18")
    },
    {
      "review_id": 785,
      "review_author": "Trina",
      "review_text": "Nice product. Slow shipping.",
      "published_date": ISODate("2019-02-17")
    },
    ...
    {
      "review_id": 1,
      "review_author": "Hans",
      "review_text": "Meh, it's okay.",
      "published_date": ISODate("2017-12-06")
    }
  ]
}
```

It is in reverse chronological order. When user visits a product page, the application loads ten most recent reviews. Instead storing all of the reviews with the product, you can split the collection into two collections.

Product, information on each product and ten most recent reviews.
```json
{
  "_id": 1,
  "name": "Super Widget",
  "description": "This is the most useful item in your toolbox.",
  "price": { "value": NumberDecimal("119.99"), "currency": "USD" },
  "reviews": [
    {
      "review_id": 786,
      "review_author": "Kristina",
      "review_text": "This is indeed an amazing widget.",
      "published_date": ISODate("2019-02-18")
    }
    ...
    {
      "review_id": 777,
      "review_author": "Pablo",
      "review_text": "Amazing!",
      "published_date": ISODate("2019-02-16")
    }
  ]
}
```

Review, stores all reviews. 
```json
{
  "review_id": 786,
  "product_id": 1,
  "review_author": "Kristina",
  "review_text": "This is indeed an amazing widget.",
  "published_date": ISODate("2019-02-18")
}
{
  "review_id": 785,
  "product_id": 1,
  "review_author": "Trina",
  "review_text": "Nice product. Slow shipping.",
  "published_date": ISODate("2019-02-17")
}
...
{
  "review_id": 1,
  "product_id": 1,
  "review_author": "Hans",
  "review_text": "Meh, it's okay.",
  "published_date": ISODate("2017-12-06")
}
```







## Mid Test
![](attachments/Pasted%20image%2020220227152406.png)

Presentation on last meeting of the class.

- Real E-R diagram -> convert into Linking-Embedding Schemas
- Drill-down/roll-up (map) and flexible dimensional views
- Creating statistical reports (min/max value, mean ,etc)

