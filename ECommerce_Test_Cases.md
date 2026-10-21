# 🧪 Functional Test Case Suite - E-Commerce Checkout & Authentication

**Module:** User Authentication & Shopping Cart Checkout  
**Testing Type:** Functional, Positive/Negative, Boundary Value  
**Author:** Sahejpreet Singh  

---

## 📋 Test Case Execution Matrix

| Test Case ID | Requirement / Feature | Test Scenario Description | Expected Result | Status |
| :--- | :--- | :--- | :--- | :--- |
| **TC_AUTH_01** | User Login | Verify login with valid registered email and correct password. | User is successfully authenticated and redirected to the user dashboard. | **Pass** |
| **TC_AUTH_02** | User Login | Verify login with an unregistered email address. | Error banner displays: *"Account not found. Please sign up."* | **Pass** |
| **TC_AUTH_03** | User Login | Verify password masking feature on the password text input field. | Characters entered in the password field are masked securely (hidden). | **Pass** |
| **TC_CART_01** | Add to Cart | Click "Add to Cart" on a Product Detail Page (PDP) with available stock. | Item count badge in the header increments by 1; success toast notification appears. | **Pass** |
| **TC_CART_02** | Cart Quantity | Attempt to increase product quantity beyond available inventory stock limit. | Quantity selector caps at max stock limit; inline warning displays: *"Maximum available stock reached"*. | **Pass** |
| **TC_CHECK_01** | Shipping Address | Proceed to checkout with blank mandatory shipping address fields. | Form validation triggers error highlights on mandatory fields; "Continue" is blocked. | **Pass** |
| **TC_CHECK_02** | Payment Gateway | Select "Cash on Delivery" and complete order placement. | Order is successfully generated, inventory is updated, and confirmation page renders with an Order ID. | **Pass** |
| **TC_CHECK_03** | Payment Gateway | Simulate payment failure response from third-party gateway (Stripe/Razorpay). | Transaction fails gracefully; error message prompts user to retry or use an alternate payment method. | **Pass** |

---

## 🔍 Detailed Test Scenario Breakdown: Checkout Flow

### **Test ID:** `TC_CHECK_02` (Cash on Delivery Order Flow)
* **Pre-requisites:** User is logged in, has a valid item in the cart, and has a saved delivery address.
* **Test Steps:**
  1. Navigate to Cart and click **Proceed to Checkout**.
  2. Verify pre-populated shipping address details.
  3. Select **Cash on Delivery** under payment options.
  4. Click **Place Order**.
* **Post-Conditions:** Database creates a new order entry with status set to `Pending Fulfillment`.
