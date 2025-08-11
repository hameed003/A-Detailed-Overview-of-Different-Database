# Types of Database:

<details>
<summary> Self-Hosted Database Vs Managed Third-Party Database✅</summary>

---

- A database can either be a **`Self Hosted`** or **`Managed By Third Party`**.

### 🏠 Self-Hosted Database

- **Self Hosted** database means we manually `install`, `Setup` and `Use` a database either on our `local machine` or on `Cloud Server` **( VPS )** like `Hostinger`, `AWS EC2`, `DigitalOcean`, `Linode`. 

**Example of Self Hosted database:**
- `SQL`: MySQL, PostgreSQL etc.
- `NoSQL`: MongoDB ( MongoDB itself is also a self‑hosted database—we install it on our own server or VM )

---

### ☁️ Managed Third-Party Database
- A cloud provider `hosts` and `manages` the database for you.

**Example of Self Hosted database:**
- `SQL`: PlanetScale ( MySQL ), Supabase,Render, Railway, Neon.tech ( PostgreSQL )
- `NoSQL`: MongoDB Atlas, Firebase
</details>

---

<details>
<summary>A: SQL Database✅ </summary>

---

* Stores data in **tables** with `rows` & `columns`.
* Uses **Structured Query Language (SQL)** for queries.
* Good for structured, relational data.
* Examples: `MySQL`, `PostgreSQL`, `SQLite`, `Oracle Database`, `MariaDB` etc.

---

<details>
<summary>Types of SQL database</summary>

1. `MySQL`, 
2. `PostgreSQL`, 
3. `SQLite`, 
4. `Oracle Database`, 
5. `MariaDB etc`.

<details>
<summary>1. MySQL</summary>

---

Here’s a detailed **MySQL installation & usage table**:

| **Ways/Methods of installation**           | **Where it Runs**   | **Type**    | **How to Use**                                                                    | **Pros**                          | **Cons**                                      |
| ----------------------------------------- | ------------------- | ----------- | --------------------------------------------------------------------------------- | --------------------------------- | --------------------------------------------- |
| **Local Install (XAMPP/WAMP/MAMP)**       | Your PC/Laptop      | Self-hosted | Install MySQL server locally, use phpMyAdmin or CLI                               | Offline dev, full control         | Not accessible online without port forwarding |
| **Local Install (Direct MySQL)**          | Your PC/Laptop      | Self-hosted | Install MySQL via installer or package manager (e.g., `apt install mysql-server`) | Lightweight, direct control       | Manual config, no GUI by default              |
| **Cloud VPS (AWS, DigitalOcean, Linode)** | Your rented server  | Self-hosted | Install MySQL yourself on VPS, configure remote access                            | Full control, scalable            | Requires setup, security, backups             |
| **PlanetScale**                           | PlanetScale servers | Managed     | Create DB online, get MySQL connection URL                                        | Serverless, autoscaling, no setup | Free tier limits, no local DB                 |
| **ClearDB (for Heroku)**                  | ClearDB servers     | Managed     | Add ClearDB add-on to Heroku, use given URL                                       | Easy with Heroku apps             | Limited free tier                             |
| **Aiven (MySQL)**                         | Aiven servers       | Managed     | Create MySQL instance, connect via credentials                                    | Easy setup, reliable              | Limited free tier                             |


</details>


<details>
<summary>2. PostgreSQL</summary>

---

Here’s the **PostgreSQL installation & usage table**:

