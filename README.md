# Babylon Radio App 📻

A Flutter mobile application with Firebase Authentication implementation for Babylon Radio assessment.

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-039BE5?style=for-the-badge&logo=Firebase&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)

## 📋 Assessment Overview

This project was developed as part of the Babylon Radio assessment task. The goal was to create a simple Flutter app with Firebase Authentication that includes:

- ✅ **Login Page** with Full Name, Email, and Password fields
- ✅ **Firebase Authentication** for user registration and login
- ✅ **Homepage** with personalized greeting and logout functionality
- ✅ **Input validation** for all form fields
- ✅ **Error handling** and user feedback
- ✅ **Responsive UI** with Material Design 3

## 🚀 Features

### Authentication System
- **User Registration**: New users can create accounts with full name, email, and password
- **User Login**: Existing users can sign in with email and password
- **Form Validation**: Real-time validation for all input fields
- **Password Visibility Toggle**: Users can show/hide password input
- **Error Handling**: Comprehensive error messages for authentication failures

### User Experience
- **Personalized Welcome**: Homepage greets users by their full name
- **User Profile Display**: Shows user's name and email on the homepage
- **Secure Logout**: Confirmation dialog before logout with automatic redirect
- **Loading States**: Visual feedback during authentication processes
- **Responsive Design**: Works seamlessly across different screen sizes

### Technical Features
- **Firebase Integration**: Complete Firebase setup with Authentication and Firestore
- **State Management**: Efficient state management using StatefulWidget
- **Navigation**: Smooth navigation between screens with proper state handling
- **Data Persistence**: User data stored securely in Firestore database
- **App Check**: Firebase App Check integration for security

## 🏗️ Project Structure

```
lib/
├── main.dart                 # App entry point with Firebase initialization
├── firebase_options.dart     # Firebase configuration (auto-generated)
├── screens/
│   ├── login_screen.dart     # Login/Registration UI and logic
│   └── home_screen.dart      # Home page with user greeting and logout
└── services/
    └── auth_service.dart     # Firebase Authentication service layer
```

## 🛠️ Tech Stack

- **Framework**: Flutter 3.0+
- **Language**: Dart
- **Backend**: Firebase
  - Firebase Authentication
  - Cloud Firestore
  - Firebase App Check
- **UI**: Material Design 3
- **State Management**: StatefulWidget with setState

## 📱 Screens & Features

### 1. Login Screen (`login_screen.dart`)
- **Dual Mode**: Switches between Login and Registration
- **Form Fields**:
  - Full Name (Registration only)
  - Email Address (with email validation)
  - Password (with strength validation)
- **Validation**:
  - Email format validation using RegEx
  - Password minimum length (6 characters)
  - Full name minimum length (2 characters)
- **UI Features**:
  - Password visibility toggle
  - Loading indicators
  - Error message display via SnackBar
  - Responsive layout with SingleChildScrollView

### 2. Home Screen (`home_screen.dart`)
- **Personalized Greeting**: "Hey, [User Name]! You're successfully logged in"
- **User Information Display**: Shows user's full name and email
- **Logout Functionality**: 
  - Confirmation dialog
  - Secure sign out
  - Automatic redirect to login screen
- **UI Elements**:
  - Success icon and welcome message
  - User info card with profile details
  - Styled logout button

### 3. Authentication Service (`auth_service.dart`)
- **User Registration**:
  - Creates Firebase Auth account
  - Stores user profile in Firestore
  - Error handling for duplicate emails and weak passwords
- **User Login**:
  - Firebase email/password authentication
  - Comprehensive error handling
- **User Data Management**:
  - Fetches user's full name from Firestore
  - Current user state management
- **Logout**: Secure Firebase sign out

## 🔧 Setup & Installation

### Prerequisites
- Flutter SDK (3.0.0 or higher)
- Dart SDK
- Android Studio / VS Code
- Firebase account
- Git

### Installation Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Ala-Eddine-Achach/bookish-memory.git
   cd babylon_radio_app
   ```

2. **Install Dependencies**
   ```bash
   flutter pub get
   ```

3. **Firebase Setup**
   - The project is already configured with Firebase
   - Firebase configuration files are included:
     - `lib/firebase_options.dart`
     - `android/app/google-services.json`
   - Firestore database is set up with proper security rules

4. **Run the Application**
   ```bash
   flutter run
   ```

### Development Setup
```bash
# Clean build files
flutter clean

