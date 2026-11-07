routers/reports.py

Line 103: Variable v possibly undefined
Line 116: Variable start possibly undefined
Line 165: Variable start possibly undefined
Fix: Ensure variables are initialized before all code paths. Add default values or restructure conditional logic to guarantee assignment.
models/product.py

Line 22: Variable t possibly undefined
Fix: Initialize t with a default value or ensure all conditional branches assign a value.
React: Missing Hook Dependencies
Why it matters: Missing dependencies cause stale closures, leading to bugs where components use outdated values and don't re-render when they should.

src/components/pos/ReceiptModal.tsx:89 in ReceiptModal()

Missing: c, customer_id, formatPhone, and 5 more dependencies
Fix: Add all missing dependencies to the useEffect dependency array, or use refs for values that shouldn't trigger re-renders.
src/components/pos/ScannerDialog.tsx:28 in anonymous function

Missing: BrowserMultiFormatReader, DOMException, IScannerControls, and 17 more
Fix: Review if these should trigger effect re-runs. Consider extracting stable references or using useCallback for functions.
src/pages/Kasir.tsx:43 in useMemo

Missing: items, okCat, okQ, and 3 more
Fix: Add all dependencies that are used in the memo computation to prevent stale cached values.
src/pages/Stok.tsx:117 in useMemo

Missing: okCat, okQ, p, and 1 more
Fix: Include all variables used in the memoization calculation.
Additional files with missing dependencies: src/components/stock/RestockModal.tsx:45, src/components/stock/ProductModal.tsx:76, src/components/stock/LabelPrintModal.tsx:31, src/components/stock/LabelPrintModal.tsx:39, src/components/stock/Barcode.tsx:7, src/components/ledger/EntryModal.tsx:41, src/components/layout/Navbar.tsx:25, src/components/layout/ChangePinModal.tsx:31

Important
Python: High Complexity Functions
Why it matters: Complex functions are hard to test, maintain, and prone to bugs.

routers/transactions.py:20 - create_transaction()

Complexity: 23, Length: 88 lines, 16 local variables
Fix: Break into smaller functions: separate validation, stock checks, transaction creation, and ledger updates. Extract helper functions for each concern.
routers/reports.py:196 - export_excel()

Complexity: 17, Length: 80 lines, 22 local variables
Fix: Extract Excel formatting logic into separate functions. Create helper methods for each worksheet generation.
routers/reports.py:23 - compute_profit()

Complexity: 14, Length: 81 lines
Fix: Break down profit calculation logic into smaller, focused functions for each calculation step.
routers/store.py:265 - closing_today()

Complexity: 12
Fix: Extract closing validation and calculation logic into separate helper functions.
React: Extremely High Complexity Components
Why it matters: These components are unmaintainable, hard to test, and likely have performance issues.

src/components/pos/CartPanel.tsx:39 - CartPanel()

Critical: Complexity: 43, Length: 373 lines
Fix: Split into smaller components: CartItems, CartSummary, CartActions, PaymentPanel. Move business logic to custom hooks.
src/components/pos/ReceiptModal.tsx:70 - ReceiptModal()

Critical: Complexity: 31, Length: 305 lines
Fix: Extract ReceiptHeader, ReceiptItems, ReceiptFooter components. Move WhatsApp formatting logic to a utility function.
src/components/stock/ProductModal.tsx:62 - ProductModal()

Complexity: 24, Length: 326 lines
Fix: Separate form sections into ProductBasicInfo, ProductPricing, ProductInventory components. Extract form validation logic.
src/components/layout/ClosingDialog.tsx:32 - ClosingDialog()

Complexity: 24, Length: 118 lines
Fix: Split into ClosingSummary and ClosingForm components. Extract calculation logic to utility functions.
React: Array Index as Key
Why it matters: Using index as key causes React to lose track of component identity, leading to state bugs and poor performance during re-renders.

Fix for all: Use stable unique identifiers (IDs) instead of array indices.

src/pages/Stok.tsx:233
src/pages/Riwayat.tsx:86
src/pages/Pembukuan.tsx:199
src/pages/Pelanggan.tsx:317
src/pages/Login.tsx:104
src/pages/Laba.tsx:202
src/pages/Kasir.tsx:199
src/components/stock/ProductModal.tsx:330
Python: Incorrect Comparison Operators
Why it matters: Using is instead of == for constants can cause unexpected behavior since is checks object identity, not value equality.

Fix for all: Replace is with == when comparing values.

routers/transactions.py:38
routers/reports.py:162
routers/products.py:46
routers/auth.py:75
models/product.py:17
lib/auth.py:18
tests/test_tscheck_riwayat_void.py:45
tests/test_tscheck_login_pin.py:15
React: Component Size Recommendations
Why it matters: Large files are harder to navigate, test, and maintain.

src/pages/Stok.tsx - 305 lines, 39 imports

Fix: Extract filtering logic to custom hook, split table rendering into separate component.
Missing TypeScript coverage in critical files:

src/components/layout/Navbar.tsx (0%), src/pages/Riwayat.tsx (3.7%), src/components/pos/CartPanel.tsx (5.4%)
Fix: Add TypeScript types for props, state, and function parameters to prevent type-related bugs.
