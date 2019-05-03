# ![alt text](https://assets.breatheco.de/apis/img/images.php?blob&random&cat=icon&tags=breathecode,32) SMS Queue Management System

Lets create a Queue System: Queue system are heavily used in Goverment institutions, airports, banks and many other venues looking to organize the incoming traffic.
Queue systems can also be used to load balancing for different applications like:
- Stablishing priorities in web servers incoming requests.
- Inmigration and visa applicantions that need to be prioritized.
- Network packages.
- etc.

## 📝 Instructions

Create an API that allows clients to manage a simple Queue

3. The API receives a request tp add Bob into the queue with any particular priority (FIFO or LIFO).
3. The API ads Bob and notifies him with an SMS confirmation, the SMS must say how many people are in front of him on the line.
4. The system now waits until the enpoint `GET /next_in_line` gets executed to process the person on the queue.
5. Every time a `GET /next_in_line` request is received, the next person on the queue gets processed until it is Bob's turn.
5. When Bob is processed, the system sends him another SMS to let him know that his turn has arrived and deletes him from the list.

## More details

1. You have to create 3 endpoints for your API:

POST /new_in_line: Will recive information about a user and ad him into the queue.
GET /next_in_line: Will process one spot of the queue.
GET /all: Will return a list with everyone that is pending to be processed (the current queue)

## 📖 Fundamentals

This exercise will make you practice the following fundamentals:

1. Here you can find the information on [how to send an sms with twillio](https://www.twilio.com/docs/sms/send-messages), you will have to register and account (free) and also register a number (free)
4. Building an RESTful API
5. Complex Data Structures.
6. Queue (FIFO vs FILO)
7. SMS.