| **Ways/Methods of installation**           | **Where it Runs**   | **Type**    | **How to Use**                                                       | **Pros**                           | **Cons**                                      |
| ----------------------------------------- | ------------------- | ----------- | -------------------------------------------------------------------- | ---------------------------------- | --------------------------------------------- |
| **Local Install (pgAdmin)**               | Your PC/Laptop      | Self-hosted | Install PostgreSQL + pgAdmin locally, manage via GUI or CLI (`psql`) | Easy dev setup, full control       | Not accessible online without port forwarding |
| **Local Install (Direct PostgreSQL)**     | Your PC/Laptop      | Self-hosted | Install via installer or package manager (`apt install postgresql`)  | Lightweight, full control          | Manual config needed                          |
| **Cloud VPS (AWS, DigitalOcean, Linode)** | Your rented server  | Self-hosted | Install PostgreSQL yourself on VPS, configure remote access          | Full control, scalable             | Setup, security, backups required             |
| **Railway**                               | Railway servers     | Managed     | Create PostgreSQL DB, get connection URL                             | Easy, free tier, auto deploy       | Free tier limits                              |
| **Render**                                | Render servers      | Managed     | Create PostgreSQL DB, connect via given credentials                  | Simple, good for apps              | Free tier size limits                         |
| **Neon.tech**                             | Neon servers        | Managed     | Serverless PostgreSQL, connect via credentials                       | Autoscaling, modern                | Newer platform, may have limits               |
| **Supabase**                              | Supabase servers    | Managed     | Comes with PostgreSQL + Auth + API                                   | Full backend features, instant API | Slightly larger learning curve                |
| **ElephantSQL**                           | ElephantSQL servers | Managed     | Create DB online, connect via URL                                    | Simple setup                       | Very small free tier                          |

</details>

---

MySQL and PostgreSQL **don't have fixed free storage limits** like `MongoDB Atlas` or `Firebase`, because they are **self-hosted** databases. You can install them locally or on `cloud servers` (like `AWS EC2`, `Render`, `Railway`) and storage depends on:

### 💾 Storage Limit Depends On:

* **Your local disk space** (for local setups)
* **Your hosting plan** (for cloud-hosted)

## ✅ Free Hosting Options:

| Platform        | Free Tier Storage (approx)                  | Notes                                  |
| --------------- | ------------------------------------------- | -------------------------------------- |
| **Render**      | 256MB (PostgreSQL)                          | Free plan, limited connections         |
| **Railway**     | 500MB (PostgreSQL)                          | Generous free tier                     |
| **ElephantSQL** | 20MB (PostgreSQL)                           | Free "Tiny Turtle" plan                |
| **Neon.tech**   | Unlimited storage (PostgreSQL), pay per use | Modern, serverless Postgres            |
| **PlanetScale** | Unlimited (MySQL)                           | Serverless, limited usage in free tier |


<details>
<summary>3. SQLite</summary>

---

Here’s the **SQLite installation & usage table**:

| **Ways/Methods of installation**  | **Where it Runs**                    | **Type**            | **How to Use**                                                                    | **Pros**                                | **Cons**                                             |
| --------------------------------- | ------------------------------------ | ------------------- | --------------------------------------------------------------------------------- | --------------------------------------- | ---------------------------------------------------- |
| **Local Install (Standalone)**    | Your PC/Laptop                       | Self-hosted         | Install SQLite CLI or use built-in support in languages (Python, PHP, Node, etc.) | Extremely lightweight, no server needed | Only one file, not great for heavy concurrent writes |
| **Embedded in Application**       | Same machine as app                  | Self-hosted         | Bundled inside desktop/mobile/web apps                                            | Portable, works offline                 | Not suited for distributed access                    |
| **In-memory Mode**                | App’s memory                         | Self-hosted         | Run SQLite purely in RAM (`:memory:` mode)                                        | Very fast for temp data                 | Data lost when app stops                             |
| **Cloud Storage (via file sync)** | Cloud drives (Dropbox, Google Drive) | Self-hosted (hacky) | Store `.sqlite` file in synced folder                                             | Easy sharing for small apps             | Risk of corruption on simultaneous access            |
| **Managed Hosting (rare)**        | Third-party                          | Managed             | Some PaaS (like Heroku add-ons) offer SQLite for dev                              | No setup needed                         | Rare for production, limited scalability             |

