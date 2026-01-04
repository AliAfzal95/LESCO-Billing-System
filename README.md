# LESCO Billing System

A comprehensive console-based C++ application designed to manage electricity billing operations for the Lahore Electric Supply Company (LESCO). This system simulates real-world utility management features, including customer registration, tariff management, and automated bill calculation for different meter types.

## 🚀 Features

### 👨‍💼 Employee (Admin) Portal
*   **Secure Authentication**: Login system for employees.
*   **Customer Management**: Register new customers with specific meter types (1-Phase/3-Phase) and customer types (Domestic/Commercial).
*   **Billing Operations**:
    *   Update bill status (Paid/Unpaid).
    *   View detailed customer information.
    *   Generate reports on paid vs. unpaid bills.
*   **Tariff Control**: Update tax rates, fixed charges, and unit prices for different meter categories.
*   **Account Management**: Update employee passwords.

### 👤 Customer Portal
*   **Easy Access**: Login using Customer ID and Date of Birth.
*   **Bill Viewing**: View detailed current bill including electricity cost, tax, and due dates.

## ⚙️ Technical Architecture

The project is built using **Object-Oriented Programming (OOP)** principles in C++:

*   **Polymorphism**: Handles different billing logic for **1-Phase** and **3-Phase** meters using a base `Billing` class and a derived `phase3Meter` class.
*   **File Handling**: Uses custom file I/O to persist data for customers, employees, billing records, and tariffs.
*   **Dynamic Memory Management**: Utilizes pointers and manual memory allocation/deallocation for efficient resource management.

### Class Structure
*   **`LESCO`**: The main controller class managing the system flow.
*   **`Customer`**: Manages customer personal data and connection details.
*   **`Employee`**: Handles admin functionalities and security.
*   **`Billing`**: Base class for standard billing calculations.
*   **`phase3Meter`**: Derived class for complex 3-Phase meter calculations (Peak/Regular units).
*   **`Tarrif`**: Manages tax rates and pricing configurations.

## 📂 Data Files

The system relies on the following text files for data persistence:
*   `EmployeesData.txt`: Stores employee credentials.
*   `CustomerInfo.txt`: Contains customer records.
*   `BillingInfo.txt`: Stores generated billing data.
*   `TarrifTaxInfo.txt`: Configurable file for unit prices and tax percentages.

## 🛠️ Getting Started

### Prerequisites
*   Visual Studio (2019/2022 recommended) or any C++ compiler supporting C++11 or later.

### Installation
1.  Clone the repository:
    ```bash
    git clone https://github.com/AliAfzal95/LESCO-Billing-System.git
    ```
2.  Open the solution file (`.sln`) in Visual Studio.
3.  Ensure all `.txt` files are located in the project's working directory.
4.  Build and Run the project.

## 📖 Usage

1.  **Launch the Application**: You will be presented with a login screen.
2.  **Select Role**: Choose between Employee or Customer.
3.  **Employee Login**: Enter valid Employee ID and Password.
4.  **Customer Login**: Enter Customer ID. The password is the customer's Date of Birth (Format: YYYYMMDD).
