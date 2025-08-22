# Smart Expense Tracker (Microservices with Azure)

Concept:
A cloud-based system that helps users upload receipts, categorize expenses, and generate monthly reports.

Microservices (Azure Functions):
	•	Receipt Upload Service (HTTP-triggered function) → saves receipt metadata to Azure Blob Storage.
	•	Expense Parser Service (Queue-triggered function) → extracts data from receipts (simulate OCR via a library or API).
	•	Categorization Service (Event Grid-triggered function) → classifies expenses into categories (Food, Travel, etc.).
	•	Reporting Service (Timer-triggered function) → aggregates data from Azure SQL / Cosmos DB and emails a monthly report.

Tech stack:
	•	Backend: Azure Functions (C#)
	•	Data: Azure SQL (structured expenses), Cosmos DB (NoSQL for unstructured receipt data)
	•	Storage: Azure Blob Storage
	•	Messaging: Azure Queue + Event Grid
	•	Frontend (Optional): React dashboard to visualize expense trends
