# expense-tracker-cli
# 💸 Expense Tracker CLI

A lightweight command-line tool to track your daily expenses, categorize spending, and generate monthly summaries — all from your terminal.

## 🚀 Features

- Add, view, and delete expense entries
- Categorize expenses (Food, Transport, Utilities, Entertainment, etc.)
- Filter expenses by date range or category
- Monthly/weekly spending summaries
- Export data to CSV
- Persistent storage using a local JSON file

## 🛠 Tech Stack

- **Language:** Python 3.10+
- **Libraries:** `argparse`, `json`, `datetime`, `tabulate`, `colorama`
- **Storage:** Local JSON file (`data/expenses.json`)

## 📦 Setup & Installation

### Prerequisites
- Python 3.10 or higher
- pip

### Steps

```bash
# Clone the repository
git clone https://github.com/yourusername/expense-tracker-cli.git
cd expense-tracker-cli

# Install dependencies
pip install -r requirements.txt

# Run the app
python main.py --help
```

## 🧪 Usage

```bash
# Add an expense
python main.py add --amount 250 --category Food --note "Lunch at cafe"

# View all expenses
python main.py list

# View expenses for a specific month
python main.py list --month 2026-03

# View summary
python main.py summary

# Delete an entry by ID
python main.py delete --id 5

# Export to CSV
python main.py export --output expenses.csv
```

## 📁 Project Structure

```
expense-tracker-cli/
├── main.py               # Entry point & CLI argument parser
├── tracker.py            # Core logic (add, delete, filter)
├── storage.py            # JSON read/write operations
├── visualizer.py         # Summary and table rendering
├── data/
│   └── expenses.json     # Local data store
├── requirements.txt
└── README.md
```

## 📊 Sample Output

```
+----+------------+----------+-----------+------------------+
| ID |    Date    | Category |   Amount  |       Note       |
+----+------------+----------+-----------+------------------+
|  1 | 2026-03-01 |   Food   |  PKR 250  |  Lunch at cafe   |
|  2 | 2026-03-02 | Transport|  PKR 100  |  Uber to uni     |
|  3 | 2026-03-03 | Utilities|  PKR 1200 |  Electricity bill|
+----+------------+----------+-----------+------------------+
Total: PKR 1550
```

## 🔧 Configuration

You can edit `config.json` to change the default currency symbol and date format:

```json
{
  "currency": "PKR",
  "date_format": "%Y-%m-%d",
  "data_file": "data/expenses.json"
}
```

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first.

## 📄 License

[MIT](LICENSE)
