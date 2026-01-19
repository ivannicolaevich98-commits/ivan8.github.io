<!DOCTYPE html><html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Marketplace (Admin only)</title>
  <script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-auth-compat.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-firestore-compat.js"></script>
  <style>
    body { font-family: Arial, sans-serif; margin: 20px; }
    .hidden { display: none; }
    .item { border: 1px solid #ccc; padding: 10px; margin: 10px 0; }
    button { margin: 5px; }
  </style>
</head>
<body>
  <h1>Marketplace</h1> <div id="auth">
    <button onclick="googleLogin()">Войти через Google</button>
    <button onclick="emailLogin()">Войти через Email</button>
  </div> <div id="user" class="hidden">
    <p id="userEmail"></p>
    <button onclick="logout()">Выйти</button>
  </div> <hr /> <div id="adminPanel" class="hidden">
    <h2>Админ-панель</h2>
    <input id="title" placeholder="Название товара" />
    <input id="price" placeholder="Цена" />
    <textarea id="desc" placeholder="Описание"></textarea><br />
    <button onclick="addItem()">Добавить объявление</button>
  </div> <h2>Объявления</h2>
  <div id="items"></div><script>
  // 🔴 ВСТАВЬ СВОИ ДАННЫЕ FIREBASE
  const firebaseConfig = {
    apiKey: "PASTE_API_KEY",
    authDomain: "PASTE_AUTH_DOMAIN",
    projectId: "PASTE_PROJECT_ID"
  };

  // 🔴 ВСТАВЬ СВОЙ UID АДМИНА
  const ADMIN_UID = "PASTE_ADMIN_UID";

  firebase.initializeApp(firebaseConfig);
  const auth = firebase.auth();
  const db = firebase.firestore();

  auth.onAuthStateChanged(user => {
    if (user) {
      document.getElementById('auth').classList.add('hidden');
      document.getElementById('user').classList.remove('hidden');
      document.getElementById('userEmail').innerText = user.email;

      if (user.uid === ADMIN_UID) {
        document.getElementById('adminPanel').classList.remove('hidden');
      }
    } else {
      document.getElementById('auth').classList.remove('hidden');
      document.getElementById('user').classList.add('hidden');
      document.getElementById('adminPanel').classList.add('hidden');
    }
  });

  function googleLogin() {
    const provider = new firebase.auth.GoogleAuthProvider();
    auth.signInWithPopup(provider);
  }

  function emailLogin() {
    const email = prompt('Email');
    const password = prompt('Пароль');
    auth.signInWithEmailAndPassword(email, password)
      .catch(() => auth.createUserWithEmailAndPassword(email, password));
  }

  function logout() {
    auth.signOut();
  }

  function addItem() {
    const title = document.getElementById('title').value;
    const price = document.getElementById('price').value;
    const desc = document.getElementById('desc').value;

    db.collection('items').add({ title, price, desc });
  }

  db.collection('items').onSnapshot(snapshot => {
    const itemsDiv = document.getElementById('items');
    itemsDiv.innerHTML = '';
    snapshot.forEach(doc => {
      const data = doc.data();
      itemsDiv.innerHTML += `<div class="item"><b>${data.title}</b><br>Цена: ${data.price}<br>${data.desc}</div>`;
    });
  });
</script></body>
</html>
