##Steps to Store Sensitive Information as Secrets in Jenkins
---
1. Access Jenkins Credentials Section
Open your Jenkins dashboard in a web browser.
From the Jenkins homepage, go to Manage Jenkins.
In the Manage Jenkins section, click on Manage Credentials.
2. Select a Domain for Storing Credentials
Global Domain: By default, Jenkins provides a global domain for storing credentials. If you don't have specific requirements for domains, you can use the global domain to store your secrets.
Create a New Domain (Optional): You can create a new domain to group your credentials by clicking (global) and then selecting Add domain.
3. Add New Credentials
Click on (global) or any other domain where you want to store the credentials.
Click Add Credentials on the left sidebar.
4. Choose the Credential Type
You will be presented with different types of credentials you can store:
##Username with Password: Store a username and password (e.g., for databases, APIs).
SSH Username with Private Key: Store an SSH username and private key (e.g., for SSH access to servers or EC2 instances).
Secret Text: Store a plain text secret (e.g., API keys, tokens).
Secret File: Store a file containing secrets (e.g., SSL certificates, private keys).
5. Add SSH Key for EC2 Access
Credential Type: Choose SSH Username with private key.
Username: Enter the SSH username (e.g., ubuntu for EC2 instances).
Private Key: You can either:
Enter directly: Paste the private key in the Private Key field.
From a file on Jenkins master: Select a file on the Jenkins master containing the private key.
ID: Provide a unique ID for the SSH key, e.g., EC2_SSH_KEY. This ID will be used in your Jenkins pipeline to access the secret.
6. Add Secret Text (For Database Password or API Keys)
Credential Type: Choose Secret text.
Secret: Paste the sensitive information (e.g., database password, API token).
ID: Provide a unique ID for the secret (e.g., DB_PASSWORD for a database password).
7. Save the Credentials
After entering the necessary details, click OK to save the credentials.

Now your sensitive information is securely stored in Jenkins and can be accessed by Jenkins jobs or pipelines.



---


