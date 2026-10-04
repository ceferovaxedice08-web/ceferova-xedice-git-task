# Git Practice

Git & GitHub branch workflow tapşırığı.

Fayllar: index.html, app.py, README.md

Branch-lər: main, staging, develop, feature/html-page, feature/python-script

## Komandalar

Clone və ilk commit:
```
git clone https://github.com/ceferovaxedice08-web/ceferova-xedice-git-task.git
git add .
git commit -m "Initial project files"
git push -u origin main
```

Branch yaratmaq:
```
git checkout -b staging
git checkout -b develop
git checkout -b feature/html-page
```

Remote branch-i lokala gətirmək:
```
git fetch origin
git checkout -b feature/python-script origin/feature/python-script
```

Merge:
```
git checkout develop
git merge feature/html-page
git merge feature/python-script
git push origin develop
```

Sonra eyni qayda ilə develop -> staging -> main merge edildi.

git fetch yenilikləri gətirir, amma branch-i dəyişmir. git pull isə həm gətirir, həm də birləşdirir.
