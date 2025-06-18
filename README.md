# rig-ui-screens
## RigBookingApp (Borewell Rig Rental)

## 🚧 Project Status: Under Development 🚧

This is a React Native mobile application built with Expo for booking borewell rigs. The project is currently in the front-end development phase, focusing on core booking functionalities and user profile management.

---

## 🚀 Features Implemented

The application currently supports the following key functionalities:

* **Rig Listing:** Browse a list of available borewell rigs.
* **Rig Details & Booking:**
    * View detailed information for a selected rig.
    * Select a booking date using a calendar picker.
    * Choose an available time slot using a dropdown picker.
    * Enter user contact details (name, phone number).
    * **Booking Confirmation:** A placeholder alert confirms the booking details (no backend integration yet).
* **User Profile Management:** A dedicated section for user-specific functionalities.
    * **Profile Dashboard:** Main entry point for profile-related actions.
    * **Edit Profile:** Update personal information such as name, email, location, and phone number with basic client-side validation.
    * **Booking History:** View a list of past, upcoming, completed, pending, and canceled bookings (using dummy data).
    * **Saved Addresses:** Manage frequently used drilling locations (using dummy data, with placeholder for add/edit/delete actions).
    * **App Settings:** Configure application preferences (e.g., push notifications, location services, privacy policy, app version).
    * **Help & Support:** Access FAQs and contact information for support.
* **Consistent Navigation:**
    * Utilizes Expo Router for file-system-based routing.
    * Ensures consistent header styles and navigation behavior across all profile-related screens via `profile/_layout.tsx`.
    * Integrates a Drawer Navigator for top-level navigation, including a custom header.
    * Uses a Tab Navigator for the main "Home" section.

---

## 🛠️ Technology Stack

* **React Native:** A framework for building native mobile apps using React.
* **Expo:** A platform for universal React applications, providing tools and services for development, building, and deployment.
* **Expo Router:** File-system-based routing for React Native and web applications built with Expo.
* **React Navigation:** Used for Drawer and Tab navigators.
* **`react-native-calendars`:** For the date selection component in the booking form.
* **`react-native-dropdown-picker`:** For the time slot selection component in the booking form.
* **`@expo/vector-icons`:** For a rich set of icons used throughout the UI.
* **`react-native-gesture-handler` & `react-native-reanimated`:** Core dependencies for React Navigation's drawer and stack navigators.

---

## 📦 Installation

To get a local copy up and running, follow these simple steps.

### Prerequisites

* Node.js (LTS version recommended)
* npm or Yarn (npm comes with Node.js)
* Expo CLI (`npm install -g expo-cli` if you don't have it)

### Steps

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/rig-ui-screens.git](https://github.com/your-username/rig-ui-screens.git)
    cd rig-ui-screens
    ```
    *(Remember to replace `your-username/rig-ui-screens.git` with your actual repository URL)*

2.  **Install Dependencies:**
    ```bash
    npm install
    # or
    yarn install
    ```

3.  **Start the Expo Development Server:**
    ```bash
    npm start
    # or
    npx expo start
    ```
    This command will open a new tab in your web browser with the Expo Dev Tools.

4.  **Run on a Device or Emulator:**
    From the Expo Dev Tools page, you can:
    * Scan the QR code with the **Expo Go app** on your physical Android or iOS device.
    * Press `a` in the terminal to open on an **Android emulator**.
    * Press `i` in the terminal to open on an **iOS simulator** (macOS only).
    * Press `w` to open in your web browser (might have UI inconsistencies compared to native).

---

## 📱 Usage

Once the app is running on your device or emulator:

1.  **Browse Rigs:** The default screen will display a list of available borewell rigs (the "Home" tab).
2.  **View Rig Details & Book:** Tap on any rig card to navigate to its details page. Here, you can select a booking date/time and fill in contact information. Tapping "Book Now" will trigger a confirmation alert.
3.  **Access Main Navigation (Drawer):** Tap the **menu icon (☰)** in the top-left corner of the "Rigs" screen header to open the main drawer navigator.
4.  **Navigate to Profile:** From the drawer, select "My Profile" to access the user's profile dashboard.
5.  **Explore Profile Features:** Within the profile section, you can:
    * Tap "Edit Profile" to update personal details.
    * Tap "Booking History" to see simulated past and upcoming bookings.
    * Tap "Saved Addresses" to manage frequently used locations.
    * Tap "App Settings" to adjust various application preferences.
    * Tap "Help & Support" for assistance.

---

## 📂 Project Structure (Key Files/Folders)

```text
rig-ui-screens/
├── app/
│   ├── (tabs)/                 # Bottom tab navigator group
│   │   ├── index.tsx           # Main Rig Listing (Home tab screen)
│   │   └── _layout.tsx         # Defines the Tab Navigator for the bottom tabs
│   ├── booking/
│   │   └── [id].tsx            # Dynamic route for specific Rig Details & Booking Form
│   ├── profile/
│   │   ├── _layout.tsx         # Defines the Stack Navigator for all profile screens
│   │   ├── index.tsx           # Main Profile Dashboard (entry point to profile features)
│   │   ├── bookingHistory.tsx  # Screen for displaying booking history
│   │   ├── editProfile.tsx     # Screen for editing user profile information
│   │   ├── helpAndSupport.tsx  # Screen for help and support content
│   │   ├── savedAddresses.tsx  # Screen for managing user's saved addresses
│   │   └── settings.tsx        # Screen for application settings
│   ├── _layout.tsx             # Root layout of the application (defines the Drawer Navigator)
├── assets/                     # Directory for images, fonts, and other static assets
├── app.json                    # Expo project configuration file
├── package.json                # Node.js project dependencies and scripts
└── README.md                   # This README file
