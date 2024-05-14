**Kafka Topics**

- Streams of data within a Kafka cluster
- Can have multiple topics with unique names (e.g., logs, purchases)
- Support any message format (e.g., JSON, Avro, binary)

**Partitions**

- Topics can be divided into partitions (e.g., three partitions: zero, one, two)
- Messages are written to partitions in an ordered sequence
- Each message has a partition offset (ID) that increases incrementally

**Data Immutability**

- Once data is written to a partition, it cannot be changed or deleted

**Data Retention**

- Data is kept for a limited time (default: one week) before being discarded

**Offsets**

- Offsets are unique within each partition
- Not reused even after messages are deleted
- Message order is guaranteed within partitions, but not across partitions

**Message Assignment**

- Messages are randomly assigned to partitions
- Can be overridden by providing a message key

**Additional Notes**

- Kafka topics are immutable (cannot be modified)
- Data is only kept for a specified duration
- Offsets are assigned incrementally and not reused
- Message order is guaranteed within partitions
- The number of partitions for a topic is configurable
- Message assignment is random by default, but can be customized with message keys