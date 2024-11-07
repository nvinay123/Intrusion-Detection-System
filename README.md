The project implements an Intelligent Intrusion Detection and Monitoring System that provides real-time assessment of system health, anomaly detection, and alert notifications. Built using Python, Flask, and JWT-based authentication, the system offers secure access to critical system metrics and alerts on a user-friendly dashboard. Designed with multi-threaded agents, it operates autonomously to monitor, evaluate, and respond to potential security threats.

Key Features:
1. System Monitoring Agents:
  SystemSentinelAgent: Collects CPU and memory usage data using psutil, identifies anomalies through predefined thresholds in the AnomalyDetectionModel, and logs them. When threats are detected, it generates a digital signature for alert authenticity and dispatches alerts via email.
  SystemFaultEvaluationAgent: Analyzes system data periodically to detect faults, assisting in anomaly analysis for enhanced system stability.
  SystemReplicationAgent: Manages replication and recovery processes, helping maintain data consistency and system resilience during critical events.
3. Anomaly Detection and Digital Signature Verification:
  Anomaly detection is performed by comparing real-time CPU and memory data to predefined thresholds. Alerts are digitally signed using RSA encryption, ensuring secure and authenticated alert messages.
4. Email Alert System:
  Alerts are securely sent to administrators via SMTP, with an App Password used for authentication. Signed messages ensure integrity, allowing admins to quickly identify genuine threats.
5. JWT Authentication:
  Provides secure access to system data by requiring users to log in to obtain a JSON Web Token (JWT), which is validated on each request for sensitive data.
5. Flask Web Interface:
  A dashboard displays real-time metrics, including CPU usage, memory usage, and any recent anomalies. The /metrics route is protected by JWT authentication to ensure that only authorized users can access system information.
6. Customizable Thresholds:
  The AnomalyDetectionModel can be adjusted with specific CPU and memory thresholds, allowing the system to adapt to different performance expectations and hardware environments.
7. Multi-threaded Execution:
  The system is designed to run multiple agents concurrently using threading, enabling continuous monitoring, analysis, and alerting without interruptions.
8. Profile Database Update:
  A ProfileDatabase component simulates updates to a central database with real-time data, facilitating better decision-making and profiling.


How to Run This:
1. Install Required Libraries: Make sure you have Python installed and install the necessary libraries with:
  "pip install Flask psutil pyjwt cryptography"
2. Configure Email Settings: Update the following email settings in the code for alert notifications:
  sender_email: Replace with your email address.
  receiver_email: Replace with the recipient’s email address.
  app_password: Replace with the App Password for the sender’s email.
3. Update the Secret Key: Modify the SECRET_KEY value in the code for secure JWT token handling.
4. Run ids_system.py in command prompt

Main Page:
<img width="1105" alt="Main Page" src="https://github.com/user-attachments/assets/8e7036fd-a5ec-4ab6-8526-2a8b414e38eb">

Token:
<img width="500" alt="Token" src="https://github.com/user-attachments/assets/619ff334-fa64-491b-b60b-1f759c963fab">

Digital Signature:
<img width="615" alt="Digital" src="https://github.com/user-attachments/assets/0e86401e-1629-4672-a3e6-c662388da2ce">

Backend:
<img width="560" alt="Backend" src="https://github.com/user-attachments/assets/fad17512-aaf7-44e6-8b33-f6e3863b4fee">

Login Page:
<img width="343" alt="Login" src="https://github.com/user-attachments/assets/435d8c14-ee91-4920-bcfa-3b888e8198cf">






