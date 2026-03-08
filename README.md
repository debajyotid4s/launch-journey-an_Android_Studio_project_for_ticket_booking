# Launch Journey — Android Ticket Booking App

![Launch Journey Banner](https://github.com/user-attachments/assets/566251d6-b586-4799-ac93-56b9172fd2db)

**Launch Journey** is a fully functional Android application for booking River Cruise / Boat tickets. In Bangladesh, these vessels are commonly referred to as "Launches." The app provides a fair, secure, and visually engaging experience — supporting user registration, authentication, ticket booking, and profile management, all directly from your Android device.

---

## Table of Contents

- [Features](#features)
- [Screenshots](#screenshots)
- [Technologies & Libraries Used](#technologies--libraries-used)
- [Project Structure](#project-structure)
- [Compatibility & Build Configuration](#compatibility--build-configuration)
- [Getting Started](#getting-started)
- [Known Limitations](#known-limitations)
- [Author](#author)

---

## Features

- **Splash / Welcome Screen**: Animated intro with auto-redirect to the sign-in screen.
- **Secure Registration & Login**: Uses Firebase Authentication with BCrypt password hashing.
- **Dynamic Trip Search**: Select departure, destination, and travel date to search available trips.
- **Available Trips Listing**: Displays real-time trip data fetched from Firestore for the selected route and date.
- **Ticket Selection**: Choose ticket type (VIP, Single Cabin, or Deck) and quantity (up to 3 per booking), with live availability checks.
- **Checkout & Payment**: 10-minute countdown timer, payment method selection, and transaction ID entry. Inventory is updated automatically after successful booking.
- **Booking History**: View and manage past and upcoming bookings.
- **Profile Management**: View and update personal information (name, email, phone, address).
- **Modern UI**: Material Design components, custom MiSans fonts, Lottie animations, and a smooth, responsive experience.

---

## Screenshots

![App Screenshot](https://github.com/user-attachments/assets/d6a163c7-c4c6-4eae-8251-811215e865d0)

---

## Technologies & Libraries Used

| Technology / Library | Purpose |
|---|---|
| **Java** | Complete application logic and UI |
| **Android Studio** | Official IDE for design, development, and debugging |
| **Firebase Firestore** | Cloud-based storage for user and ticket data |
| **Firebase Realtime Database** | Fast UID storage and auxiliary backend operations |
| **Firebase Authentication** | Secure user sign-up, sign-in, and session management |
| **BCrypt (`org.mindrot.jbcrypt`)** | Secure password hashing before storage |
| **Glide** | Efficient image loading and caching |
| **Lottie** | Smooth vector animations |
| **Material Components** | Modern Android UI following Material Design guidelines |
| **XML Layouts** | Responsive and interactive screen layouts |
| **Gradle** | Build automation, dependency management, and versioning |
| **Custom Fonts (MiSans)** | Unique, modern app typography |

---

## Project Structure

```
app/src/main/java/com/example/launchjourney/
├── MainActivity.java            # Splash / welcome screen with animations
├── sign_in_activity.java        # User login screen
├── creating_account_page.java   # User registration screen
├── home_page_activity.java      # Main search screen (departure, destination, date)
├── AvailableTripsActivity.java  # Lists available trips for the selected route & date
├── TicketDetailsActivity.java   # Ticket type and quantity selection
├── CheckOut.java                # Payment screen with countdown timer
├── Finalize.java                # Booking confirmation screen
├── TicketAdapter.java           # RecyclerView adapter for ticket items
├── LaunchAdapter.java           # RecyclerView adapter for launch/trip items
├── TicketCancel.java            # Ticket cancellation flow
├── TicketCanceled.java          # Cancellation confirmation screen
├── trips.java                   # Booking history screen
├── profile.java                 # User profile view
├── contact.java                 # Profile edit / contact update screen
├── Launch.java                  # Data model for a Launch (vessel/trip)
├── ticket.java                  # Data model for a Ticket
└── User.java                    # Data model for a User
```

---

## Compatibility & Build Configuration

| Setting | Value |
|---|---|
| **Namespace** | `com.example.launchjourney` |
| **Compile SDK** | 34 |
| **Target SDK** | 34 |
| **Minimum SDK** | 24 (Android 7.0 Nougat and above) |
| **Java Compatibility** | Java 11 |
| **View Binding** | Enabled |
| **ProGuard** | Configured (minification disabled in release builds) |
| **Test Runner** | AndroidJUnitRunner |

### Gradle Plugins

- `com.android.application`
- `com.google.gms.google-services`

### Key Dependencies

- **Material Design**: `com.google.android.material:material`
- **Glide**: `com.github.bumptech.glide:glide` + annotation processor
- **Lottie**: `com.airbnb.android:lottie`
- **Firebase BOM**: Authentication, Firestore, Analytics, Storage, Realtime Database
- **Google Play Services Auth**: `com.google.android.gms:play-services-auth`
- **BCrypt**: `org.mindrot:jbcrypt`
- **AndroidX**: AppCompat, ConstraintLayout, Activity, Navigation

---

## Getting Started

### Prerequisites

- [Android Studio](https://developer.android.com/studio) (Hedgehog or later recommended)
- Android device or emulator running Android 7.0+ (API 24+)
- A Firebase project with Firestore, Authentication, and Realtime Database enabled
- `google-services.json` placed in the `app/` directory

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/debajyotid4s/launch-journey-an_Android_Studio_project_for_ticket_booking.git
   ```
2. **Open in Android Studio** — select *Open an Existing Project* and choose the cloned folder.
3. **Sync Gradle** — Android Studio will automatically prompt you to sync; let all dependencies resolve.
4. **Add Firebase config** — place your `google-services.json` in the `app/` directory.
5. **Build & Run** — connect a device or start an emulator and click **Run**.

### Quick Install (APK)

[⬇ Download APK](https://www.mediafire.com/file/j4wf3dgkoggefpa/LaunchJourney.apk/file) — install directly on any Android 7.0+ device (enable *Install from Unknown Sources* in device settings).

---

## Known Limitations

- **Forgot Password**: Not yet implemented.
- **Profile Picture Upload**: Not fully implemented; uploading to Firebase Storage was skipped to stay within free-tier usage limits.
- **OTP Verification**: Not implemented; Firebase discontinued free SMS OTP for this use case.

---

## Author

Developed by **[debajyotid4s](https://github.com/debajyotid4s)**.

---
