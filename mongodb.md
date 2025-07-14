# MongoDB Interview Questions and Answers

## Basic MongoDB Interview Questions

### 1. What is MongoDB, and how does it differ from traditional SQL databases?
**Answer:** MongoDB is a NoSQL, document-oriented database that stores data in BSON (Binary JSON) format. Unlike SQL databases that use tables, rows, and columns, MongoDB uses collections and documents, allowing for flexible, schema-less data structures and easier handling of unstructured or semi-structured data.

### 2. What is BSON and why is it used in MongoDB?
**Answer:** BSON (Binary JSON) is a binary-encoded serialization format. It extends JSON by supporting additional data types (like dates and binary data) and is designed for efficient storage and retrieval, making MongoDB operations faster.

### 3. What is a collection in MongoDB?
**Answer:** A collection is a group of MongoDB documents, similar to a table in relational databases. Collections do not enforce a schema, so documents within a collection can have different structures.

### 4. Describe the structure of a MongoDB document.
**Answer:** A document is a set of key-value pairs, similar to a JSON object. Values can be strings, numbers, arrays, nested documents, or other types.

---

## Intermediate MongoDB Interview Questions

### 5. How does MongoDB ensure high availability?
**Answer:** MongoDB uses replica sets, which are groups of servers that maintain the same data. If the primary node fails, a secondary node is automatically promoted to primary, ensuring continuous availability.

### 6. What is sharding, and what is the role of a sharding key?
**Answer:** Sharding is MongoDB's method for horizontal scaling. Data is distributed across multiple shards (servers) using a sharding key, which determines how documents are partitioned. Choosing the right sharding key is crucial for balanced data distribution and efficient queries.

### 7. What is the aggregation pipeline?
**Answer:** The aggregation pipeline is a framework for data aggregation and transformation. It processes documents through multiple stages (like `$match`, `$group`, `$sort`), each transforming the data before passing it to the next stage, enabling complex analytics and reporting.

### 8. How do you monitor MongoDB performance?
**Answer:** MongoDB provides built-in metrics, logs, and monitoring tools such as MongoDB Atlas, Cloud Manager, and third-party solutions. These tools help track performance, query execution, and resource usage.

### 9. What are read and write concerns in MongoDB?
**Answer:** Read and write concerns specify the level of acknowledgment and consistency required for operations. For example:
- `"majority"` ensures data is acknowledged by most replica set members.
- `"acknowledged"` and `"unacknowledged"` offer different levels of durability and performance.

---

## Advanced MongoDB Interview Questions

### 10. How do you scale a MongoDB database?
**Answer:** Scaling can be done in three ways:
- **Horizontally** using sharding.
- **Vertically** by upgrading server hardware.
- **Logically** by optimizing schema design and indexing.

### 11. What is the WiredTiger storage engine?
**Answer:** WiredTiger is MongoDB's default storage engine since version 3.2. It provides document-level concurrency, data compression, and improved performance and scalability compared to the legacy MMAPv1 engine.

### 12. How is security implemented in MongoDB?
**Answer:** MongoDB supports:
- Authentication
- Role-Based Access Control (RBAC)
- SSL/TLS encryption
- Auditing
- Network security configurations

### 13. What is GridFS and when is it used?
**Answer:** GridFS is used to store and retrieve large files (e.g., images, videos) that exceed the BSON-document size limit of 16 MB. It splits files into smaller chunks and stores them as separate documents.

### 14. How does MongoDB handle schema migrations?
**Answer:** MongoDB's flexible schema allows evolving data models over time. Schema changes can be done by updating documents in place or using background migration scripts, without downtime.

### 15. What are common pitfalls in MongoDB data modeling?
**Answer:**
- Poor choice of sharding key
- Misaligned schema with query patterns
- Ignoring index size and impact
- Not denormalizing data where needed for performance

---

## Query-Based Interview Questions

### 16. Find all documents with status = "active":
```js
db.collection.find({ status: "active" })

### 17. How do you update the salary of an employee with a specific ID?
db.employees.updateOne({ _id: 1 }, { $set: { salary: 50000 } })


### 18. Create an index on the "email" field in a users collection:
db.users.createIndex({ email: 1 })

## MongoDB Query Operators

### 19. $eq (Equal To):
db.collection.find({ age: { $eq: 25 } })

### 20. $ne (Not Equal To):
db.collection.find({ status: { $ne: "inactive" } })

### 21. $gt (Greater Than):
db.collection.find({ salary: { $gt: 50000 } })

### 22. $gte (Greater Than or Equal To):
db.collection.find({ salary: { $gte: 50000 } })