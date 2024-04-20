Nama    : Samuel Taniel Mulyadi
NPM     : 2206081805

a. How many data your publisher program will send to the message broker in one run?
Publisher program akan mengirimkan 5 data ke message broker dalam satu kali proses.

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
URL "amqp://guest:guest@localhost:5672" yang sama pada program pelanggan dan penerbit berarti keduanya terhubung ke broker pesan yang sama di localhost dengan kredensial default "guest:guest".

Screen of my running RabbitMQ
![Screen of my running RabbitMQ](images/rabbit.png)

Screen of subscriber terminal with 5 messages
![Screen subscriber terminal with 5 messages](images/subcsriber-publisher-terminal.png)
Screenshoot ini menunjukkan terminal subscriber dimana subsrciber berhasil menerima 5 event message broker dari publisher ditunjukkan dengan tiap kali melakukan cargo run di publisher.

Screen of rabbit spikes
![Screen rabbit when publisher is running](images/subscriber-publisher-rabbit.png)
Screenshoot ini menunjukkan spikes pada graf di rabbit ketika melakukan cargo run di publisher. Ditunjukkan ada spike pada publish dan consumer ack sebesar 1.00/s

Screen of slow subscriber simulation
![Screen rabbit when doing slow subscriber simulation](images/slow-subscriber-publisher-rabbit.png)
Screenshoot ini menunjukkan spikes pada graf di rabbit ketika melakukan cargo run di publisher berkali-kali disertai dengan perubahan pada subscriber dimana terdapat delay 1 second tiap proses.




