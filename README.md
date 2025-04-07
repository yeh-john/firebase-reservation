# Reservation Form

This project provides an HTML-based reservation form that allows users to select their name, email, phone number, reservation date, and class type. The form validates the date to ensure reservations are only made for Tuesdays or Fridays. Once the user submits the form, a summary of their reservation is displayed for confirmation, and upon confirmation, the reservation data is saved to Firebase Realtime Database.

## Features

- **Input Fields:**
  - Name
  - Email
  - Phone Number
  - Reservation Date (Date Picker)
  - Class Selection (Class A, B, C, D)
  
- **Validation:**
  - Ensures the reservation date falls on a Tuesday or Friday.
  - Displays a warning message if the selected date is invalid.
  
- **Summary:**
  - Displays a reservation summary for confirmation.
  - Option to save the reservation or cancel.

- **Firebase Integration:**
  - Saves reservation data (name, email, phone number, reservation date, and class) to Firebase Realtime Database.
  - Automatically converts the reservation date to Japan Standard Time (JST) before saving.

## Requirements

- A Firebase project with the Firebase Realtime Database enabled.
- Firebase SDK to be included in the project for database operations.

## Setup

1. Clone or download the project files.
2. Replace the Firebase configuration in the script section with your own Firebase credentials. You can obtain these from your Firebase console.
3. Open the HTML file in any modern web browser to use the form.

## Firebase Configuration

The Firebase SDK is included in the `<script>` tags in the HTML file. Replace the placeholder values in the script below with your Firebase project details:

```js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  databaseURL: "YOUR_DATABASE_URL",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

Make sure the Firebase SDKs are loaded correctly in your project.

## Functionality

1. **Reservation Validation:**
   - The form checks if the selected date is either a Tuesday or Friday. If it is not, a warning message will appear, and the reservation summary will not display.
   
2. **Reservation Summary:**
   - After selecting a valid date, the form shows a summary of the reservation with details such as name, email, phone, date, and class.
   
3. **Save Reservation:**
   - Upon confirmation, the reservation is saved to Firebase, and the form is reset for the next entry.

4. **Cancel Reservation:**
   - If the user cancels, the form will reset without saving any data.

## Contributing

Feel free to contribute by submitting issues or pull requests. Ensure that any changes you make are well-documented and tested.

## Contact

For any questions or feedback, feel free to reach out via email or open an issue on GitHub. You can also visit my website at [https://yeh-john.github.io](https://yeh-john.github.io).

---

Enjoy using the reservation form!
