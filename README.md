```
# 🌾 Milarie Accounting Software

An open-source, lightweight double-entry accounting ledger tailored specifically for farmers, agricultural enthusiasts, and agribusiness startups. Built on the modern **TALL Stack** (Tailwind CSS, Alpine.js, Laravel, and Livewire), this system provides a decentralized, free alternative to expensive proprietary accounting software.

It empowers agricultural producers to track their physical assets, biological transformations (livestock growth, crop progression), and seasonal operational expenses without friction.

---

## 🚀 Key Features

* **Double-Entry General Ledger:** Built natively around fundamental accounting rules (Debits/Credits) to ensure mathematically sound trial balances.
* **Agricultural Chart of Accounts:** Pre-configured database structures tailored specifically for farm environments:
  * **Biological Assets:** Tracking for Market Livestock, Breeding/Bearer Livestock, Growing Crops, and Bearer Plants.
  * **Inventories:** Dedicated accounts for Feed, Harvested Crops, and Farm Supplies.
  * **Production Expenses:** Clean buckets for Fertilizer, Seed/Seedlings, Crop Protection Chemicals, and Veterinary Care.
* **Livewire Reactive UI:** Post operational transactions, track current multi-category account balances, and audit general ledger entries in real time without refreshing pages.
* **Zero Configuration Seeders:** Populate a standardized, production-ready agricultural chart of accounts immediately upon deployment.

---

## 🛠️ Technical Stack

* **Framework:** Laravel (v11.x+)
* **Frontend Logic:** Livewire (v3.x) & Alpine.js
* **Styling UI:** Tailwind CSS
* **Database Engine:** MySQL / PostgreSQL / SQLite

---

## 📦 Project Architecture (A, B, C Model)

The core application follows a clean, decoupled three-part implementation strategy:

### Part A: Database Schema
Consists of optimization structures managing long-term indices:
* `accounts`: Manages structural nodes across five main financial categories (`asset`, `liability`, `equity`, `revenue`, `expense`).
* `ledger_entries`: Stores granular itemized transaction histories maintaining perfect cross-entity debit/credit parity.

### Part B: Livewire Component Engine (`app/Livewire/SimpleLedger.php`)
Manages state synchronization, transactional form validations (`account_id`, `amount`, `transaction_date`), database ingestion protocols, and automated flash messaging hooks.

### Part C: Blade View Template (`resources/views/livewire/simple-ledger.blade.php`)
An interactive, responsive dashboard engineered with clean utility styling divided into:
1. Transaction Entry Form
2. Running Balance Portfolio Matrix
3. Chronological General Ledger Audit Log

---

## ⚙️ Installation & Setup

Follow these sequential steps to assemble the ledger locally:

### 1. Clone & Install Dependencies
```bash
git clone [https://github.com/yourusername/agribalance-ledger.git](https://github.com/yourusername/agribalance-ledger.git)
cd agribalance-ledger
composer install
npm install && npm run build

```

### 2. Environment Configuration

Copy the example environment file and configure your database settings:

```bash
cp .env.example .env
php artisan key:generate

```

> 💡 **Tip:** Open your `.env` file and update the `DB_DATABASE`, `DB_USERNAME`, and `DB_PASSWORD` fields to match your local database environment.

### 3. Database Migrations & Seeders

Run the migrations along with the zero-configuration seeders to instantly build your agricultural chart of accounts:

```bash
php artisan migrate --seed

```

### 4. Launch the Application

Start your local development server:

```bash
php artisan serve

```

You can now access the application by navigating to `http://127.0.0.1:8000` in your web browser.

---

## 📝 License

This project is open-source software licensed under the [MIT License](https://www.google.com/search?q=LICENSE).

```

```