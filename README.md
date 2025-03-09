## 🚀 GraphZen - Graph Algorithms Visualizer

### 📌 Introduction :

GraphZen is an interactive graph algorithms visualizer that helps users understand and analyze graph algorithms through dynamic visual representations. It is designed for students, developers, and competitive programmers to experiment with various graph algorithms and gain deeper insights into their working.

### ✨ Features :
- 🔍 Visualize Popular Graph Algorithms such as BFS, DFS, Dijkstra’s Algorithm, Kruskal’s Algorithm, Prim’s Algorithm, and more.

- 🎨 Interactive UI with real-time graph manipulation and visualization.

- 🚀 Step-by-Step Execution for easy understanding of how algorithms progress.

- 📊 Performance Analysis with execution time and complexity display.

- 🔄 Custom Graph Creation – Users can add or remove nodes and edges dynamically.

- 🏆 Algorithm Comparison Mode – Compare multiple algorithms on the same graph.

- 📡 Backend Processing with Java (Spring Boot) for efficient computation.

- 🗄 Data Persistence using MySQL to store user-created graphs.


### 🛠 Technologies Used :
- ☕ Java (Spring Boot) – Backend logic for algorithm processing.

- 🌐 React.js – Frontend for interactive visualization.

- 🗄 MySQL – Database for storing user-generated graphs.

- 📡 RESTful APIs – Communication between frontend and backend.

- 🎨 D3.js/Vis.js – Graph visualization and animation.


### 🏗 Installation & Setup
  #### Prerequisites

- Java 17+

- MySQL Server

- Maven

- Node.js & npm (for frontend)

- IDE (IntelliJ IDEA, VS Code, or Eclipse)

#### Steps to Run the Project

###### 1. Clone this repository:

```bash
git clone https://github.com/swathi-57/GraphZen
```
##### 2. Navigate to the backened directory:
```bash
cd graphzen/backend
```
###### 3. Configure the application.properties file with MySQL credentials:

```bash
spring.datasource.url=jdbc:mysql://localhost:3306/graphzen
spring.datasource.username=root
spring.datasource.password=yourpassword
```

##### 4. Run the application:
```bash
mvn spring-boot:run
```

#### Frontend (React.js)

1. Navigate to the frontend directory:
    
  ```bash
  cd graphzen/frontend
  ```

2.Install dependencies:
  ```bash
  npm install
  ```
3. Start the frontend server:
  ```bash
  npm start
  ```


### 📌 Usage Example
```bash
@RestController
@RequestMapping("/algorithm")
public class AlgorithmController {
    @Autowired
    private AlgorithmService algorithmService;

    @PostMapping("/bfs")
    public ResponseEntity<List<Integer>> runBFS(@RequestBody GraphRequest request) {
        return ResponseEntity.ok(algorithmService.executeBFS(request));
    }
}
```


###  🎯 API Endpoints
| Method | Endpoint    | Description                |
| :-------- | :------- | :------------------------- |
| `POST` | `/graph/create` | Create a custom graph
| `GET` | `/graph/load` | Load a saved graph
| `POST` | `/algorithm/bfs` | Run BFS algorithm
| `POST` | `/algorithm/dfs` | Run DFS algorithm
| `POST` | `/algorithm/dijkstra` |Run Dijkstra’s algorithm
| `POST` | `/algorithm/kruskal` | Run Kruskal’s algorithm
| `POST` | `/algorithm/prim` | Run Prim’s algorithm




### 🤝 Contributing

 If you want to contribute, feel free to fork this repository and submit a pull request.

### 📜 License

This project is licensed under the MIT License.
