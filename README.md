**GCP Cloud Infrastructure Automation using Python, Cloud Functions, and Cloud Scheduler**

This project automates the management of Google Cloud Platform (GCP) services for non-production environments using Python scripts, Cloud Functions, and Cloud Scheduler. The automation reduces cloud costs by controlling services such as Compute Engine, Cloud SQL, and Kubernetes, automatically starting and stopping them based on scheduled times.

**Key Features**

**Automated Cloud Management:** Python scripts that automate starting and stopping GCP services based on schedules.

**Serverless Cloud Functions:**  Deployed Cloud Functions to execute the Python scripts, ensuring efficiency and scalability.

**Scheduled Tasks**: Cloud Scheduler triggers Cloud Functions to run the automation scripts at predefined intervals.

**Cost Optimization:** Automated control over non-production cloud resources reduces unnecessary resource consumption during off-hours.

**Role-Based Access Control (RBAC):** Service accounts with precise roles to ensure secure automation workflows.

**Technologies Used**

Google Cloud Platform (GCP)
Cloud Functions
Cloud Scheduler
Compute Engine
Cloud SQL
**Python:** Automation scripting language.
**Terraform:** Infrastructure as code for deploying cloud resources.

**Prerequisites**

**Google Cloud SDK:** Ensure you have the GCloud SDK installed and configured.
**Terraform:** Install Terraform for infrastructure provisioning.
**Python 3.x:** Ensure Python is installed for scripting.

**Setup Guide**
**Clone the Repository:**
Copy code
git clone https://github.com/your-username/cloud-infra-automation.git
cd cloud-infra-automation
Configure GCP: Set up your GCP project and ensure you have the correct IAM roles to manage Cloud Functions and Cloud Scheduler.

**Deploy Terraform:**

Navigate to the terraform/ directory.
Initialize and apply Terraform to provision necessary resources:
bash
Copy code
terraform init
terraform apply
**Python Script Configuration:**
Edit start_services.py and stop_services.py with the service names and project configurations you want to control.
**Deploy Cloud Functions:** Use Terraform to deploy the Python scripts as Cloud Functions:


Copy code
terraform apply
**Set Up Cloud Scheduler:**

Configure Cloud Scheduler to trigger the Cloud Functions at specific times (e.g., during non-working hours for stop and start).
Usage
Once the Terraform script is applied, Cloud Scheduler will automatically trigger the Cloud Functions at the defined intervals. You can monitor the execution of Cloud Functions and manage the logs through the GCP Console.

**To manually test the automation:**

Copy code
gcloud functions call start_services_function
gcloud functions call stop_services_function
Contributing
Feel free to fork this repository, submit pull requests, or raise issues. Contributions are welcome to improve the project further.



