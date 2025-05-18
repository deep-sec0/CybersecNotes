# 07 - IoT & Cloud Computing

## ☁️ Cloud Computing

### What is it?
Cloud computing lets users access computing resources—like servers, storage, databases, and software—**on demand via the internet**, instead of owning them physically.

### Key Characteristics:
- On-demand self-service
- Broad network access
- Resource pooling
- Rapid elasticity
- Measured service (pay-as-you-go model)

### Service Models:
- **IaaS (Infrastructure as a Service)** – e.g., AWS EC2
- **PaaS (Platform as a Service)** – e.g., Heroku
- **SaaS (Software as a Service)** – e.g., Gmail, Zoom

### Deployment Models:
- **Public Cloud** – Shared infrastructure
- **Private Cloud** – Owned by a single organization
- **Hybrid Cloud** – Mix of public and private
- **Community Cloud** – Shared by related organizations

### Benefits:
- Scalability
- Cost efficiency
- Accessibility
- Flexibility

### Threats:
- Data breaches
- Insecure APIs
- Insider threats
- Misconfigured storage

### Security Control Layers:
- **Physical** – Securing hardware and facilities
- **Network** – Firewalls, intrusion detection systems
- **Application** – Secure coding practices
- **Data** – Encryption, access control

---

## 🔌 Internet of Things (IoT)

### What is IoT?
IoT is a network of **physical devices** embedded with sensors, software, and connectivity, enabling them to **collect and exchange data**.

### How It Works:
Devices connect → collect data → send to cloud/server → analytics → take action or feedback.

### Architecture:
- **Perception Layer**: Sensors and devices
- **Network Layer**: Transfers data
- **Application Layer**: User interaction and control

### Communication Models:
- **Device-to-Device (D2D)**
- **Device-to-Cloud**
- **Gateway-to-Cloud**
- **Back-end Data Sharing**

### Common Attacks on IoT:
- **DDoS**: Distributed Denial of Service by hijacking multiple devices.
- **Rolling Code Attacks**: Capturing and replaying wireless signals (e.g., car remotes).
- **Jamming**: Interrupting wireless communications with noise signals.
- **Backdoor Access**: Exploiting hidden/unpatched access routes in devices or firmware.

> ⚠️ IoT devices are like toddlers on WiFi—always online and often unsupervised. Handle with care.
