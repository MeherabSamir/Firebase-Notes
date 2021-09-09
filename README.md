# Firebase Notes

### Setting Up Auth

```javascript
// Importing getAuth
import { getAuth } from "https://www.gstatic.com/firebasejs/9.0.1/firebase-auth.js";
```

### Creating User With Email & Password

```javascript
// Importing createUserWithEmailAndPassword
import {
  getAuth,
  createUserWithEmailAndPassword,
} from "https://www.gstatic.com/firebasejs/9.0.1/firebase-auth.js";

const auth = getAuth();

createUserWithEmailAndPassword(auth, email, password).then(() => {
  // Actions here...
});
```

### Checking Auth State

```javascript
// Importing onAuthStateChanged
import {
  getAuth,
  createUserWithEmailAndPassword,
  onAuthStateChanged,
} from "https://www.gstatic.com/firebasejs/9.0.1/firebase-auth.js";

const auth = getAuth();

onAuthStateChanged(auth, (user) => {
  if (user) {
    // User is signed in, see docs for a list of available properties
    // Actions here...
  } else {
    // User is signed out
    // Actions here...
  }
});
```

### Getting Data From Firestore

```javascript
// Importing collection,getDocs & getFirestore
import {
  collection,
  getDocs,
  getFirestore,
} from "https://www.gstatic.com/firebasejs/9.0.1/firebase-firestore.js";
const db = getFirestore();
const querySnapshot = await getDocs(collection(db, "dashboard-info"));
querySnapshot.forEach((doc) => {
  console.log(`${doc.id} => ${doc.data()}`);
  console.log(doc.data());
});
```

Will Be Updated Soon Insha Allah 😃
