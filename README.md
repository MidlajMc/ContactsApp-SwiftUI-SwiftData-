# 📱 Contacts App (SwiftUI + SwiftData)

A simple and modern **Contacts Management App** built using **SwiftUI** and **SwiftData** (iOS 17+).
This project demonstrates how to build a fully functional CRUD app with persistent storage using Apple’s latest data framework.

---

## 🚀 Features

* ✅ Add new contacts
* ✏️ Edit existing contacts
* 🗑️ Delete contacts (swipe & button)
* 🔍 Search contacts by name
* 💾 Persistent storage using SwiftData
* 🔄 Automatic UI updates

---

## 🛠 Tech Stack

* **SwiftUI** – UI framework
* **SwiftData** – Data persistence
* **iOS 17+**

---

## 📸 Screenshots

> Add your screenshots here (recommended)

* Contact List
* Add Contact Screen
* Edit Contact Screen

---

## 🧱 Project Structure

```
ContactsApp/
│
├── Models/
│   └── Contact.swift
│
├── Views/
│   ├── ContentView.swift
│   ├── ContactRawView.swift
│   ├── AddContactView.swift
│   └── EditContactView.swift
│
├── ContactsApp.swift
```

---

## ⚙️ Setup Instructions

1. Clone the repository:

```bash
git clone https://github.com/your-username/contacts-app.git
```

2. Open in Xcode (iOS 17+ required)

3. Run the project on Simulator or Device

---

## 🧩 SwiftData Integration

### Model

```swift
@Model
class Contact {
    var firstName: String
    var lastName: String
    var email: String
    var phone: String
}
```

### Container Setup

```swift
.modelContainer(for: Contact.self)
```

### Fetching Data

```swift
@Query var contacts: [Contact]
```

---

## ➕ Add Contact

```swift
context.insert(contact)
try? context.save()
```

---

## ✏️ Update Contact

```swift
contact.firstName = "Updated Name"
try? context.save()
```

---

## 🗑️ Delete Contact

```swift
context.delete(contact)
try? context.save()
```

---

## ⚠️ Known Issues / Notes

* If data behaves unexpectedly during development, delete and reinstall the app (SwiftData schema reset)
* Avoid manually managing IDs unless needed
* Ensure `.modelContainer()` is properly configured

---

## 💡 Future Improvements

* 📸 Add profile images
* 🔤 A–Z contact grouping
* ☁️ iCloud sync
* 📞 Call / Email actions
* 🎨 UI enhancements

---

## 🤝 Contributing

Feel free to fork this project and submit pull requests.

---

## 📄 License

This project is open-source and available under the MIT License.

---

## 🙌 Acknowledgements

Built using Apple’s modern frameworks:

* SwiftUI
* SwiftData

---

⭐️ If you like this project, give it a star on GitHub!
