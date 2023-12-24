Create Kraft with monitoring and unit-test

1. Create a Kraft node (broker & controller mode) - Confluent Community 7.5.2
2. Setup open-source monitoring - Kafdrop
3. Unit test with sample Node JS producer & consumer script

Steps: 
./bin/kafka-server-start ./etc/kafka/server.properties
![image](https://github.com/amitsahu07/Setup-Kraft-MacOS/assets/32631010/d4cc332c-1826-440d-81dc-bd006518d296)

java --add-opens=java.base/sun.nio.ch=ALL-UNNAMED -jar kafdrop-4.0.1.jar --kafka.brokerConnect=localhost:9092 &
![image](https://github.com/amitsahu07/Setup-Kraft-MacOS/assets/32631010/b2d56b06-eae0-40b1-a648-5bc04db407d9)

brew install npm
npm install kafkajs
npm install -g npm@10.2.5
node kafka-test.js
![image](https://github.com/amitsahu07/Setup-Kraft-MacOS/assets/32631010/b82d2a88-ec68-41da-b516-b00bd8e09a63)

Kafdrop endpoint: http://localhost:9000/
![image](https://github.com/amitsahu07/Setup-Kraft-MacOS/assets/32631010/2f6a1c0c-c713-4a5b-8b11-ee32a5312ec6)
