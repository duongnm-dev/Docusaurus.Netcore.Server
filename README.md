# Docusaurus + ASP.NET Core Server

This repository is a full example of hosting a **Docusaurus site** using an **ASP.NET Core server**.  
The solution contains both:

- **DocusaurusApp** → a [Docusaurus](https://docusaurus.io/) project (React-based static site generator).  
- **DocusaurusServer.Web** → a lightweight ASP.NET Core project that serves the static files built by Docusaurus.  

---

## 🚀 How it works
1. When you build the .NET project, it automatically:
   - Runs `npm install` in the Docusaurus project (if needed).  
   - Builds the Docusaurus site (`npm run build`).  
   - Copies the generated files from `DocusaurusApp/build` into `wwwroot` of the ASP.NET Core project.  
2. ASP.NET Core then serves the static site at `http://localhost:5000` (or `https://localhost:7000`).  

---

## 🛠 Project structure
```
DocusaurusServer.sln
├── DocusaurusServer.Web/     # ASP.NET Core server
│   ├── Program.cs
│   └── wwwroot/              # Static files (auto-filled after build)
└── DocusaurusApp/            # Docusaurus site
    ├── package.json
    └── ...
```

---

## ▶️ Run locally

### 1. Clone the repo
```bash
git clone https://github.com/yourname/DocusaurusServer.git
cd DocusaurusServer
```

### 2. Run the server
```bash
dotnet run --project DocusaurusServer.Web
```

### 3. Open your browser
- Go to [http://localhost:5000](http://localhost:5000)  
- You will see your Docusaurus site served by ASP.NET Core 🎉  

---

## 📦 Publish
When you publish the .NET app:
```bash
dotnet publish -c Release
```
The output will already contain the built Docusaurus site inside `wwwroot`.  
You can then deploy it anywhere you host .NET applications (IIS, Docker, Kubernetes, Azure, etc).  

---

## ✅ Benefits
- Keep frontend (Docusaurus) and backend (ASP.NET Core) in one solution.  
- Automatic Docusaurus build during .NET build.  
- Easy deployment as a single .NET Core app.  
