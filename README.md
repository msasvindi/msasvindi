# Project Report

## Implementation Strategy

The project is structured to include three key algorithmic implementations: the Breadth-First Search (BFS) algorithm, hashing, and heap sort. Each component is encapsulated in its respective Java class, and a TestHarness class facilitates the testing and validation of these components. The implementation strategy focused on modularity, readability, and efficiency.

1. **BFS Algorithm**:
   - **Class**: AirportGraph.java
   - **Description**: This class represents a graph structure using adjacency lists, where each node (airport) is connected to other nodes via edges (flights). The BFS algorithm is implemented to traverse the graph and find the shortest path between nodes.
   - **Key Methods**:
     - `addEdge()`: Adds a connection (edge) between two nodes.
     - `bfs()`: Performs the BFS traversal from a given starting node, marking visited nodes and recording the shortest path.

2. **Hashing**:
   - **Class**: HashTable.java
   - **Description**: This class implements a hash table data structure with a specific hash function and a collision resolution strategy. The primary operations include insertion, deletion, and search.
   - **Key Methods**:
     - `put()`: Inserts a key-value pair into the hash table.
     - `get()`: Retrieves the value associated with a given key.
     - `remove()`: Deletes a key-value pair from the hash table.

3. **Heap Sort**:
   - **Class**: Heapsort.java
   - **Description**: This class implements the heap sort algorithm, which sorts an array by first building a binary heap and then repeatedly extracting the maximum (or minimum) element.
   - **Key Methods**:
     - `heapify()`: Ensures the binary heap property is maintained.
     - `heapsort()`: Performs the heap sort on an array.

4. **Data Loading**:
   - **Class**: CsvLoader.java
   - **Description**: This class is responsible for reading data from CSV files (AirPorts.csv, Flights.csv, HashTable.csv) and populating the corresponding data structures.
   - **Key Methods**:
     - `loadAirports()`: Loads airport data into the graph.
     - `loadFlights()`: Loads flight data and adds edges between airports.
     - `loadHashTable()`: Loads data into the hash table.

### Challenges and Solutions

- **Graph Representation**: Efficiently representing the graph structure was a challenge. Using adjacency lists allowed for a space-efficient representation, making it easy to traverse and update the graph.
- **Hash Function Design**: Designing an effective hash function to minimize collisions was crucial. By experimenting with different hash functions, a balanced solution was found that provided good performance with minimal collisions.
- **Heap Sort Efficiency**: Ensuring the heap sort algorithm's efficiency required careful implementation of the heap operations. Using a binary heap provided a balance between simplicity and efficiency, ensuring O(log n) complexity for heap operations.

### Analysis of Efficiency

- **BFS Algorithm**:
  - **Time Complexity**: O(V + E), where V is the number of vertices (airports) and E is the number of edges (flights).
  - **Space Complexity**: O(V), due to the storage requirements for visited nodes and the queue.

- **Hashing**:
  - **Average Time Complexity**: O(1) for insertion, deletion, and search.
  - **Worst-Case Time Complexity**: O(n), occurring when many collisions degrade performance.

- **Heap Sort**:
  - **Time Complexity**: O(n log n), making it efficient for sorting large datasets.
  - **Space Complexity**: O(1), as it sorts the array in place.

### Potential Improvements

- **BFS Algorithm**: Implementing advanced traversal algorithms like A* could improve performance for specific use cases, such as weighted graphs where finding the shortest path is crucial.
- **Hashing**: Implementing dynamic resizing of the hash table can improve performance by maintaining an optimal load factor and minimizing collisions.
- **Heap Sort**: Utilizing advanced data structures like Fibonacci heaps could further enhance performance, particularly for applications requiring frequent insertions and deletions.

### Conclusion

The project successfully demonstrates the implementation of BFS, hashing, and heap sort algorithms, showcasing their practical applications and efficiency. Despite the challenges, the resulting implementations are robust and efficient. Future enhancements can further optimize performance and broaden the applicability of these algorithms.

### Appendices

**Sample Input and Output**
- **BFS Algorithm**:
  - **Input**: Graph data from AirPorts.csv and Flights.csv.
  - **Output**: Shortest path between airports.

- **Hash Table**:
  - **Input**: Key-value pairs from HashTable.csv.
  - **Output**: Results of insertion, search, and deletion operations.

- **Heap Sort**:
  - **Input**: Unsorted array.
  - **Output**: Sorted array.
