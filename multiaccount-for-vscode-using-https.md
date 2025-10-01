# GitHub Multi-Account (HTTPS + VS Code)

## 1. Set remote with username
Personal repo:
```bash
git remote set-url origin https://PersonalUser@github.com/PersonalUser/repo.git
```

Work repo:
```bash
git remote set-url origin https://WorkUser@github.com/WorkOrg/repo.git
```

Check:
```bash
git remote -v
```

---

## 2. Save credentials per repo
```bash
git config --global credential.helper manager
git config --global credential.useHttpPath true
```

---

## 3. Login in VS Code
- First time you push/pull, VS Code opens browser.  
- Log in with the account that matches the repo URL.  
- Token is saved in Windows Credential Manager.  

---

## 4. Switch account if wrong
1. Delete GitHub entries in Windows Credential Manager.  
2. Update remote with correct username.  
3. Run:
```bash
git ls-remote origin
```
→ Login again with correct account.

---

## 5. Default branch
If repo uses `main`:
```bash
git branch --set-upstream-to=origin/main
```
