## Hi there 👋  
I'm **Raj Sonu** — a passionate Web Developer from India 🇮🇳

🔭 **Currently working on:**  
Full-Stack Web Development Projects & Real-World Applications

🌱 **Currently learning:**  
React.js, Node.js, Database Design & Cloud Fundamentals

👯 **Looking to collaborate on:**  
Innovative Tech Projects, Product Development & Open Source

🤔 **Looking for help with:**  
System Design, Backend Optimization & Scalable Applications

💬 **Ask me about:**  
JavaScript, Web Development, APIs, Freelancing & Project Building

📫 **How to reach me:**  
Email: rs2420315@gmail.com  
LinkedIn: https://www.linkedin.com/in/purushottam-kumar-5111b1160/

⚡ **Fun fact:**  
I love solving complex problems and turning ideas into scalable products 🚀

---

### 🛠️ Tech Stack

**Frontend:** HTML | CSS | JavaScript | React  
**Backend:** Node.js | Express  
**Database:** MySQL | MongoDB  
**Tools:** Git | GitHub | VS Code | Postman

---

### ⚡ Performance Optimization Tips

A key area I focus on is writing **efficient, scalable code**. Here are common patterns I watch for and improve:

#### 1. Avoid repeated DOM lookups (Frontend)
```js
// ❌ Slow – queries the DOM on every iteration
for (let i = 0; i < 1000; i++) {
  document.getElementById('output').innerText += i;
}

// ✅ Fast – cache the reference once
const output = document.getElementById('output');
let result = '';
for (let i = 0; i < 1000; i++) {
  result += i;
}
output.innerText = result;
```

#### 2. Use efficient data structures (JavaScript)
```js
// ❌ Slow – O(n) lookup on every check
const allowedRoles = ['admin', 'editor', 'viewer'];
if (allowedRoles.includes(userRole)) { /* ... */ }

// ✅ Fast – O(1) lookup with a Set
const allowedRoles = new Set(['admin', 'editor', 'viewer']);
if (allowedRoles.has(userRole)) { /* ... */ }
```

#### 3. Batch database queries (Node.js / Backend)
```js
// ❌ Slow – N+1 problem: one query per user
const users = await User.findAll();
for (const user of users) {
  user.orders = await Order.findAll({ where: { userId: user.id } });
}

// ✅ Fast – single query with a JOIN / eager loading
const users = await User.findAll({ include: [{ model: Order }] });
```

#### 4. Use pagination for large result sets
```js
// ❌ Slow – loads the entire table into memory
const allRecords = await db.query('SELECT * FROM logs');

// ✅ Fast – fetch only what is needed
const DEFAULT_PAGE = 1, DEFAULT_LIMIT = 20;
const records = await db.query(
  'SELECT * FROM logs ORDER BY created_at DESC LIMIT ? OFFSET ?',
  [DEFAULT_LIMIT, (DEFAULT_PAGE - 1) * DEFAULT_LIMIT]
);
```

#### 5. Cache expensive computations
```js
// ❌ Slow – recomputes on every call
function getConfig() {
  return JSON.parse(fs.readFileSync('./config.json', 'utf8'));
}

// ✅ Fast – parse once and reuse
const config = JSON.parse(fs.readFileSync('./config.json', 'utf8'));
function getConfig() {
  return config;
}
```

---

### 📊 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=rajsonu315&show_icons=true&theme=tokyonight)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=rajsonu315&layout=compact&theme=tokyonight)
