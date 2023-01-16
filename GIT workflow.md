## Quy trình tạo 1 PR:
Checkout về branch `develop`

```
git checkout develop
```

Pull code mới nhất về

```
git pull origin develop
```

Tạo branch mới

```
git checkout -b <branch-name>
```

*Note: branch-name có dạng: `issue-{ID}-{tên-issue}`*

Chuyển sang branch mới tạo

```
git checkout <branch-name>
```

Khi làm xong, commit code

```
git add .
git commit -m "Issue {ID}: commit message"
```

Push code lên

```
git push origin <branch-name>
```

## Quy trình rebase code mới nhất từ `develop`:

Pull code mơi nhất của branch `develop` về

```
git fetch origin develop:develop
```

*Note: Kiểm tra code ở nhánh hiện tại, nếu có file thay đổi thì commit lại hoặc stash lại*

Rebase code mới nhất từ `develop` vào branch hiện tại

```
git rebase develop
```

*Note: Nếu có conflict thì fix conflict và commit lại*

```
git add .
git rebase --continue
```