💡 **Key Note**:
SQLite is **not like MySQL/PostgreSQL** — it’s file-based, meaning the “database” is just a single `.sqlite` file. No dedicated server process is needed.



</details>

</details>

</details>

---

<details>
<summary>B: NoSQL Database✅</summary>

---

* Stores data in **non-tabular** formats ( `documents`, `key-value`, `graphs` ).
* Flexible schema, scales easily.
* Good for unstructured or rapidly changing data.
* Examples: `MongoDB`, `Firebase Firestore`, `Cassandra`, `Redis`, `DynamoDB`. 

---

<details>
<summary>Types of NoSQL Database</summary>

---

 1. `MongoDB`, 
 2. `Firebase Firestore`, 
 3. `Redis`, 
 4. `Cassandra`, 
 5. `DynamoDB` ( AWS-managed NoSQL database. )

---

<details>
<summary>1. MongoDB</summary>

---

Here’s the **MongoDB installation & usage table**:

| **Ways/Methods of installation**           | **Where it Runs**    | **Type**    | **How to Use**                                                | **Pros**                            | **Cons**                            |
| ----------------------------------------- | -------------------- | ----------- | ------------------------------------------------------------- | ----------------------------------- | ----------------------------------- |
| **Local Install (MongoDB Community)**     | Your PC/Laptop       | Self-hosted | Install MongoDB locally, use `mongosh` or MongoDB Compass GUI | Full control, offline dev           | Not accessible online without setup |
| **Local Install (Docker)**                | Your PC/Laptop       | Self-hosted | Run MongoDB in a Docker container (`docker run mongo`)        | Isolated environment, easy reset    | Need Docker knowledge               |
| **Cloud VPS (AWS, DigitalOcean, Linode)** | Your rented server   | Self-hosted | Install MongoDB manually on VPS, enable remote access         | Full control, scalable              | Manual security & backups           |
| **MongoDB Atlas**                         | Atlas servers        | Managed     | Create cluster online, connect with Mongo URI                 | Easiest, free tier, global clusters | Free tier storage limits            |
| **ScaleGrid (MongoDB)**                   | ScaleGrid servers    | Managed     | Create MongoDB instance, connect via URI                      | Advanced options, automated backups | Paid for larger setups              |
| **Aiven (MongoDB)**                       | Aiven servers        | Managed     | Create DB online, connect via credentials                     | Easy to set up, reliable            | Free tier is small                  |
| **ObjectRocket (MongoDB)**                | ObjectRocket servers | Managed     | Hosted MongoDB with scaling support                           | Enterprise-grade                    | Mostly paid plans                   |

</details>

---

<details>
<summary>2. Firestore</summary>

---

Here’s the **Firestore installation & usage table**:

| **Ways/Methods of installation**                        | **Where it Runs**    | **Type**                   | **How to Use**                                                            | **Pros**                           | **Cons**                                               |
| ------------------------------------------------------- | -------------------- | -------------------------- | ------------------------------------------------------------------------- | ---------------------------------- | ------------------------------------------------------ |
| **Firebase Local Emulator Suite**                       | Your PC/Laptop       | Self-hosted (for dev only) | Install Firebase CLI, run Firestore emulator (`firebase emulators:start`) | Test locally, no internet needed   | Not for production, data wiped easily                  |
| **Firebase Firestore (Cloud)**                          | Google Cloud servers | Managed                    | Create Firestore DB in Firebase Console, use SDK or REST API              | Fully managed, scalable, real-time | Free tier has limits, tied to Google ecosystem         |
| **Google Cloud Firestore (Native)**                     | Google Cloud servers | Managed                    | Access directly from Google Cloud console without full Firebase setup     | More cloud flexibility             | Still Google-managed, billing applies after free tier  |
| **Third-party Wrappers (e.g., Appwrite Firestore API)** | Various              | Managed                    | Use Firestore-like APIs provided by other platforms                       | Easier integration in some cases   | May have limited features compared to native Firestore |

