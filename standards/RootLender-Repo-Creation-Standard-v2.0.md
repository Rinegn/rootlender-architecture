# 📘 RootLender Repo Creation Standard
Version: 2.0
Status: Mandatory for All New Repositories

---

## PURPOSE

Defines the required process for creating any new RootLender repository.

Ensures:
- Structural consistency
- Deterministic setup
- Clean boot validation
- Review-ready baseline state
- Controlled commit hygiene

Applies to:
- Backend services
- Frontend dashboards
- Shared libraries
- Infrastructure repos

---

## GLOBAL RULES

### GitHub First
- Owner: Rinegn
- Public during dev
- Use HTTPS clone
- Do NOT auto-generate README, .gitignore, or license

Local root:
C:\Users\ericowow\Documents\RootLender

---

### Clone Before Writing

git clone https://github.com/Rinegn/<repo-name>.git
cd "<repo-name>"

Must contain only .git before writing files.

---

### PowerShell-Only Population

All folders and files must be created using:
- New-Item
- Out-File
- Here-strings
- UTF8Encoding without BOM

No manual file creation.

---

# BACKEND STANDARD (FastAPI)

1. Create venv per repo
2. Full folder layout first
3. No empty directories
4. Root files required:
   - .gitignore
   - .env.example
   - .env
   - requirements.txt
5. README required before install
6. Install via requirements.txt only
7. Import sanity check before run
8. Run on explicit port
9. Commit baseline then push
10. Change repo to private

---

# FRONTEND STANDARD (Next.js)

1. No venv
2. Required structure:
   - app/
   - components/
   - lib/
3. Boot placeholder before UI logic
4. Layout system required
5. API calls only through gateway
6. Validate after each major change
7. Commit clean baseline
8. Change repo to private

---

# PROHIBITED PRACTICES

- Manual folder creation
- Empty files
- Direct microservice calls from frontend
- Installing packages before structure complete
- Writing code before cloning repo

---

# CORE PRINCIPLE

Backend punishes partial logic.
Frontend punishes partial structure.

This standard prevents both.

---

# STATUS UPDATE FORMAT

Example:
Loan Service baseline stable — OpenAPI + health verified — Port 8003 assigned.

Borrower Dashboard baseline stable — Layout + routing clean — Gateway-ready.
