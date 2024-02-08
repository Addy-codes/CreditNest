
# CreditNest

CreditNest is a credit approval system designed to streamline the process of loan approvals by utilizing past transactional data and predicting future transactions. Our system leverages a robust tech stack including Django, Celery, Redis, and Docker to ensure efficient and reliable service.

## Getting Started

To get the CreditNest system up and running on your local machine, follow the steps below:

### Prerequisites

- Docker
- Docker Compose

### Installation

1. Clone the repository to your local machine.
2. Navigate to the project directory.
3. Run the following command to build and start the containers:

```shell
docker-compose up --build
```

### Initial Setup

Once the containers are up and running, you need to populate the database with the initial data:

1. Open your web browser.
2. Go to `http://localhost:8000/fill-data` to ingest the xlsx data into the PostgreSQL database.

## API Endpoints

CreditNest provides several endpoints for managing users, loans, and checking eligibility:

- `fill-data/`: Ingest xlsx data into the database. Run this initially.
- `register/`: Register a new user.
- `check-eligibility/`: Check if a customer is eligible for a loan.
- `create-loan/`: Create a new loan for a customer.
- `view-loan/<int:loan_id>/`: Retrieve information about a specific loan.
- `view-loans/<int:customer_id>`: View all loans associated with a customer.

## Usage

After completing the initial setup, you can start using the system by registering a user and then proceeding to check loan eligibility, create loans, and view loan information as required.