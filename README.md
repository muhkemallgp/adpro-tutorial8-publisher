#### Nama : Muh. Kemal Lathif Galih Putra
#### NPM : 2206081225
#### Kelas : ADPRO - A
#### ASDOS : REN

## TUTORIAL - 8 - PUBLISHER

### Refleksi
1. Try to answer the following questions, and write the answer in the and new file readme.md in
you repository.

    #### a) How many data your publlsher program will send to the message broker in one run?
    
    Program _publisher_ akan mengirimkan 5 pesan data ke pialang pesan dalam satu kali jalankan. Hal ini karena ada 5 panggilan metode publish_event, masing-masing memublikasikan sebuah instance UserCreatedEventMessage.

    #### b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

    URL "amqp://guest:guest@localhost:5672" sama di kedua program _publisher_ dan _subscriber_, yang berarti keduanya terhubung ke instance pialang pesan yang sama yang berjalan di localhost dengan port 5672. 
    
    Ini berarti bahwa _publisher_ dan _subscriber_ sedang berkomunikasi melalui pialang pesan yang sama, memungkinkan mereka untuk bertukar pesan dengan lancar.

### RunningRabbitMQ
![alt text](assets\RabbitMQ.png)

### ProcessingEvent (Concole SS)
![alt text](assets\ConsoleRunning.png)


Ketika message broker seperti RabbitMQ sedang aktif, setiap kali kita menjalankan program Subscriber dan Publisher (dengan perintah cargo run), Publisher akan mengirimkan data ke broker pesan, yang kemudian diterima oleh Subscriber. Dari ilustrasi yang diberikan, terlihat bahwa Publisher mengirimkan data sekali ke broker pesan dan kemudian Subscriber menerima data tersebut. Dengan kata lain, dalam proses ini, Publisher bertindak sebagai pengirim data, sedangkan Subscriber berperan sebagai penerima.