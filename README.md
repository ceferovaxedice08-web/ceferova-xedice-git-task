# Git Practice

Git & GitHub branch workflow üzrə praktiki tapşırıq.

## Fayllar
- `index.html` - sadə HTML səhifə
- `app.py` - sadə Python skript
- `README.md` - layihə təsviri

## Branch strukturu
`main` -> `staging` -> `develop` -> `feature/html-page`, `feature/python-script`

## İstifadə olunan komandalar

### 1. Repository-ni clone etmək və ilk commit
```
git clone https://github.com/ceferovaxedice08-web/ceferova-xedice-git-task.git
cd ceferova-xedice-git-task
git status
git add .
git commit -m "Initial project files"
git branch -M main
git push -u origin main
```

### 2. staging və develop branch-lərini yaratmaq
```
git checkout -b staging
git push -u origin staging
git checkout -b develop
git push -u origin develop
```

### 3. Lokal feature branch (feature/html-page)
```
git checkout develop
git pull origin develop
git checkout -b feature/html-page
git add index.html
git commit -m "Update HTML page"
git push -u origin feature/html-page
```

### 4. GitHub-da yaradılan remote branch (feature/python-script)
```
git checkout develop
git fetch origin
git branch -a
git checkout -b feature/python-script origin/feature/python-script
git add app.py
git commit -m "Improve Python script"
git push origin feature/python-script
```

### 5. Feature branch-ləri develop ilə birləşdirmək
```
git checkout develop
git pull origin develop
git merge feature/html-page
git merge feature/python-script
git push origin develop
```

### 6. develop -> staging -> main
```
git checkout staging
git pull origin staging
git merge develop
git push origin staging
git checkout main
git pull origin main
git merge staging
git push origin main
```

### 7. git fetch və git pull fərqi
```
git fetch origin
git status
git pull origin main
```
- `git fetch` - remote-dakı yenilikləri gətirir, amma cari branch-i dəyişmir.
- `git pull` - yenilikləri gətirir və cari branch ilə birləşdirir (fetch + merge).

### 8. Tarixçəyə baxmaq
```
git log --oneline --graph --all
```
