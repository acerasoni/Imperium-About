# Introduction 

Imperium is a subscription management platform. It has been developed for my Undergraduate Dissertation project during 2019/20 at the University of Nottingham. 

The system allows customers to subscribe to online services and control their subscription status (including suspension and deletion) directly from the Android application. 

The solution integrates seamlessly into eCommerce websites, and provides merchants with a payment portal through which they can bill their customers. The foremost focus of this project is the security of cardholder data, therefore this system implements payment tokenization and encrypts all data on the customer's device. 

The project is currently under beta phase development and is not yet available for usage. For business enquiries, contact [business.imperiumapp@gmail.com](mailto:business.imperiumapp@gmail.com)

Take me to:  
[Android Application](#aa)  
[Merchant Integration](#mi)  
[Payment Portal](#pp)

# <a name="aa"></a>Android Application

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

## Statistics

The application provides overall statistics including monthly spending and a pie chart of subscription prices.

![Stats](https://user-images.githubusercontent.com/32521086/87017173-f0c42980-c1cf-11ea-9710-2f18e74538bb.png)

# <a name="mi"></a>Merchant Integration

Merchants must setup the Sync Up page in their subscription process. They may do so through the use of a simple client-side SDK that will create the input field and handle all necessary network requests. As good practice, the merchant should display the outcome of the sync up attempt.

![SyncUp](https://user-images.githubusercontent.com/32521086/87015372-a0e46300-c1cd-11ea-8f01-0b78bf0eb665.png)

# <a name="pp"></a>Payment Portal

Merchants can bill their customers through the payment portal. They can select a One-Time or Recurring options for the amount entered. The JSON response body will display the outcome of the transaction. The transaction are implemented through authorized payment tokens. This means that the card details are never exposed, and that only authorized merchants can utilize the payment tokens assigned to them.

If a customer pauses or deletes their subscription, this will immediately impact transactions attempted from the merchant. Below is the outcome shown when a subscription has been paused.

![Payment](https://user-images.githubusercontent.com/32521086/87017443-44cf0e00-c1d0-11ea-8225-c08e11025c9d.png)

### Legal Disclaimer: I claim no copyright on any trademarks shown above, including Visa, MasterCard and Netflix logos. These companies do not endorse the product in any way, and their logos have been used for purely expository purpose.
