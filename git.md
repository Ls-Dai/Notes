```
git checkout --orphan temp
git add -a
git commit -m "..."
git branch -d main
git branch -m main
git push -f origin main
```