# DAA Load Balancer Project

## Overview

This project implements an Intelligent Load Distribution Engine as part of the Design and Analysis of Algorithms (DAA) course. It demonstrates real-time load balancing across multiple backend servers using classical algorithms, along with monitoring and a control dashboard.

## Features

* Multiple load balancing algorithms:

  * Round Robin
  * Weighted Round Robin
  * Least Connections
  * IP Hash
  * Random Selection
* C++-based algorithm engine for efficient computation
* Python Flask-based load balancer and backend servers
* Web dashboard for monitoring and control
* Real-time metrics (requests, connections, response time)
* Health monitoring of backend servers

## Project Structure

```
DAA_LoadBalancer/
├── config/
│   └── server_config.json
├── backend/
│   └── backend_server.py
├── load_balancer/
│   └── load_balancer.py
├── algorithms/
│   └── algo_logic.cpp
├── templates/
│   └── dashboard.html
├── requirements.txt
└── README.md
```


## Setup

### Install dependencies

```
pip install -r requirements.txt
```

### Compile C++ algorithm module

```
g++ algorithms/algo_logic.cpp -o algorithms/algo_logic
```

## Running the Project

### Start backend servers

```
python backend/backend_server.py 5001
python backend/backend_server.py 5002
python backend/backend_server.py 5003
```

### Start load balancer

```
python load_balancer/load_balancer.py
```


## Access

* User endpoint: http://localhost:8000/
* Dashboard: http://localhost:8000/dashboard
* API metrics: http://localhost:8000/api/metrics


## Algorithms and Complexity

| Algorithm            | Time Complexity |
| -------------------- | --------------- |
| Round Robin          | O(1)            |
| Weighted Round Robin | O(1)            |
| Least Connections    | O(n)            |
| IP Hash              | O(1)            |
| Random               | O(1)            |


## DAA Concepts Used

* Scheduling algorithms
* Greedy approach
* Hashing techniques
* Randomized algorithms


## Conclusion

This project demonstrates practical implementation of DAA concepts in distributed systems by combining algorithm design with real-world networking and system behavior.
