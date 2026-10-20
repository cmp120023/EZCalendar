# EZCalendar

# Mechanic Shop Management & Tracking System

A robust **ASP.NET Core MVC** web application designed for automotive repair shops to track clients, manage vehicle data, monitor parts inventory, optimize manufacturer ordering, and visualize shop floor operations in real-time.

---

## 🚀 Core Features

### 1. Client & Vehicle Management
* **Client Profiles:** Tracks first name, last name, phone number, and email.
* **Vehicle Profiles:** Detailed tracking per client including color, year, make, and model.
* **Appointments & Estimations:** Schedules appointment dates/times and logs repair or service cost estimations.

### 2. Inventory & Manufacturer Integration
* **Stock Inventory:** Keeps a live count of available parts and shop supplies.
* **Manufacturer Directory:** Stores pricing structures, primary contact details, and direct hyperlinks to online parts ordering portals.

### 3. Dynamic Operations Dashboard (UI)
* **Lot Tracker:** Displays vehicles currently parked in the shop's lot.
* **Active Bays:** Monitors vehicles currently being worked on by technicians.
* **Mobile Dispatch:** Tracks if and where the mobile service unit has been deployed.

---

## 🛠️ Tech Stack

* **Framework:** ASP.NET Core MVC (v8.0+)
* **Database:** Entity Framework Core (SQL Server / PostgreSQL)
* **Frontend:** Razor Views, Bootstrap, JavaScript (SignalR recommended for live dashboard updates)

---

## 📂 Project Structure

```text
├── Controllers/
│   ├── ClientController.cs       # Handles clients, vehicles, and appointments
│   ├── InventoryController.cs    # Manages parts, manufacturer data, and links
│   └── DashboardController.cs    # Powers the live shop floor and mobile tracking UI
├── Models/
│   ├── Client.cs
│   ├── Vehicle.cs
│   ├── Appointment.cs
│   ├── InventoryItem.cs
│   └── Manufacturer.cs
├── Views/
│   ├── Client/
│   ├── Inventory/
│   └── Dashboard/               # The interactive live status interface
└── Data/
    └── ApplicationDbContext.cs
```

---

## ⚙️ Getting Started

### Prerequisites
* [.NET SDK](https://microsoft.com) (Latest LTS version)
* [Visual Studio 2022](https://microsoft.com) or [VS Code](https://visualstudio.com)
* SQL Server instance (or localDB)

### Local Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd mechanic-shop-tracker
   ```

2. **Configure Connection String:**
   Update the connection string in `appsettings.json` to point to your local database instance:
   ```json
   "ConnectionStrings": {
     "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=MechanicShopDb;Trusted_Connection=True;MultipleActiveResultSets=true"
   }
   ```

3. **Run Database Migrations:**
   Open the Package Manager Console or terminal and run:
   ```bash
   dotnet ef database update
   ```

4. **Launch the Application:**
   ```bash
   dotnet run
   ```
   Open your browser and navigate to `https://localhost:5001` or `http://localhost:5000`.
