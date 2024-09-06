Расположение файла страницы руководства в рамках файловой системы может быть определено с помощью команды `whereis`.
```run-bash
yurasik@NoName:~$ whereis -m whois
whois: /usr/share/man/man1/whois.1.gz
```

Этот файл может быть непосредственно прочитан с помощью команды `man`.

```run-bash
yurasik@NoName:~$ man /usr/share/man/man1/whois.1.gz
```
