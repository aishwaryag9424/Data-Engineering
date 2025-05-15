# Data-Engineering

## File formats used in Big Data:

A good file format should be stored, ordered and compressed efficiently. Following are the file formats used commonly: 
1. JSON: JSON (JavaScript Object Notation) is a human-readable text format for storing and transmitting data, often used in web applications and APIs. It's built on key-value pairs and arrays, allowing for flexible data representation.
Example:

   {
  "name": "John Doe",
  "age": 30,
  "address": {
    "street": "123 Main St",
    "city": "Anytown"
  },
  "skills": ["HTML", "CSS", "JavaScript"]
}

2. AVRO: Avro is a data serialization system that provides a compact, fast, binary data format for storing and transmitting data. It uses a schema, which describes the structure of the data, in a JSON format and stores the data in blocks within a file, according to the Apache Avro website. Avro supports a range of data types, including primitive types like boolean, int, long, and string, as well as complex types like arrays, maps, and enums. 

3. CSV: A CSV (Comma-Separated Values) file is a simple text file that stores data in a tabular format, where each row represents a record, and each column represents a field. Fields within a row are separated by commas. If a field itself contains a comma, it's enclosed in double quotes. CSV files are widely used for data exchange and storage due to their simplicity and versatility.
   
4. ORC: ORC (Optimized Row Columnar) is a columnar file format for storing data, especially in Hadoop environments, that offers efficient data storage and processing, particularly for large datasets. It's type-aware, meaning it chooses the best encoding for each data type, and it includes indexes for faster data access. ORC is often used with Apache Hive and Spark. 

5. Parquet: Parquet is a widely-used open-source columnar storage file format designed for efficient data storage and retrieval, particularly for large datasets. It excels at handling complex data in bulk due to its efficient compression and encoding schemes. 

## Types of Storage format:
1. Column based: ORC, Parquet
2. Row based: JSON, CSV, AVRO

## Best format to store your data?
Storing the data depends on how we are accessing the end result. For example if you want to know total sales or total items sold, which are some aggregation focused on some particular column then it is prefered to store in column based format. But if some ML model or data analysis such as how a product is sold and what is the user behavior when he is buying things, in this case row based format is preferred.
