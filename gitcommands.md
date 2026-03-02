#git commands
git config --list
git config --global user.name ""
git config --global user.email ""




 1465  git --version
 1466  git config --list
 1467  git config --global user.name "tester"
 1468  git config --global user.email "tooltesting07@gmail.com"
 1469  git config --list
 1470  cd Documents/
 1471  ls
 1472  mkdir testgit
 1473  git init
 1474  git status
 1475  cd testgit
 1476  git init
 1477  nano gitcommands.md
 1478  git add gitcommands.md
 1479  git commit -m "First commit"
 1480  git branch
 1481  git branch -M main
 1482  git branch
 1483  git remote add origin git@github.com:tester-2070/testgit.git
 1484  git push -u origin main
 1485  git remote add origin https://github.com/tester-2070/testgit.git
 1486  ls -al ~/.ssh
 1487  ssh-keygen -t ed25519 -C "tooltesting007@gmail.com"
 1488  cat ~/.ssh/id_ed25519.pub
 1489  ssh -T git@github.com
 1490  git push -u origin main
 1491  git status
 1492  history > history.md