💡 **Key Note**:
Unlike MySQL, PostgreSQL, or MongoDB, **Firestore can’t be truly self-hosted for production** — you can only emulate it locally for development. For production, you must use Google’s managed infrastructure.



</details>

---
<details>
<summary>3. Redis</summary>

---
Here’s the **Redis installation & usage table**:

| **Ways/Methods of installation**          | **Where it Runs**                                                      | **Type**    | **How to Use**                                                                     | **Pros**                              | **Cons**                                   |
| ----------------------------------------- | ---------------------------------------------------------------------- | ----------- | ---------------------------------------------------------------------------------- | ------------------------------------- | ------------------------------------------ |
| **Local Install**                         | Your PC/Laptop                                                         | Self-hosted | Install Redis server from [redis.io](https://redis.io), run `redis-server` locally | Fast for dev, full control            | Not accessible from internet without setup |
| **Self-Hosted on VPS**                    | Cloud servers (AWS, DigitalOcean, etc.)                                | Self-hosted | Install Redis on a cloud VM, connect via TCP                                       | Full control, customizable            | You handle scaling, backups, security      |
| **Docker Container**                      | Local or VPS                                                           | Self-hosted | Run `docker run redis` for instant setup                                           | Easy deploy/reset                     | Still your responsibility to maintain      |
| **Managed Services (Redis Cloud)**        | Redis Labs, AWS ElastiCache, Azure Cache for Redis, Google MemoryStore | Managed     | Create instance via provider UI, connect with provided URI                         | Auto-scaling, backups, no maintenance | Paid after free tier, vendor lock-in       |
| **In-Memory Embedded Mode (for testing)** | Inside app memory                                                      | Self-hosted | Run embedded Redis-like mock in dev tools                                          | No install needed                     | Not real Redis performance/features        |

💡 **Key Note**:
Redis is an **in-memory key-value database** — lightning fast, great for caching, session storage, and pub/sub messaging. It’s **NoSQL** but not document-oriented like MongoDB or Firestore.



</details>
</details>

</details>

---


<details>
<summary>Similarities and Differences between Supabase and Firebase and how they are different from other managed third party databases</summary>

---

Here’s a **detailed breakdown** of **Supabase vs Firebase**, plus how both differ from other managed third-party databases like **MongoDB Atlas, PlanetScale, Neon, ElephantSQL, etc.**

---

## **1. Similarities Between Supabase & Firebase**

| Feature                  | Supabase                                                   | Firebase                           |
| ------------------------ | ---------------------------------------------------------- | ---------------------------------- |
| **Authentication**       | ✅ Yes                                                      | ✅ Yes                              |
| **Database**             | ✅ Yes (PostgreSQL)                                         | ✅ Yes (Firestore or Realtime DB)   |
| **Real-time Updates**    | ✅ Yes (Postgres subscriptions)                             | ✅ Yes (native)                     |
| **Storage**              | ✅ Yes (file & image storage)                               | ✅ Yes (Cloud Storage)              |
| **APIs**                 | ✅ Auto-generated REST & GraphQL                            | ✅ Client SDKs for Firestore & RTDB |
| **Hosting**              | ❌ No built-in hosting (needs external hosting like Vercel) | ✅ Yes (Firebase Hosting)           |
| **Serverless Functions** | ✅ Edge Functions                                           | ✅ Cloud Functions                  |
| **Free Tier**            | ✅ Yes                                                      | ✅ Yes                              |

---

## **2. Differences Between Supabase & Firebase**

| Aspect                  | Supabase                                          | Firebase                                                   |
| ----------------------- | ------------------------------------------------- | ---------------------------------------------------------- |
| **Database Type**       | SQL (**PostgreSQL**)                              | NoSQL (**Firestore** or **Realtime DB**)                   |
| **API Access**          | Auto-generated REST & GraphQL                     | SDK-based (JavaScript, iOS, Android)                       |
| **Query Power**         | SQL queries (complex joins, aggregations)         | NoSQL queries (limited joins)                              |
| **Self-Hosting Option** | ✅ Open-source, can self-host Supabase             | ❌ Proprietary, only Google Cloud                           |
| **Pricing Growth**      | Scales with database size (Postgres)              | Scales with document reads/writes                          |
| **Ecosystem**           | PostgreSQL ecosystem (extensions, triggers)       | Google Cloud ecosystem                                     |
| **Best For**            | Apps needing relational DB power with auth & APIs | Apps needing rapid real-time sync and low setup complexity |

---

## **3. How They Differ From Other Managed Third-Party Databases**

Other managed database platforms like **MongoDB Atlas (MongoDB), PlanetScale (MySQL), Render (PostgreSQL),  Railway (PostgreSQL), Neon.tech (PostgreSQL), ElephantSQL (PostgreSQL)** are **just databases** — they don’t include:

* ✅ Authentication
* ✅ Auto-generated APIs
* ✅ File storage
* ✅ Real-time capabilities out of the box

**Example:**

* **MongoDB Atlas** → Only manages MongoDB (NoSQL document store). You must build authentication, API routes, file storage, and real-time features yourself (usually using Node.js/Express or another backend).
* **PlanetScale** → Managed MySQL only, no APIs or auth built in.
* **Neon** → Managed PostgreSQL only, no APIs or auth built in.

---

**💡 In short:**

* **Supabase & Firebase** = Full Backend-as-a-Service (BaaS) → Database + Auth + APIs + Storage + Realtime
* **Other Managed DBs** = Database-as-a-Service (DBaaS) → Only the database, you handle backend logic & integrations yourself

---

</details>

---

<details>
<summary>A detailed comparison table of Supabase, Firebase, MongoDB Atlas, PlanetScale, Neon, Railway, and Render — including whether they are SQL/NoSQL, which database type they use, and the key features.</summary>

---

Here’s a **detailed comparison table** of **Supabase, Firebase, MongoDB Atlas, PlanetScale, Neon, Railway, and Render** — including whether they are **SQL/NoSQL**, which **database type** they use, and the key features.

---

| Platform          | SQL / NoSQL                                | Database Type           | Self-host Option                                          | Auth | Auto APIs        | Storage | Real-time                      | Hosting                  | Serverless Functions | Free Tier               |
| ----------------- | ------------------------------------------ | ----------------------- | --------------------------------------------------------- | ---- | ---------------- | ------- | ------------------------------ | ------------------------ | -------------------- | ----------------------- |
| **Supabase**      | SQL                                        | PostgreSQL              | ✅ Yes (open-source)                                       | ✅    | ✅ REST + GraphQL | ✅       | ✅                              | ❌ (needs Vercel/Netlify) | ✅ Edge Functions     | ✅ Generous              |
| **Firebase**      | NoSQL                                      | Firestore / Realtime DB | ❌                                                         | ✅    | ❌ (SDK only)     | ✅       | ✅                              | ✅ Firebase Hosting       | ✅ Cloud Functions    | ✅ Generous              |
| **MongoDB Atlas** | NoSQL                                      | MongoDB                 | ❌ (Atlas is managed only, but MongoDB can be self-hosted) | ❌    | ❌                | ❌       | ❌ (needs change streams setup) | ❌                        | ❌                    | ✅ Generous              |
| **PlanetScale**   | SQL                                        | MySQL (serverless)      | ❌                                                         | ❌    | ❌                | ❌       | ❌                              | ❌                        | ❌                    | ✅ Generous              |
| **Neon**          | SQL                                        | PostgreSQL (serverless) | ❌                                                         | ❌    | ❌                | ❌       | ❌                              | ❌                        | ❌                    | ✅ Generous              |
| **Railway**       | SQL / NoSQL (depending on what you deploy) | PostgreSQL by default   | ❌                                                         | ❌    | ❌                | ❌       | ❌                              | ✅ App Hosting + DB       | ✅                    | ✅ Generous              |
| **Render**        | SQL / NoSQL (depending on what you deploy) | PostgreSQL by default   | ❌                                                         | ❌    | ❌                | ❌       | ❌                              | ✅ App Hosting + DB       | ✅                    | ✅ Free tier but limited |

---

### **Key Takeaways**

* **Supabase** → SQL (PostgreSQL) BaaS, similar to Firebase but SQL-based and open-source friendly.
* **Firebase** → NoSQL BaaS with Firestore/Realtime DB, best for quick real-time apps but no SQL queries.
* **MongoDB Atlas** → Managed MongoDB, NoSQL only, backend logic must be done separately.
* **PlanetScale & Neon** → Managed serverless SQL DBs (MySQL & PostgreSQL), no extra backend features.
* **Railway & Render** → More like general hosting platforms that **include** managed databases but are not full backend providers like Supabase/Firebase.

---

If you want, I can **add a “What You Still Need to Build” column** to show exactly what features you must handle yourself for each platform, like auth, API, storage, etc. That would make the differences even clearer.


</details>


---

### Note:
* For **MySQL**, there’s no platform like `Supabase` (PostgreSQL) or `Firebase` ( Firestore ) that gives full backend + auth + API out-of-the-box.
* You must handle things yourself using backend code ( like Express/Node.js ):

---

<details>

<summary>What does Serverless means in databases?</summary>

---

> “serverless” database usually means you don’t manage the server infrastructure yourself, but it doesn’t mean there’s no server at all (the provider runs it for you). it's just that you don't have to do setups and manage the server yourself instead ( the provider `setups`,`runs` and `manage` it for you )


### 🔹 Key Points:

* No need to set up or manage servers.
* You pay for usage, not uptime.
* Automatically scales for traffic.
* Can **pause when idle** to save cost.

### 🔸 Example:

With Neon:

* You create a PostgreSQL DB.
* Neon handles storage, compute, scaling.
* You connect via connection string—no server config.

🟢 Ideal for React + Node apps where you want simplicity, autoscaling, and minimal DevOps.

---

### List of database that are `serverless`.

| **Platform**      | **Serverless?**   | **Notes**                                                                      |
| ----------------- | ----------------- | ------------------------------------------------------------------------------ |
| **Supabase**      | ✅ Yes             | Serverless Postgres + auth + storage.                                          |
| **Firebase**      | ✅ Yes             | Fully serverless backend + Firestore/Realtime DB.                              |
| **MySQL (self-hosted)**        | ❌ No            | You install & manage the server yourself (local or VPS).            |
| **PostgreSQL (self-hosted)**   | ❌ No            | Same — needs manual setup & maintenance.                            |
| **MongoDB**       | ❌ No              | The DB engine itself is self-hosted unless you use Atlas.                      |
| **MongoDB Atlas** | ✅ Yes             | Serverless MongoDB hosting (managed by MongoDB).                               |
| **PlanetScale**   | ✅ Yes             | Serverless MySQL platform.                                                     |
| **Neon**          | ✅ Yes             | Serverless PostgreSQL platform.                                                |
| **Railway**       | ⚠️ Partial        | Can be serverless-like for DBs, but also hosts full apps/servers.               |
| **Render**        | ❌ No              | PaaS — hosts web services, databases, cron jobs (you manage server processes). |
| **Redis**         | ❌ No (by default) | In-memory DB, usually self-hosted; can be serverless via Redis Cloud.          |

</details>

---

<details>
<summary>List of Third Party Managed database platforms that also have self-hosting options, especially if they are open-source.</summary>

---
✅ quite a few **managed database platforms** also have **self-hosting options**, especially if they are **open-source**.

Here are some examples:

| **Platform**       | **DB Type**        | **Managed Cloud** | **Self-Host Option**     |
| ------------------ | ------------------ | ----------------- | ------------------------ |
| **Supabase**       | PostgreSQL         | Yes               | Yes (Docker, VPS, local) |
| **Appwrite**       | MongoDB (internal) | Yes               | Yes (Docker)             |
| **Parse Platform** | MongoDB            | Yes               | Yes                      |
| **Hasura**         | PostgreSQL         | Yes               | Yes                      |
| **Directus**       | Any SQL DB         | Yes               | Yes                      |
| **PocketBase**     | SQLite             | Yes               | Yes (single binary)      |

💡 **Note:** Services like **Firebase** or **MongoDB Atlas** are **not open-source**, so you cannot truly self-host them (you’d need to set up the underlying DB yourself instead).

</details>

---

<details>
<summary>Alternatives of Supabase</summary>

---

### 🔹 1. **Firebase**

* **DB**: NoSQL (Firestore, Realtime DB)
* ✅ Auth, Hosting, Functions, Storage
* ❌ Not SQL-based

---

### 🔹 2. **Appwrite**

* **DB**: Internal (uses MongoDB under the hood)
* ✅ Auth, Functions, Realtime, Storage
* 📦 Open source, self-hostable

---

### 🔹 3. **Nhost**

* **DB**: PostgreSQL
* ✅ Auth, GraphQL API, Functions, File storage
* 🚀 Developer-friendly, Supabase-like

---

### 🔹 4. **Hasura**

* **DB**: PostgreSQL (bring your own)
* ✅ Instant GraphQL APIs
* ❌ No built-in Auth (needs Firebase/Auth0)

---

### 🔹 5. **Parse (Back4App)**

* **DB**: MongoDB
* ✅ Auth, Realtime, Cloud functions
* 📱 Good for mobile apps

---


🧠 **Note**: Most of these use **PostgreSQL or NoSQL**, not **MySQL**.
For MySQL, platforms like **PlanetScale** give serverless DB, but **not full backend** like Supabase.

</details>

---

<details>
<summary>Does Supabase, Firebase or other Managed Third Party Databases provide file storage facility?</summary>

---

Yes ✅

Many **managed third-party databases** (especially BaaS platforms) provide **file storage** in addition to the database.

| Platform          | Provides Storage? | Notes                                                       |
| ----------------- | ----------------- | ----------------------------------------------------------- |
| **Supabase**      | ✅ Yes             | File & image storage with public/private access control.    |
| **Firebase**      | ✅ Yes             | Firebase Storage for files, backed by Google Cloud Storage. |
| **Appwrite**      | ✅ Yes             | Self-hostable storage API.                                  |
| **MongoDB Atlas** | ❌ No              | Only database, no file storage.                             |
| **PlanetScale**   | ❌ No              | Only MySQL database.                                        |
| **Neon**          | ❌ No              | Only PostgreSQL database.                                   |
| **Railway**       | ❌ No              | Focused on hosting DBs & apps.                              |
| **Render**        | ❌ No              | App & DB hosting, but no object storage.                    |
| **Redis Cloud**   | ❌ No              | In-memory cache DB only.                                    |

</details>

---

<details>
<summary>What is the difference between "database" and "file storage"?</summary>

---

Here’s the key difference:

| Feature         | **Database**                                                                       | **File Storage**                                              |
| --------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| **Purpose**     | Store **structured data** (rows, columns, key-value, documents) for fast querying. | Store **unstructured data** like files, images, videos, PDFs. |
| **Data Format** | Text, numbers, JSON, binary (small files).                                         | Raw files (any type) as they are.                             |
| **Querying**    | Search/filter using SQL or API queries.                                            | No complex queries — only upload, download, list files.       |
| **Performance** | Optimized for reading/writing small to medium-sized data quickly.                  | Optimized for serving large files efficiently.                |
| **Examples**    | PostgreSQL, MySQL, MongoDB, Redis.                                                 | Firebase Storage, AWS S3, Supabase Storage.                   |

💡 **Analogy**:

* Database = Your **notebook** with organized tables of information.
* File storage = Your **Google Drive folder** with raw files.

</details>