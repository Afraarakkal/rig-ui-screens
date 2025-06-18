# rig-ui-screens
RigBookingApp (Borewell Rig Rental)
🚧 Project Status: Under Development 🚧
This is a React Native mobile application built with Expo for booking borewell rigs. The project is currently in the front-end development phase, focusing on core booking functionalities and user profile management.

🚀 Features Implemented
The application currently supports the following key functionalities:

Rig Listing: Browse a list of available borewell rigs.
Rig Details & Booking:
View detailed information for a selected rig.
Select a booking date using a calendar picker.
Choose an available time slot using a dropdown picker.
Enter user contact details (name, phone number).
Booking Confirmation: A placeholder alert confirms the booking details (no backend integration yet).
User Profile Management: A dedicated section for user-specific functionalities.
Profile Dashboard: Main entry point for profile-related actions.
Edit Profile: Update personal information such as name, email, location, and phone number with basic validation.
Booking History: View a list of past, upcoming, completed, pending, and canceled bookings (using dummy data).
Saved Addresses: Manage frequently used drilling locations (using dummy data, with placeholder for add/edit/delete actions).
App Settings: Configure application preferences (e.g., push notifications, location services, privacy policy, app version).
Help & Support: Access FAQs and contact information for support.
Consistent Navigation:
Utilizes Expo Router for file-system-based routing.
Ensures consistent header styles and navigation behavior across all profile-related screens via profile/_layout.tsx.
Integrates a Drawer Navigator for top-level navigation, including a custom header.
Uses a Tab Navigator for the main "Home" section.
🛠️ Technology Stack
React Native: A framework for building native mobile apps using React.
Expo: A platform for universal React applications, providing tools and services for development, building, and deployment.
Expo Router: File-system-based routing for React Native and web applications built with Expo.
React Navigation: Used for Drawer and Tab navigators.
react-native-calendars: For the date selection component in the booking form.
react-native-dropdown-picker: For the time slot selection component in the booking form.
@expo/vector-icons: For a rich set of icons used throughout the UI.
react-native-gesture-handler & react-native-reanimated: Core dependencies for React Navigation's drawer and stack navigators.
📦 Installation
To get a local copy up and running, follow these simple steps.

Prerequisites
Node.js (LTS version recommended)
npm or Yarn (npm comes with Node.js)
Expo CLI (npm install -g expo-cli if you don't have it)
Steps
Clone the repository:
Bash

git clone https://github.com/your-username/RigBookingApp.git
cd RigBookingApp
Install dependencies:
Bash

npm install
# or
yarn install
Start the Expo development server:
Bash

npm start
# or
npx expo start
This will open a new tab in your browser with Expo Dev Tools.
Run on a device or emulator:
Scan the QR code with the Expo Go app on your physical device.
Press a to run on an Android emulator.
Press i to run on an iOS simulator (macOS only).
📱 Usage
Once the app is running:

Browse Rigs: The home screen (default tab) will display a list of available borewell rigs.
Book a Rig: Tap on any rig card to view its detailed information. On the rig details page, select a booking date and time, fill in your contact information, and tap the "Book Now" button. A confirmation alert will appear (no actual booking occurs without a backend).
Access Drawer Navigation: On the "Rigs" home screen, tap the menu icon (☰) in the top-left corner to open the main drawer navigator.
Navigate to Profile: From the drawer, select "My Profile" to access your user profile dashboard.
Manage Profile:
Edit Profile: Update your personal details like name, email, and location.
Booking History: View a list of your simulated past and upcoming rig bookings.
Saved Addresses: Manage your frequently used drilling site addresses.
App Settings: Adjust application preferences such as notifications and privacy settings.
Help & Support: Find help resources and contact information.
📂 Project Structure (Key Files/Folders)
RigBookingApp/
├── app/
│   ├── (tabs)/                 # Contains screens for the bottom tab navigator
│   │   ├── index.tsx           # Main rig listing (Home tab)
│   │   └── _layout.tsx         # Defines the bottom tab navigator
│   ├── booking/
│   │   └── [id].tsx            # Dynamic route for individual rig details and booking
│   ├── profile/
│   │   ├── _layout.tsx         # Defines the stack navigator for all profile screens (consistent headers)
│   │   ├── index.tsx           # Main Profile dashboard
│   │   ├── bookingHistory.tsx  # User's booking history list
│   │   ├── editProfile.tsx     # Form to edit user profile details
│   │   ├── helpAndSupport.tsx  # Help, FAQ, and support page
│   │   ├── savedAddresses.tsx  # Manage user's saved addresses
│   │   └── settings.tsx        # App settings (notifications, privacy, etc.)
│   ├── _layout.tsx             # Root layout of the entire app (defines the Drawer Navigator)
├── assets/                     # Placeholder for images, fonts, etc.
├── app.json                    # Expo project configuration
├── package.json                # Project dependencies and scripts
└── README.md                   # This file
💡 Future Enhancements
Backend Integration: Implement a robust backend to handle user authentication, rig data, booking management, and data persistence.
User Authentication: Full login, registration, password reset, and session management.
Payment Gateway: Integrate a secure payment system for rig bookings.
Real-time Availability: Display dynamic rig availability based on actual booking data and scheduling.
Map Integration: Allow users to view and select drilling locations on an interactive map.
Push Notifications: Implement real-time push notifications for booking updates, reminders, and offers.
Search & Filters: Enhance rig listing with search functionality and various filtering options (e.g., rig type, capacity, location).
User Reviews/Ratings: Enable users to leave reviews and ratings for completed bookings and rigs.
Admin/Rig Owner Panel: Develop a separate interface for rig owners to manage their fleet, bookings, and availability.
🤝 Contributing
Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

Fork the Project
Create your Feature Branch (git checkout -b feature/AmazingFeature)
Commit your Changes (git commit -m 'Add some AmazingFeature')
Push to the Branch (git push origin feature/AmazingFeature)
Open a Pull Request
📄 License
Distributed under the MIT License. See LICENSE for more information (you might need to create a LICENSE file in your repository if you haven't already).
