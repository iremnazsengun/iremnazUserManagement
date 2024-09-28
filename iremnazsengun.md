# User Management Screen - UI Specification

### Overview
The User Management screen provides a visual interface for administrators to manage users. The functionalities include displaying a list of users, adding new users, and editing existing users. This document details the requirements, UI components, and expected behavior of the User Management screen.

---

## 1. Initial View

- The screen is divided into two main sections:
  - **User List Table** (left section)
  - **User Form** for adding or editing a user (right section)

- **User List Table**:
  - Displays the current users in the system.
  - Each row represents one user, showing:
    - **ID**: A unique identifier for each user.
    - **User Name**: The username of the user.
    - **Email**: The email address of the user.
    - **Enabled**: A boolean value indicating whether the user is active (true) or inactive (false).

- **User Form**:
  - At the beginning, the form is empty and used to create a new user.
  - If a user from the User List is selected, the form fields are populated with the user’s details for editing.

---

## 2. User List Table

### Requirements:
- **Columns**:
  - **ID**: Displays a unique integer representing each user.
  - **User Name**: Displays the username of the user.
  - **Email**: Displays the email address.
  - **Enabled**: Displays whether the user is active (true) or inactive (false).

- **Filters**:
  - There are filter icons next to each column header that allow filtering of users based on that column's value.

- **Sort**:
  - Clicking the column headers allows sorting users in ascending/descending order for that specific column.

### Behavior:
- Clicking a row in the table loads the user’s information into the form on the right for editing.

---

## 3. User Form

### Requirements:
This form is used to add or edit users.

- **Fields**:
  1. **Username**: Input field for the user's username.
  2. **Display Name**: Input field for the user's display name.
  3. **Phone**: Input field for the user's phone number.
  4. **Email**: Input field for the user's email address.
  5. **User Roles**: Dropdown to assign roles to the user.
     - Available roles:
       - **Guest**
       - **Admin**
       - **SuperAdmin**
  6. **Enabled**: A checkbox indicating if the user is active (enabled).

- **Buttons/Actions**:
  - **Save**: Submits the form, either adding a new user or saving edits to an existing user.
  - **Clear**: Resets the form, clearing all fields for new user creation.

### Behavior:
- When a user is selected from the User List Table, the form is pre-filled with that user’s details.
- The dropdown for **User Roles** allows multiple selections.
- The checkbox for **Enabled** will be checked if the user is active.
- Upon saving, the list on the left is refreshed to show the updated user list.

---

## 4. Error Handling

- **Mandatory Fields**: If required fields like Username or Email are not filled, the system should display an error message, e.g., “Username is required.”
- **Duplicate Entries**: If a user tries to save a username or email already existing, an error message should be shown, e.g., “Username already exists.”

---

## 5. Additional Details

- **Responsive Design**: The layout should be responsive and adjust based on screen size.
- **Accessibility**: Ensure all input fields and buttons are accessible via keyboard navigation.

---

### To-Do for Developers:
1. Implement the User List Table with sorting and filtering functionality.
2. Create the User Form with validation for each field.
3. Ensure the form can both create and edit users.
4. Provide error handling and user feedback for invalid input or duplicate data.
5. Ensure the UI is responsive and accessible.

---

### Next Steps:
This specification should guide the development team in creating the User Management screen. Ensure to follow this document closely to meet the functional and design requirements.
