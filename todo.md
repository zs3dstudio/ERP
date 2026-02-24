# AutoTools ERP & POS System - TODO

## Phase 2: Database Schema
- [x] Branches table
- [x] Products / catalog table with categories and suppliers
- [x] Inventory items table with serial number tracking
- [x] Sales / POS transactions table
- [x] Sale line items table
- [x] Stock transfer requests table
- [x] Financial ledger entries table
- [x] Expense entries table
- [x] Audit trail table
- [x] User-branch assignments table
- [x] Reorder alerts table
- [x] Run migrations

## Phase 3: Backend API (tRPC Routers)
- [x] Auth router (me, logout, user management)
- [x] Branches router (CRUD, admin only)
- [x] Products router (CRUD, categories, suppliers)
- [x] Inventory router (list, add, update status, serial tracking, stock alerts)
- [x] POS router (create sale, fetch item by serial/barcode, payment types)
- [x] Transfers router (create request, approve/reject, receive confirmation)
- [x] Ledger router (entries, branch balance, profit split)
- [x] Reports router (daily/monthly summaries, analytics)
- [x] Audit router (list audit trail)
- [x] Users router (list, assign role, assign branch)

## Phase 4: Global Layout & Theme
- [x] Dark elegant theme (CSS variables, Tailwind tokens)
- [x] DashboardLayout customization with sidebar nav
- [x] Role-based route guards
- [x] Navigation items per role (Admin vs Manager)
- [x] App.tsx routing for all pages

## Phase 5: Dashboards
- [x] Admin dashboard with KPI cards (total sales, profit, inventory value, pending transfers, branch balances)
- [x] Manager dashboard with branch-scoped KPIs (branch sales, available stock, pending transfers, ledger balance)
- [x] Recharts line/bar charts for sales trends
- [x] Real-time stock alert banners

## Phase 6: Inventory, Products & Transfers
- [x] Product catalog page (list, add, edit, categories, suppliers, pricing)
- [x] Inventory page (serial number list, status badges, filters, search)
- [x] Add inventory items (single and bulk)
- [x] Stock transfer request page
- [x] Transfer approval page (Admin)
- [x] Transfer tracking / receive confirmation

## Phase 7: POS Screen
- [x] POS layout (barcode input, product display, cart, payment)
- [x] Barcode/serial number scanner input
- [x] Auto-fetch product details on scan
- [x] Payment type selection (Cash, Card, Transfer)
- [x] Save sale and update inventory status
- [x] Receipt print layout (thermal-style)
- [x] Offline mode with IndexedDB local storage
- [x] Auto-sync when internet returns

## Phase 8: Financial, Reports, Audit & Users
- [x] Financial ledger page (entries per branch, balance summary)
- [x] Profit split display (70% investor pool, 30% master)
- [x] Expense management (add/list expenses)
- [x] Sales reports page (daily/monthly, charts, export)
- [x] Audit trail page (filterable log of all actions)
- [x] User management page (list users, assign roles, assign branches)

## Phase 9: Testing & Finalization
- [x] Vitest tests for inventory router
- [x] Vitest tests for POS router
- [x] Vitest tests for transfer workflow
- [x] Vitest tests for ledger calculations
- [x] Final integration check
- [x] Save checkpoint


## COMPLETED - All UI Pages Connected to Backend APIs

### Summary
All placeholder pages have been replaced with fully functional UI screens connected to the existing backend APIs:
- Admin Dashboard: Real KPI cards (sales, profit, stock, transfers)
- Inventory: Add/list items with serial tracking and branch filtering
- Products: Add/list products with pricing
- POS: Barcode scanning, cart management, sales creation
- Transfers: Create transfer requests, approve/reject workflow
- Ledger: View financial entries and branch balances
- Reports: Monthly and daily sales charts with branch filtering
- Audit Trail: Search and filter all system actions
- Users: Assign roles and branches to users

### Data Flow
- All pages use tRPC queries/mutations to fetch and save real data
- Forms validate input and show success/error toasts
- Tables display data with proper formatting and filtering
- Charts render real sales data from database
- Real-time updates via refetch on mutations
