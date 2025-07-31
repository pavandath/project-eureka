Hello! Here's a **simple and clear real-time scenario** to demonstrate **absolute and relative paths**, assuming your home directory is `/home/rama`.

---

### 🔧 **Scenario: Navigating Project Files**

Assume you’re working on a project with the following folder structure:

```
/home/rama/
├── project/
│   ├── README.md
│   ├── scripts/
│   │   └── deploy.sh
│   └── config/
│       └── settings.json
```

---

### 🎯 **Goal**: Access `settings.json` from `deploy.sh`

---

### ✅ **Absolute Path Usage**

From inside the `deploy.sh` script, you want to access `settings.json` using the **absolute path**:

```bash
cat /home/rama/project/config/settings.json
```

* **Always starts from root `/`**
* Works from **anywhere** in the system
* **Never breaks** even if your current directory changes

---

### ✅ **Relative Path Usage**

If you're **already inside** the `scripts/` directory:

```bash
cd /home/rama/project/scripts
cat ../config/settings.json
```

* Starts **relative to current directory**
* `..` goes **one level up** to `project/`
* Then navigates into `config/`

---

### 🧠 Summary for Students

| Concept       | Command Example                               | From Where?                            |
| ------------- | --------------------------------------------- | -------------------------------------- |
| Absolute Path | `cat /home/rama/project/config/settings.json` | Anywhere in the system                 |
| Relative Path | `cat ../config/settings.json`                 | Only from `/home/rama/project/scripts` |

---

