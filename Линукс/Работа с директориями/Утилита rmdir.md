Чтобы удалить директорию следует воспользоваться командой`rmdir`
--
Только в том случае, если директория пуста

```bash
paul@debian8:~$ rmdir mydir
```

**Команда rmdir -p**
--
По аналогии с параметром `mkdir -p`, вы также можете использовать утилиту `rmdir` для рекурсивного удаления директорий.

```bash
paul@debian8:~$ rmdir -p test42/subdir
```
