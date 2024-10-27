# Data Structure, Algorithms in C++

It’s implied in all of the following assignments that you:
- Follow the C++ core guidelines
- Organise the code into classes, making use of RAII and writing the most clean, predictable and efficient code that you can come up with
- Have a relatively easy build process with low chances of build failure due to, say, a library not being found (look into CMake FetchContent or Conan)
- Ideally, use modern C++20 (and above) features
- Make use of generics
- Make use of multithreading techniques where you see fit
- Don’t overuse features provided by the standard library
- Don’t overcomplicate the code
- Format the code uniformly using reasonable and readable guidelines
- Use Conan or CMakeLists.txt for the project
- For the best results and the least amount of headache, we recommend using clang-tidy and clang-format.

Implement either 1 of the 1-4 challenge assignments. Implement 4 and it's a direct hire (pending interview with CEO).

## 1. Location Tracking System

Design and implement two micro-services in C++, one that uses WebSockets to get location data from multiple clients, labels it and sends it to a Kafka broker and another micro-service (Iterates!) consumes said data and inserts it into a SQL or NoSQL DB of your choice and has a CLI interface to interact with the DB in order to retrieve the data via a simple interface. Note that in a real life scenario, the location data tends to be a lot when you have about 10,000 users as you might be able to guess, so making this kind of a program scaleable from the start is crucial. The Kafka technique may not be the best but is mandatory to test your knowledge of the system.

## 2. Chat Application: Design a chat application

with high write throughput to be used by thousands of users using append only databases (such as red panda/kafka, since that is what we use :wink:). Assuming that your application is web based, what kind of technologies would you use so that the server can communicate with the client when it receives new data (for example, a text message being sent). You may also use a SQL database, or any other technology to aggregate the data you receive from your append only database. Also outline the programming language you would use in each part of your system and explain why. Detail the different parts of the application, what data is important to be sent through Kafka/Red Panda, and what data can you derive from them.

## 3. OHLC Trading System 

In a modern online trading, we know the concept of OHLC with Volume & Value to indicate a stock’s performance in real-time, this concept is highly leveraged by investors to guide their investment decisions. The nature of the data is small but moving ultra-fast, we can’t afford to delay a single second. Worry not, in this challenge, we only provided you a tiny subset of the real data. A crash-course of terminologies used in this challenge for you: Stock: a tradeable equity OHLC: stands for Open High Lowes Price Close Price: the very last price of today Previous Price: the Close of the previous day Open Price: the first price of today Lowest Price: the lowest price that is ever archived today Transaction: Elements of a transaction are Quantity and Price. Quantity and Executed Quantity are the same. Price and ExecutionPrice are the same Volume the sum of quantity Value the sum of (quantity * price) Average Price: is value / volume
Given Transaction inside a bunch of .ndjson from rawdata.zip. Calculate OHLC with Volume and Value
Convert OHLC to protobuf and send the protobuf to another service called consume OHLC.
In consumer you can save in a database like redis or whatever
And inside the consumer create the gRPC server that will give client data based on stock

## 4. Direct Hire Question. Crypto Exchange (might be hard): Design a cryptocurrency exchange

with high write throughput exchange to be used by thousands of users using append only databases (such as red panda/kafka, since that is what we use :D). Assume that your application is web based, since the application is a cryptocurrency exchange user’s need to receive live data on the state of their orders, state of their orderbook and data on last traded prices. What kind of technologies would you use so that the server can communicate with the browser client, so that the client can have the most up to date data. SQL or NoSQL databases may also be used to aggregate data you receive from the append only database. Also outline the programming language you would use in each part of your system and explain why. Detail the different parts of the application, what data is important to be through Kafka/Red Panda, and what data can you derive from them. Bonus Questions: How might you scale the application? Increase the number of instances of the append only database? How would you balance load between your services? Assume that you have a tighter deadline. Would you change your choice of programming languages?


# Assembly Language and Compiler Optimization
- Use your C++ assignments
- Go to Godbolt.com
- Try to do optimization on your code and explain why

# Mathematics
- Explain in multiple paragraphs the Clay millennium problems.
- Please explain The Elliptic Curve Digital Signature Algorithm: ECDSA, as mathematically thorough as possible

# Probability and Statistics
- Please derive the probability density function and cumulative probability function of a 1) Gaussian distribution 2) Poisson Distribution 3) Uniform Distribution
- Please implement the probability density function and cumulative probability function of a 1) Gaussian distribution 2) Poisson Distribution 3) Uniform Distribution in Python

# Cryptocurrencies
- Explain in your own words what are cryptocurrencies?
- Explain what is zero-knowledge proofs? Give an example of a simple ZKP.
- Why do you want to work for Bitwyre?
