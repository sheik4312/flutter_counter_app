# 🚀 Flutter Counter App

A professional **Flutter application** featuring **Firebase Authentication** and a **counter functionality** — built using **Riverpod** for state management.  
This project showcases **clean architecture**, **best practices**, and **modern Flutter development** techniques.

![Flutter](https://img.shields.io/badge/Flutter-3.19+-02569B?style=for-the-badge&logo=flutter)
![Dart](https://img.shields.io/badge/Dart-2.19+-0175C2?style=for-the-badge&logo=dart)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![Riverpod](https://img.shields.io/badge/Riverpod-State_Management-4B32C3?style=for-the-badge)

---

## ✨ Features

### 🔐 Authentication
- ✅ User Registration & Login  
- ✅ Firebase Authentication  
- ✅ Password Reset Functionality  
- ✅ Form Validation  
- ✅ Error Handling with Snackbars  

### 🔢 Counter Functionality
- ✅ Increment Counter (+1)  
- ✅ Decrement Counter (-1)  
- ✅ Reset Counter (0)  
- ✅ Real-time State Management  

### ⚙️ Technical Excellence
- ✅ 100% Riverpod State Management  
- ✅ Clean Architecture  
- ✅ Responsive UI Design  
- ✅ Loading States  
- ✅ Professional Error Handling  

---

## 📸 Screenshots

| Login Screen | Signup Screen | Home Screen |
|--------------|---------------|-------------|
| <img width="1080" height="2400" alt="Screenshot_1762603591" src="https://github.com/user-attachments/assets/c665d667-26ed-44a1-819b-c43f8e1062a4" /> | <img width="1080" height="2400" alt="Screenshot_1762603601" src="https://github.com/user-attachments/assets/fbc3fcf2-6e96-434b-91ae-2ade9ff0b74d" /> | <img width="1080" height="2400" alt="Screenshot_1762603635" src="https://github.com/user-attachments/assets/99bce72f-019c-4dc2-b5f5-264e19aa3c86" />|




---

## 🛠️ Tech Stack

- **Framework:** Flutter 3.19+  
- **Language:** Dart 2.19+  
- **State Management:** Riverpod  
- **Backend:** Firebase Authentication  
- **Architecture:** Clean Architecture with StateNotifier  

---

## 📁 Project Structure

```
flutter_counter_app/
├── lib/
│   ├── main.dart
│   ├── loginpage.dart
│   ├── signup.dart
│   ├── homepage.dart
│   └── providers/
│       ├── auth_controller.dart
│       └── auth_state.dart
├── firebase_options.dart
└── pubspec.yaml
```

---

## 🏗️ Architecture

### 🧠 State Management with Riverpod

```dart
// Auth State Management
final authControllerProvider = StateNotifierProvider<AuthController, AuthState>((ref) => AuthController());
final authStateChangesProvider = StreamProvider<User?>((ref) => FirebaseAuth.instance.authStateChanges());

// Counter State Management
final counterProvider = StateProvider<int>((ref) => 0);
```

#### Provider Hierarchy
```
ProviderScope
├── authStateChangesProvider (Stream)
├── authControllerProvider (StateNotifier)
└── counterProvider (State)
```

---

## 🚀 Getting Started

### 🧩 Prerequisites
- Flutter SDK 3.19+  
- Dart SDK 2.19+  
- Firebase Project  
- Android Studio / VSCode  

### 🪜 Installation

```bash
# Clone the repository
git clone https://github.com/your-username/flutter_counter_app.git
cd flutter_counter_app

# Install dependencies
flutter pub get
```

### 🔥 Firebase Setup

1. Create a new Firebase project  
2. Enable **Email/Password Authentication**  
3. Download `google-services.json` (Android) or `GoogleService-Info.plist` (iOS)  
4. Place the files in appropriate directories  
5. Generate Firebase options:
   ```bash
   flutterfire configure
   ```

### ▶️ Run the app
```bash
flutter run
```

---

## 📋 Usage

### Authentication Flow
- **Sign Up:** Create a new account  
- **Login:** Sign in with existing credentials  
- **Forgot Password:** Reset password via email  
- **Home:** Access counter features after login  

### Counter Features
- **➕ Increment:** Increases counter by 1  
- **➖ Decrement:** Decreases counter by 1  
- **🔁 Reset:** Resets counter to 0  

---

## 🔧 Configuration

### Firebase Initialization

```dart
await Firebase.initializeApp(
  options: DefaultFirebaseOptions.currentPlatform,
);
```

### Environment Variables
(Optional) Create a `.env` file for sensitive configuration values.

---

## 🧪 Testing

Run tests using:
```bash
flutter test
```

### Test Coverage
- ✅ Unit tests for `AuthController`  
- ✅ Widget tests for UI components  
- ✅ Integration tests for user flows  

---

## 📦 Dependencies

### Main Dependencies
```yaml
dependencies:
  flutter:
    sdk: flutter
  firebase_core: ^2.24.0
  firebase_auth: ^4.13.0
  flutter_riverpod: ^2.4.0
```

### Dev Dependencies
```yaml
dev_dependencies:
  flutter_test:
    sdk: flutter
  flutter_lints: ^3.0.0
```

---

## 🎯 Design Patterns

- **State Management:** Riverpod + StateNotifier  
- **Authentication:** Firebase Auth + StreamProvider  
- **Error Handling:** Centralized error management  
- **Form Validation:** Real-time validation with `FormKey`  
- **Navigation:** MaterialPageRoute with structured routing  

---

## 🔒 Security

- Firebase Authentication for secure user management  
- Strong password validation  
- Token-based authentication  
- Input sanitization and validation  


