# Introduction 

Imperium is a subscription management platform. It has been developed for my Undergraduate Dissertation project during 2019/20 at the University of Nottingham. 

The system allows customers to subscribe to online services and control their subscription status (including suspension and deletion) directly from the Android application. 

The solution integrates seamlessly into eCommerce websites, and provides merchants with a payment portal through which they can bill their customers. The foremost focus of this project is the security of cardholder data, therefore this system implements payment tokenization and encrypts all data on the customer's device. 

# Android Application

## Adding a card

The Android application can be used to manage subscriptions and generate Sync Codes, which can be entered on a merchant's website during the subscription process. 

You must first add a card through the Add Card screen. The application is integrated with Google Wallet, so that you may automatically populate the card data. 

![AddCard](https://user-images.githubusercontent.com/32521086/87012507-aa6bcc00-c1c9-11ea-94c4-5a1bb6b8a17e.png)

The card data is encrypted on the mobile device with a unique encryption key. It is then sent to the backend through a HTTPS-secured connection and irreversibly replaced with payment token.

## Subscribing to a merchant

Next, you can generate a Sync Code to enter on the merchant's website during the subscription process.

![SyncCode](https://user-images.githubusercontent.com/32521086/87013502-097e1080-c1cb-11ea-823b-45611eadff6e.png)

## Managing your subscriptions

You can view your subscription status and details. You may suspend or delete the subscription instantly, although the merchant will be immediately notified.

![Manage](https://user-images.githubusercontent.com/32521086/87014417-67f7be80-c1cc-11ea-8adb-7cb176d4ac92.png)
