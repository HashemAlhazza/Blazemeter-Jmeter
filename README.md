# Blazedemo Performance Testing with JMeter

## 📌 Overview
This project is a complete performance testing suite for [Blazedemo.com](https://blazedemo.com), created using **Apache JMeter 5.6.3**.  
The goal is to simulate real-world user behavior and evaluate the system's performance, stability, and scalability under different load conditions.

The test plan includes four primary types of performance tests:
1. **Load Test** – Evaluate performance under expected peak load.
2. **Stress Test** – Determine breaking point and behavior under extreme load.
3. **Spike Test** – Measure recovery and stability after sudden traffic surges.
4. **Endurance/Soak Test** – Assess stability over long periods.

---

## 🎯 Purpose
- Measure response times, throughput, and error rates.
- Identify bottlenecks, anomalies, and potential points of failure.
- Simulate realistic traffic patterns and user actions.
- Provide reproducible performance test scenarios.

---

## 🛠 Tools Used
- **Apache JMeter 5.6.3**
- **Blazedemo.com** as the test target

---

## 📂 Test Structure
Each test type has its own **Thread Group** in JMeter, with independent controllers, samplers, and assertions.

### 1. Load Test
- **Goal:** Assess performance under predicted peak usage.
- **Expected Load:** 1,500 concurrent users.
- **Duration:** 1 hour.
- **Ramp-Up:** 30 minutes.
- **User Actions:**
  - Select Destination (25%)
  - Choose Flight (50%)
  - Input Data & Purchase (25%)

### 2. Stress Test
- **Goal:** Identify breaking point.
- **Phases:**
  - Phase 1: 100 users
  - Phase 2: 600 users
  - Phase 3: 1,700 users
- Each phase runs 5 minutes at steady load.

### 3. Spike Test
- **Goal:** Observe system behavior after sudden load surges.
- **Stages:**
  - Stage 1: 100 users (baseline)
  - Stage 2: Spike to 300 users
  - Stage 3: Spike to 500 users

### 4. Endurance/Soak Test
- **Goal:** Detect long-term stability issues.
- **Expected Load:** 1,200 concurrent users.
- **Duration:** Extended run (hours/days).

---

## 📊 Metrics Collected
| Metric                     | Unit          |
|----------------------------|---------------|
| Average Response Time      | seconds       |
| Average Throughput         | requests/sec  |
| Error Rate                 | %             |
| Resource Utilization       | %             |

---

## 📄 How to Run
1. Install [Apache JMeter](https://jmeter.apache.org/) (version 5.6.3 or later).
2. Open the provided `.jmx` file in JMeter.
3. Configure listeners to capture and visualize results.
4. Run the desired Thread Group.

---

## 📈 Results
Each test execution records performance metrics for different user actions and phases.  
The detailed results are available in the `Performance Test Execution Sheet` included in this repository.

---

## 👨‍💻 Author
**Hashem Al-Hazzaa**  
Automotive Embedded Software Engineer & Performance Testing Enthusiast

---

## 📜 License
This project is licensed under the [MIT License](LICENSE).