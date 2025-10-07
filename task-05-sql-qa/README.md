# SQL Q&A System (Banking Data)
### Objective
Enable natural language queries on structured customer and transaction data.
### Database Schema:

- customers(id, name, account_type, balance, risk_profile)

- transactions(id, customer_id, type, amount, date, branch)

- clients(client_id, name, age, risk_profile, portfolio_value)

- investments(investment_id, client_id, fund_name, amount_invested, date)

### Implementation Steps:

- Create SQLite database and populate ≥30 sample rows per table.

- Use LangChain SQLDatabaseChain to translate natural queries to SQL.

- Execute query and return readable output.

- Use prompt templates for safe query construction.

### Example Query:

- “Show all customers with balance > ₹5L and more than 3 transactions this month.”

Code Example:
<img width="1034" height="330" alt="task5_code1" src="https://github.com/user-attachments/assets/b8b7bc5c-b629-4f0b-add6-dc224d8c0791" />

Sample Output:
<img width="1198" height="618" alt="task5_output" src="https://github.com/user-attachments/assets/03d7376e-93b4-4636-9039-4d4008749359" />

