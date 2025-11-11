# LR6
Лабораторная работа №6

**Цель работы:** *изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.*

```zsh
git config --global user.name "4415 Алексеев Д.А."
git config --global user.email "danlmalexeev@yandex.ru"
git clone https://github.com/Skorozp/LR6
cd LR6
git pull
git log
git branch -a
git log
git checkout -b new-feature
echo "изменения в ветке new-feature" >> test-file.txt
git add .
git commit -m "Добавлен файл в новую ветку"
git merge new-feature
git status
git checkout -b conflict-branch
echo "conflict-branch" >> New_file.txt
git add New_file.txt
git commit -m "добавил New_file.txt в conflict-branch что бы создать конфликт"
git checkout master
echo "изменение из master" >> New_file.txt
git add New_file.txt
git commit -m "изменение New_file.txt в master"
git merge conflict-branch
git add New_file.txt
git commit -m "слияние conflict-branch в master, разрешен конфликт в New_file.txt"
git branch -d new-feature
git branch -d conflict-branch
git push origin master
echo "первое изменение" >> changes.txt
git add changes.txt
git commit -m "добавлен файл changes.txt"
echo "второе изменение" >> changes.txt
git add changes.txt
git commit -m "изменён файл changes.txt"
echo "Третье изменение" >> New_file.txt
git add New_file.txt
git commit -m "Обновлен New_file.txt"
git log --oneline -5
git reset --soft HEAD~1
git status
git checkout -b report-branch
mkdir screenshots
```

**Выводы:** *В ходе работы были освоены основные операции работы с Git и GitHub.*


## История операций
```
0bbf853 - 2025-11-11 - 4415 Алексеев Д.А. - изменён файл changes.txt
923c806 - 2025-11-11 - 4415 Алексеев Д.А. - добавлен файл changes.txt
d12ac17 - 2025-11-11 - 4415 Алексеев Д.А. - слияние conflict-branch в master, разрешен конфликт в New_file.txt
4b1fc35 - 2025-11-11 - 4415 Алексеев Д.А. - изменение New_file.txt в master
efb57e7 - 2025-11-11 - 4415 Алексеев Д.А. - добавил New_file.txt в conflict-branch что бы создать конфликт
5b90983 - 2025-11-11 - 4415 Алексеев Д.А. - Добавлен файл в новую ветку
c4ea9c5 - 2025-11-11 - skorozp - Create New_file.txt
921f53b - 2020-11-21 - Kurtyanik - Обновление информации
c08a654 - 2020-11-21 - Kurtyanik - Файл создан пустым
3c6e913 - 2020-11-21 - Kurtyanik - Initial commit
```

