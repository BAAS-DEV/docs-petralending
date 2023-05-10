# Hosting

## Managed Server Instances
Your website deployment forms a part of a larger and intricate ecosystem, dedicated to managing a diverse set of services, processes, and deployments. This integrated system is designed with reliability and resilience in mind.

This ecosystem ensures continuous monitoring and management of all deployments, including yours. In case of any anomalies or disruptions such as a service failure, it is equipped to initiate immediate remedial action by automatically launching a replacement service. This ensures minimal downtime and seamless user experience.

The components of your website deployment within this ecosystem include:

### Front-End Website
This is the interface that your users will interact with. It will be designed with intuitive navigation and a responsive layout to ensure a positive user experience across various devices.

### Back-end API
This is the server-side of your website, which processes requests from the front-end, interacts with the database, and returns responses. It forms the backbone of your site functionality and will be designed for efficient and reliable performance.

### Redis Cache
Redis is an in-memory data structure store used as a database, cache, and message broker. It will help improve the speed and performance of your website by caching frequently accessed data, thereby reducing the load on your database and back-end.

### Postgres Database
This is where all your data is securely stored and managed. Postgres is a powerful, open-source relational database system with a strong reputation for reliability, data integrity, and correctness.

## Robust Data Storage
Your custom website will come with an initial provision of 50 Gigabytes of dedicated instance storage. This storage capacity is allocated for the persistent storage of your website data.

The storage architecture is designed for distribution across several storage nodes. This distributed storage architecture enhances data resilience and accessibility, allowing for high availability and fault tolerance. It ensures that your data is always accessible when needed and safeguards against potential data loss.

## Monitoring

To ensure the health and performance of your website, we employ a comprehensive monitoring approach that includes both logging and metrics.

We use **Grafana** and **Kibana** as our primary monitoring dashboards. They provide us with real-time data visualization, enabling us to monitor various metrics such as server load, response times, and error rates. This helps us identify any potential issues and optimize performance.

For log management, we use the **Loki** and **ELK (Elasticsearch, Logstash, Kibana)** stacks. Loki enables us to aggregate and query logs from various sources, providing valuable insights into system performance and identifying potential issues. The ELK Stack complements Loki by providing a robust platform for searching, analyzing, and visualizing log data in real time.

## Alerting

Our alerting system is designed to notify us immediately of any issues that could impact your website's performance or availability. We use **Alertmanager**, a component of the Prometheus monitoring system, to handle alerts. Alertmanager groups similar alerts, suppresses noise, and routes alerts to the appropriate receiver, such as email, chat applications, or custom webhooks.

Our custom webhooks interface allows us to trigger specific actions in response to an alert, such as triggering auto-scaling in response to increased load or automatically creating a bug ticket for a recurring issue. This ensures that we react swiftly and effectively to any potential problems.

## Backups & Restores

Data integrity and recovery are crucial aspects of our services. We perform backups of your website twice a day to an **Amazon S3 bucket**. This bucket is secured using industry-standard encryption and access control policies to ensure your data is protected.

In the event of a data loss or corruption, we can quickly restore your website from these backups. This process is facilitated either automatically on failure, or through an admin panel, making it possible to restore your website to a previous state with minimal downtime.

In conclusion, we employ a robust set of tools and practices for monitoring, alerting, and backups, ensuring that your website remains secure, available, and performing at its best. Your peace of mind is our priority, and we strive to deliver a service you can rely on.