
Valuify - Personal Finance Tracker
A premium, CRED-style personal finance app built with Flutter.


## ✨ Features

- 🔐 Authentication (Email/Password + Google Sign-In)
- 💰 Dashboard with animated balance cards
- 📊 Interactive charts (3-month trend, category pie chart)
- 💳 Transaction management (CRUD with receipt photos)
- 🏷️ Custom categories with icons and colors
- 💵 Monthly budgets with progress tracking
- 📈 Reports (CSV export, PDF generation)
- 💸 **UPI Wallet & Mock Payments** (NEW!)
  - Mock wallet with starting balance
  - Send/receive money via UPI
  - Transaction history
  - Real-time balance updates
- ⚙️ Settings (currency, theme, biometric lock)

## Setup Instructions

### Prerequisites

1. Install Flutter SDK (3.x or higher)
2. Install Android Studio / Xcode
3. Set up Firebase project

### Firebase Setup

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Create a new project named "Valuify"
3. Enable the following services:
   - Authentication (Email/Password + Google)
   - Cloud Firestore
   - Firebase Storage

4. **For Android:**
   - Download `google-services.json`
   - Place it in `android/app/`

5. **For iOS:**
   - Download `GoogleService-Info.plist`
   - Place it in `ios/Runner/`

### Installation

```bash
# Clone the repository
git clone https://github.com/skulllord/Valuify.git
cd Valuify

# Install dependencies
flutter pub get

# Run the app
flutter run
```

### Build APK

```bash
# Debug APK
flutter build apk --debug

# Release APK
flutter build apk --release

# APK location: build/app/outputs/flutter-apk/
```

## Project Structure

```
lib/
├── main.dart
├── screens/
│   ├── auth/
│   │   ├── login_screen.dart
│   │   └── register_screen.dart
│   ├── dashboard/
│   │   └── dashboard_screen.dart
│   ├── transactions/
│   │   ├── transactions_screen.dart
│   │   └── add_transaction_screen.dart
│   ├── categories/
│   │   └── categories_screen.dart
│   ├── budgets/
│   │   └── budgets_screen.dart
│   ├── reports/
│   │   └── reports_screen.dart
│   └── settings/
│       └── settings_screen.dart
├── widgets/
│   ├── balance_card.dart
│   ├── transaction_item.dart
│   ├── category_icon.dart
│   └── chart_widgets.dart
├── models/
│   ├── user_model.dart
│   ├── transaction_model.dart
│   ├── category_model.dart
│   └── budget_model.dart
├── services/
│   ├── auth_service.dart
│   ├── firestore_service.dart
│   ├── storage_service.dart
│   └── pdf_service.dart
├── providers/
│   ├── auth_provider.dart
│   ├── transaction_provider.dart
│   ├── category_provider.dart
│   ├── budget_provider.dart
│   └── theme_provider.dart
└── utils/
    ├── constants.dart
    ├── colors.dart
    └── helpers.dart
```

## Firestore Structure

```
users/{userId}
  ├── accounts/{accountId}
  ├── categories/{categoryId}
  ├── transactions/{txnId}
  ├── budgets/{budgetId}
  └── settings
```

## Tech Stack

- **Framework:** Flutter 3.x
- **State Management:** Riverpod
- **Backend:** Firebase (Auth, Firestore, Storage)
- **Charts:** FL Chart
- **Authentication:** Firebase Auth + Google Sign-In

## 📱 Screenshots

<img width="937" height="847" alt="add-transaction" src="https://github.com/user-attachments/assets/b02e7143-b516-4822-a75f-18d6515474e0" />
<img width="916" height="860" alt="budgets" src="https://github.com/user-attachments/assets/7bee910b-372c-4468-901a-3e8aed5011ae" />
<img width="925" height="852" alt="dashboard" src="https://github.com/user-attachments/assets/492683f8-285f-41e4-aeb9-38243d89e60f" />
<img width="534" height="495" alt="Screenshot 2026-04-06 110730" src="https://github.com/user-attachments/assets/f6024567-3187-4609-837b-fe25df3e5d59" />

