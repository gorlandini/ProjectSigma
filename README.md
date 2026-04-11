# 🚀 Performance Comparison: WebFlux vs Traditional Spring

> This project was created as part of a technical study to evaluate performance and scalability in modern backend applications.

This project demonstrates a simple performance comparison between two approaches:

- **Spring WebFlux (reactive, non-blocking)**
- **Spring MVC (traditional, blocking)**

The goal was to understand how each one behaves under load.

---

# 📊 Test Summary

The tests were executed using Apache JMeter with the same conditions for both versions.

## Results

### ✅ WebFlux (Reactive)

- Average response time: **5 ms**
- Throughput: **~948 requests/second**
- Stable performance under load

---

### ⚠️ Spring MVC (Blocking)

- Average response time: **983 ms**
- Throughput: **~409 requests/second**
- High variation in response times under load

---

# 🔍 Key Insight

Even while performing **database operations**, the reactive version (WebFlux) was significantly faster and more stable than the traditional approach using in-memory data.

👉 This shows that:

> **How the application handles concurrency can impact performance more than the type of database used.**

---

# 💡 Why This Matters

- Applications with many simultaneous users benefit from reactive architectures
- Blocking models can become slower under heavy load due to thread limitations
- Performance should be validated with real tests, not assumptions

---

# 🧪 Tools Used

- Spring Boot
- Spring WebFlux
- Spring MVC
- Apache JMeter
- H2 Database

---

# 📌 Conclusion

This project highlights the importance of choosing the right architecture based on scalability needs and demonstrates a data-driven approach to decision making.
