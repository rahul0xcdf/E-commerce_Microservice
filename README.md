This is an e-commerce application built with a microservices architecture.

### Architecture

The application is divided into the following services:

*   **Frontend:** An Angular application located in the `emartapp/client` directory.
*   **Backend:**
    *   A Java API in the `emartapp/javaapi` directory.
    *   A Node.js API in the `emartapp/nodeapi` directory.
*   **API Gateway:** Nginx is used as an API gateway, with configuration in the `emartapp/nginx` directory.
*   **Deployment:** The application is designed to be deployed using Docker and Kubernetes. Docker files are in the `emartapp` directory, and Helm charts are in the `emartapp/kkartchart` directory.

### Getting Started

To get started with development, you will need to have the following installed:

*   Node.js and npm
*   Angular CLI
*   Java and Maven
*   Docker

To run the application locally, you can use the `docker-compose.yaml` file in the `emartapp` directory.

### Building and Running

Each service can be built and run independently.

*   **Frontend:**
    *   To install dependencies, run `npm install` in the `emartapp/client` directory.
    *   To start the development server, run `ng serve` in the `emartapp/client` directory.
*   **Java API:**
    *   To build the application, run `mvn clean install` in the `emartapp/javaapi` directory.
*   **Node.js API:**
    *   To install dependencies, run `npm install` in the `emartapp/nodeapi` directory.
    *   To start the server, run `npm start` in the `emartapp/nodeapi` directory.

### Deployment

The application can be deployed using the Helm charts in the `emartapp/kkartchart` directory. You will need to have a Kubernetes cluster set up and `helm` installed.

To deploy the application, run the following command from the `emartapp/kkartchart` directory:
helm install <release-name> .

This will deploy all the services to your Kubernetes cluster. You can customize the deployment by modifying the `values.yaml` files in the `emartapp/kkartchart` directory.