# Get dependencies
flutter pub get

# Run on specific device
flutter run -d <device_id>

# Build for Android
flutter build apk

# Build for iOS
flutter build ios
```

## 🔥 Firebase Configuration

### Project Details
- **Project ID**: `babylon-radio-app-dd53c`
- **Authentication**: Email/Password enabled
- **Firestore**: User profiles stored in `users` collection
- **App Check**: Enabled for security (debug mode for development)

### Firestore Schema
```
users/ (collection)
├── [userId]/ (document)
    ├── fullName: string
    ├── email: string
    └── createdAt: timestamp
```

## 🧪 Testing Scenarios

The app has been tested for the following scenarios:

### ✅ New User Registration
1. User enters full name, email, and password
2. Form validation ensures all fields are valid
3. Firebase creates new account
4. User profile stored in Firestore
5. Automatic navigation to home screen
6. Personalized welcome message displayed

### ✅ Existing User Login
1. User enters email and password
2. Firebase authenticates credentials
3. User profile retrieved from Firestore
4. Navigation to home screen
5. Welcome message with user's name

### ✅ Logout Functionality
1. User clicks logout button
2. Confirmation dialog appears
3. Upon confirmation, Firebase signs out user
4. Automatic redirect to login screen
5. Authentication state properly cleared

### ✅ Error Handling
- Invalid email format
- Weak passwords
- Duplicate account registration
- Wrong login credentials
- Network connectivity issues
- Empty form fields

## 📝 Development Approach

### Architecture Decisions
1. **Service Layer**: Separated authentication logic into `AuthService` class for better code organization and reusability
2. **State Management**: Used StatefulWidget with setState for simple, effective state management
3. **Form Validation**: Implemented real-time validation with comprehensive error messages
4. **Error Handling**: Added try-catch blocks and user-friendly error messages
5. **UI/UX**: Focused on Material Design 3 principles for consistent, modern interface

### Code Quality
- **Clean Architecture**: Separation of concerns between UI, business logic, and data layers
- **Error Handling**: Comprehensive error handling throughout the application
- **Code Documentation**: Inline comments and clear variable naming
- **Responsive Design**: Layouts that work across different screen sizes
- **Security**: Firebase App Check integration and secure authentication flow

## 🔮 Future Improvements

### Potential Enhancements
1. **Enhanced Authentication**
   - Social login (Google, Apple, Facebook)
   - Phone number authentication
   - Biometric authentication
   - Password reset functionality

2. **User Experience**
   - Profile editing functionality
   - Profile picture upload
   - Remember me functionality
   - Dark mode support
   - Internationalization (i18n)

3. **Technical Improvements**
   - State management with Provider/Riverpod/Bloc
   - Unit and integration tests
   - CI/CD pipeline setup
   - Performance monitoring
   - Crash reporting (Firebase Crashlytics)
   - Analytics integration

4. **Security Enhancements**
   - Two-factor authentication
   - Account verification via email
   - Session management
   - Rate limiting for authentication attempts

## 🐛 Known Issues & Limitations

- **Development Mode**: Firebase App Check is configured for debug mode only
- **Email Verification**: Email verification is not implemented
- **Password Reset**: Password reset functionality not included
- **Offline Support**: Limited offline capabilities

## 🤝 Challenges Faced

1. **Firebase Configuration**: Setting up Firebase with multiple platform support required careful configuration management
2. **Form Validation**: Implementing comprehensive validation while maintaining good UX
3. **State Management**: Ensuring proper state synchronization between authentication states and UI
4. **Error Handling**: Creating user-friendly error messages for various Firebase authentication errors

## 📞 Contact & Support

- **Developer**: Ala Eddine Achach
- **Repository**: [bookish-memory](https://github.com/Ala-Eddine-Achach/bookish-memory)
- **Assessment**: Babylon Radio Flutter Developer Position

---

**Note**: This project was developed as part of a technical assessment for Babylon Radio. It demonstrates proficiency in Flutter development, Firebase integration, and mobile app architecture principles.
