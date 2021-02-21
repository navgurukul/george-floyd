## To Update with Upstream while separating the commits

1. ```git checkout -b upstream main branch_name```
(Assuming upstream remote is referred to as "main")

2. ```git checkout branch_name```

3. ```git diff upstream > diff.patch```

4. ```git checkout upstream```

5. ```git branch -d branch_name```

6. ```git apply diff.patch```

7. ```rm diff.patch```

8. ```git add -A```

9. ```git commit -m "Diff Commit"```

10. ```git checkout -b develop```

11. ```git branch -d upstream```

12. ```git push -f --set-upstream origin develop```
