# Create-a-Personalized-Contact-Book-app-with-tkiner.
This Tkinter-based application allows users to manage a contact book where they can add, edit, delete, and  search contacts. The contacts are stored in a JSON file, allowing the data to persist even after the  application is closed. 
Below is an explanation of the program logic, broken down into key components
Loading and Saving Contacts 
Loading Contacts (load_contacts): 
The program first attempts to load contacts from a JSON file (contacts.json). If the file is 
missing or contains invalid data, it returns an empty dictionary. 
The contacts are stored in the contacts variable as a dictionary, where each contact's name is 
the key, and the value is another dictionary containing phone and email. 
Saving Contacts (save_contacts): 
The contacts dictionary is saved back to the contacts.json file whenever a contact is added, 
deleted, or edited. This is done using the json.dump() method. 
2. Adding a Contact (add_contact) 
 Users can input a contact's name, phone, and optionally email. 
 If both name and phone are provided, the contact is added to the contacts dictionary, and the list of 
contacts is updated in the Listbox widget. 
 After the new contact is added, the contact list is saved to the file, and the input fields are cleared. 
 If any required field is missing, a warning message box appears. 
3. Updating the Contact List (update_contact_listbox) 
 This function is called whenever there is a change in the contact list (e.g., adding, deleting, or 
editing contacts). 
 It clears the current Listbox and reloads it with the names of all contacts from the contacts 
dictionary. 
4. Deleting a Contact (delete_contact) 
 The user can select a contact from the Listbox and delete it. 
 The contact is removed from the contacts dictionary, and the contact list is updated. 
 After deletion, the updated list of contacts is saved back to the JSON file. 
 If no contact is selected, a warning message is displayed. 
5. Searching for a Contact (search_contact) 
 The search functionality allows the user to type in a search query (e.g., part of a contact's name). 
 The program filters the contacts and only displays those whose names match the search query 
(case-insensitive). 
 If no contacts match, an informational message is displayed. 
6. Viewing and Editing Contact Details (view_contact_details and edit_contact) 
 View Contact Details: When a user selects a contact from the Listbox, its details (name, phone, 
email) are loaded into the input fields so the user can view or edit them. 
Edit Contact: The user can modify the details of the selected contact. If the contact's name is 
changed, the old contact entry is removed from the dictionary, and the new entry is saved. The 
contact list and JSON file are updated accordingly. 
7. UI Elements (Tkinter Widgets) 
 Entry Fields: For entering contact details (name, phone, and email). 
 Buttons: For adding, editing, deleting, and searching contacts. 
 Listbox: To display the contact names and allow the user to select a contact for editing or deletion. 
 Search Bar: An input field where the user can type a search query, and a button to trigger the 
search function.
