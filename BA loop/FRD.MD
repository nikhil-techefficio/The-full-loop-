# 1. 👑 USER ROLES & PERMISSIONS
   -- Owner
      Full system access
      View analytics, reports
      Manage users, warehouses, products
   -- Warehouse Admin
      Manage inventory (inflow/outflow)
      Generate barcodes
      Manage staff under warehouse
   -- Warehouse Helper (Mobile Only)
      Scan barcode
      View storage location
   -- Inventory Sales Helper
      Pick items via scanning
      Add to cart
   -- Billing Admin
      Verify cart
      Process billing
   -- Handle failed payments
      If failed return to inventory
      Else remove from inventory 

# 2. 📦 INVENTORY MANAGEMENT
   -- Functional Requirements:
      System must allow adding new products
   -- Each product must have:
      Name
      SKU
      Warehouse ID
      Quantity
      Rack location
   -- System must update stock on:
      Product addition
      Sale
      Return(In terms of payment failure)

# 3. 🔖 BARCODE SYSTEM
   -- Requirements:
      Generate unique barcode for each product batch
      Barcode must store:
      Product ID
      Rack location
      Date of arrival
      Status (Available / Booked / Sold)
      System must support:
      Barcode scanning (mobile)

# 4. 📊 INVENTORY ALERT SYSTEM
   -- Rules:
      Low stock → 25%
      Medium → 45%
      Critical → 15%
   -- Dead stock → No sale for 30 days
   -- System Behavior:
      Trigger alerts based on thresholds
      Display alerts in dashboard

# 5. 🛒 ORDER PROCESSING
   -- Flow:
      Order received
      Sales helper scans items
      Items added to cart
   -- Requirements:
      System must validate stock availability
      System must lock stock once added to cart

# 6. 💳 BILLING SYSTEM
   -- Requirements:
      Billing admin verifies cart
      Generates invoice
      Processes payment
   -- Conditions:
      If payment success:
   -- Deduct stock
      Mark as sold
   -- If payment fails:
      Return items to inventory

# 7. 🔄 STOCK TRANSFER (WAREHOUSE TO WAREHOUSE)
   -- Requirements:
      Admin can initiate transfer
   -- System must:
      Deduct from source
      Add to destination
      Track transfer history

# 8. 📈 REPORTING & ANALYTICS
   -- Reports:
      Sales (daily/monthly/yearly)
   -- Product performance:
      Fast-moving
      Slow-moving
   -- Warehouse-wise performance
   -- Profit/margin analysis

# 9. ⏱️ USER ACTIVITY TRACKING
   -- Track login/logout
   -- Track working hours
   -- Track actions performed

# 10. 🔐 SECURITY REQUIREMENTS
  -- Role-based access control
  -- Secure authentication 
  -- Data validation
  -- Session management

# 11. 📱 MOBILE REQUIREMENTS
  -- Barcode scanning support
  -- Lightweight UI
  -- Fast response time