# Deployment (Dağıtım)
Docker - Kubernetes-Heroku Notes

### Monitoring 
Hangi url ne kadar istek geldi vs vs.
### Docker
"Konteynerleştirme" olarak da bilinen işletim sistemi seviyesinde sanallaştırma sağlayan bir bilgisayar programıdır
### Container
Kendilerine ait prosesleri, servisleri ve ağları vardır.

Container yönetimi oldukça zor ve low level bir iştir. Docker bu işi kolaylaştırmak için high level bir çok araç sunar.

![image](https://github.com/cengarm/Deployment/assets/126611512/3e8bc248-cea9-46dd-b9c0-7a6d62707c17)

# Container vs VM
Container > VM
![image](https://github.com/cengarm/Deployment/assets/126611512/f667d84f-0383-4b49-b58a-f435f88a782c)

# Container , Image
![image](https://github.com/cengarm/Deployment/assets/126611512/d08d61a7-100f-4898-be6d-0464fb0d7c71)
![image](https://github.com/cengarm/Deployment/assets/126611512/e6249b14-eeaf-44c1-918a-b8311a999f1d)

# Docker ne işe yarar
* Bilgisayara veya sunucuya kurmadan uygulamayı çalıştırmamıza yarar.
* Geliştiriciler ile DevOPS arasında herhangi bir iletişime ihtiyaç kalmamasını sağlar.
* 3 farklı işletim sisteminde aynı ortamda çalışmasını sağlıyor
![image](https://github.com/cengarm/Deployment/assets/126611512/20d134e6-47da-4d8c-b4e9-08cd93311465)

# cmd kodları:
### docker pull ubuntu --> docker pull * cmd üzerinden imagelerin dowland etmemize yarıyor.
### docker run ubuntu  --> localde image bulursa direk çalıştırıyor. Yok ise önce indirip çalıştırıyor.
### docker run ubuntu sleep 3 --> 3 saniye çalıştırıp kapatır.
### docker run -it ubuntu --> ubuntunun içerisine girmemize yarar. Çıkış için exit dememiz yeterli.
### docker container ls -a --> görev yöneticisi gibi açık ve kapalı olanları gösteriyor.
### docker ps --> açık olanları gösteriyor.
### docker run -it --name bash_ubuntu ubuntu --> ubuntunun namesini bash_ubuntu yaptık.
### docker start containerName : isimden çalıştırabiliriz. Arka planda çalışmaya devam ediyor.
### docker stop containerName : durdurmamıza yarıyor Arka planda çalışmıyor. 
### docker stop Id: id girerekte kapatabiliriz.
### docker images --> indirdiğimiz tüm imageleri gösteriyor.
### docker rm contreiner id veya name yazabilirsiniz. --> rm remove anlamına geliyor.
### docker container rm$(docker container ls -aq) --> tüm idleri bize veriyor. ve id üzerinden hepsini siliyor.

# Port Mapping 
![image](https://github.com/cengarm/Deployment/assets/126611512/4d8880a4-e6b8-4715-af53-96524197a0dc)

# Volume Mapping
![image](https://github.com/cengarm/Deployment/assets/126611512/14522e01-8c80-4fd9-80f9-3d872f03a520)

# Docker Network Türleri
![image](https://github.com/cengarm/Deployment/assets/126611512/a0af88ba-f01e-4f3f-8332-93e867ecb4a2)
