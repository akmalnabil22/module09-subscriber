1. What is `amqp`?  
    `amqp` adalah protokol yang memungkinkan aplikasi untuk berkomunikasi dengan mengirim message melalui broker. `amqp` digunakan untuk menghandle komunikasi asynchronous antara publisher dan subscriber pada tutorial ini.  


2. What does it mean? `guest\:guest\@localhost:5672` , what is the first `guest`, and what
is the second `guest`, and what is localhost:5672 is for?  
    `guest\:guest\@localhost:5672` merupakan URI untuk melakukan koneksi dengan server AMQP seperti RabbitMQ. `guest` pertama merupakan username dan `guest` kedua merupakan password yang digunakan untuk autentikasi server RabbitMQ.



![](./img/slow%20subscriber.png)  
Sekarang subscriber akan memakan waktu untuk menerima sebuah pesan. Karena publisher mengirim pesan dalam satu waktu ke broker, maka broker akan membuat antrian pesan yang akan diterima subscriber. Semakin banyak pesan yang dikirim maka semakin banyak juga antrian pesan.