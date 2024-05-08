# Tutorial-10
---
#### Nama: Naufal Ichsan
#### NPM: 2206082013
#### Kelas: Adpro A
---
### Refleksi
#### 2.1. Original code of broadcast chat.
#### Server
![server](assets/images/server.png)
#### Client 1
![client 1](assets/images/client1.png)
#### Client 2
![client 2](assets/images/client2.png)
#### Client 3
![client 3](assets/images/client3.png)

Setelah server dijalankan dan 3 client mengirimkan pesan, dari output di atas dapat terlihat bahwa setiap client dan juga server menerima siaran obrolan dari setiap client. Setiap kali seorang client mengetikkan pesan di baris perintah, string tersebut akan dikirim ke server dan server akan terus mengirimkannya ke semua client yang terhubung dengannya.


#### 2.2. Modifying the websocket port
Apabila port client dan server sama, maka aplikasi dapat berjalan dengan lancar
#### Client
![client same port](assets/images/client-sameport.png)

#### Server
![server same port](assets/images/server-sameport.png)


Namun, jika misalnya kita hanya mengubah salah satu port, misalnya port server menjadi 8080 dan port client tetap 2000, maka akan terjadi error pada client karena menurut client port tersebut tidak memiliki koneksi

#### Client
![client different port](assets/images/client-differentport.png)

#### Server
![server different port](assets/images/server-differentport.png)


#### 2.3. Small changes. Add some information to client
![serverside](assets/images/serverside.png)
![clientside](assets/images/clientside.png)
**server code changes**
![codechanges-server](assets/images/codechanges-server.png)
**client code changes**
![codechanges-client](assets/images/codechanges-client.png)
Perubahan tersebut dilakukan agar ketika bcast.tx ke semua client menyertakan alamat pengirim teks melalui variabel addr.
