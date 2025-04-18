Прежде чем ставить [[Docker Desktop]], необходимо поставить Docker Engine. Для этого:
1. Удаляем конфликтующие пакеты старых версий (вводить все сразу):
```sh
for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; 
do sudo apt-get remove $pkg; 
done
```
2. Добавляем GPG - ключ:
```sh
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
```
3. Прописываем источник обновлений для Docker:
```sh
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$UBUNTU_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
Если стоит Ubuntu, а не какое-то из ее ответвлений (у меня Mint), то вместо `UBUNTU_CODENAME`  надо вставить `VERSION_CODENAME`.
4. Устанавливаем Docker:
```sh
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
5. Контрольный выстрел:
```sh
sudo docker run hello-world
```

#docker #linux 