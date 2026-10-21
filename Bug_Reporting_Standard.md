## 📋 Standard Bug Report Structure

| Field | Description |
| :--- | :--- |
| **Bug ID** | Unique identifier for tracking (e.g., `BUG-001`) |
| **Summary / Title** | Concise description stating *What*, *Where*, and *Under what condition* |
| **Module / Feature** | Functional area affected (e.g., Checkout, User Auth, Search, API) |
| **Severity** | Impact on software functionality (`Blocker` / `Critical` / `Major` / `Minor`) |
| **Priority** | Urgency for business/fix (`P0 - Immediate` / `P1 - High` / `P2 - Medium` / `P3 - Low`) |
| **Environment** | OS, Device, Browser version, App Build version |
| **Pre-requisites** | Setup required before executing the test steps |
| **Steps to Reproduce** | Clear, numbered, step-by-step instructions |
| **Expected Result** | Intended behavior according to specifications |
| **Actual Result** | Observed incorrect behavior |
| **Attachments / Logs** | Screenshots, screen recordings, network logs, console errors |

---

## 🛠️ Real-World Sample Defect Reports

### Sample Bug 1: E-Commerce Payment Gateway Failure
* **Bug ID:** `ECOMM-102`
* **Summary:** Infinite loading spinner and JS error on selecting "Cash on Delivery" during checkout on mobile responsive viewport.
* **Module:** E-Commerce / Checkout Flow
* **Severity:** Critical | **Priority:** P1 - High
* **Environment:** Web / Chrome 120.0 / Windows 11 (Viewport: 375x812 - Mobile Emulator)
* **Pre-requisites:**
  1. User is authenticated with a verified delivery address.
  2. Cart contains at least one in-stock item.

#### Steps to Reproduce:
1. Navigate to the Cart and click **Proceed to Checkout**.
2. Complete shipping address selection and click **Continue to Payment**.
3. Select the **Cash on Delivery (COD)** payment radio option.
4. Click the **Place Order** button.

#### Expected Result:
The order is created successfully in the database, and the user is redirected to the `/order-confirmation` page displaying a valid Order ID.

#### Actual Result:
The "Place Order" button enters a frozen loading state. No confirmation page renders, and no order record is generated in the backend.

#### Attachments / Developer Logs:
* **Browser Console Log:**
  ```text
  Uncaught (in promise) TypeError: Cannot read properties of undefined (reading 'cod_status')
      at checkout.js:248:19
