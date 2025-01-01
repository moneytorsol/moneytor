
# 👁️ Moneytor

An advanced real-time monitoring tool for pump-fun tokens, designed to help traders focus on the top-performing coins. In the future, we'll offer websocket access for developers to customize their experience.

## 🌟 Key Features

### X.com Account Watcher

-   Track multiple accounts effortlessly with a customizable watchlist.
-   Set time limits to narrow down the best opportunities.
-   Receive real-time notifications for high-potential tickers as soon as they launch.
-   Experience low-latency tracking for rapid insights.
-   Developers can connect to the main websocket and integrate their own logic for enhanced automation.

## 🛡️ Roadmap

-  Send alerts to Discord and Slack when a ticker meets your defined conditions.
-  Configure the cloud version across multiple regions for better performance and scalability.
-  Contribute to and customize the project by accessing the open-source code.
-  Learn how to build the project locally and integrate with multiple APIs with our step-by-step video guide.
-  Expand support beyond "pump"-ending contract addresses to include all pump.fun tokens.
-  Replace AWS's SNS x SQS stack with Google Cloud Pub/Sub for more robust messaging.
-  Offer a fully managed Moneytor (utilizing the cloud) for traders that are allergic to dev tasks.
-  Python and JavaScript SDK to consume Moneytor's backend.

## 🛠 Technologies Used

- **Blockchain**
  - Solana Web3.js
- **Tools**
  - Websockets
  - SNS x SQS 
  - Utilizing multiple API's (e.g https://react-tweet.vercel.app/api-reference)
  - Dedicated Node to run the main Moneytor backend (currently running in Frankfurt)

- **Social Media**
  - Twitter API v2
  - Discord.js
  - Message Queue System

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/moneytorsol/moneytor.git

# Install dependencies
cd moneytor/app
npm i

# Setup environment variables 
cp .env.example .env
```
## 📦 Deployment

```
Coming soon... 
```
## ⚙️ Configuration

Create a `.env` file with:

```env
MONEYTOR_API_KEY=yourMoneytorApiKey
MONEYTOR_API_SECRET=yourMoneytorApiSecret
PUBLIC_PUMPFUN_WEBSOCKET_STREAM=
AWS_ACCESS_KEY_ID=yourAWSAccessKeyID
AWS_SECRET_ACCESS_KEY=yourAWSSecretAccessKey
AWS_REGION=useTheClosestRegionFromYouForBetterLatency
SNS_TOPIC_ARN=yourTargetSNSTopicARNWhereTheMessagesAreGonnaBePublished
QUEUE_URL=yourSQSQueueURLWhereYoureGonnaPollTheMessagesFrom
```

## 🚀 Usage

```bash
# Run in development mode (locally = best latency)
npm run dev
```
## 📊 Architecture
- **Main page flow (/)**
https://cdn.discordapp.com/attachments/1323702889012658278/1324094463638769715/image.png?ex=6776e690&is=67759510&hm=e00ccc905e11bf7db0345679a091b1f2b3b0bb6e5dfa18bfaa2b848d625407c3&
- **Moneytor page flow (/moneytor)**
https://cdn.discordapp.com/attachments/1323702889012658278/1324096700536852550/image.png?ex=6776e8a5&is=67759725&hm=45e34a90cb349f565db845bd83bc76ce3e73e534cdb0642d10ef0460a3929b7e&

## 🛡️ Security

- IP Authorizing mechanisms.
- Rate limiting.
- Session issuing.
- Each client got a seperate session and websocket connection.

## 📜 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

---

Built with ❤️ for the pump.fun trading community.
