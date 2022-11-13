# vcs-submodules
Этот репозиторий получен следующим образом:
1) создали и склонировали этот репозиторий
2) склонировали https://github.com/tensorflow/tensorflow
3) ``cd tensorflow/``
4) ``git checkout r1.14``
5) ``git filter-branch --subdirectory-filter tensorflow/contrib/ HEAD -- --all``
6) ``git reset --hard``
7) ``git gc --aggressive``
8) ``git prune``
9) ``git remote rm origin``
10) создали репозиторий `tensorflow-contrib`
11) ``git remote add origin https://github.com/zilante/tensorflow-contrib.git``
12) ``git push --set-upstream origin r1.14``
13) ``cd vcs-submodules/``
14) ``git submodule add https://github.com/zilante/tensorflow-contrib.git``
15) ``cd tensorflow-contrib/``
16) ``git checkout r1.14``
17) ``cd ../``
18) ``git add .gitmodules tensorflow-contrib/``
19) ``git commit -m "add submodule"``
20) ``git push``