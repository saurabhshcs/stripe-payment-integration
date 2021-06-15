# stripe-payment-integration

## What is Stripe!
> https://stripe.com/docs/payments/checkout

This application of collection of couple of microservices, which is based upon online payment transaction modules.
- Payment Authorisation
  When customer make any online payment for an order then technically order amount is get blocked(Authorised) until order gets confirmed. 

- Payment Capture
  When customer's order has been confirmed then order amount gets captured (charged).

- Payment Refund
  When customer cancels that order then amount will be refunded but few payment service provider will charge to the online company for capture & refund both. 
  Note - it may different because it depends on the volume of the online transactions.

- Card Tokenisation
  When customer allows online company to save their cards into the my account section then card get masked and gets some random aplhanumeric encrypted value i.e. 
  called tokenisation 


## How intents work
> Learn about the status and lifecycle of PaymentIntents and SetupIntents.
> Asynchronous payment flows are complex to manage because they depend on customer interactions that happen outside of your application. PaymentIntents and SetupIntents simplify this by keeping track of the status of the payment or setup flow. The PaymentIntent and SetupIntent objects act as the single source of truth in the lifecycle of the flow.

```curl
curl https://api.stripe.com/v1/payment_intents \
  -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
  -d "amount"=1099 \
  -d "currency"="usd" \
  -d "payment_method_types[]"="card"
```

```java
// Set your secret key. Remember to switch to your live secret key in production.
// See your keys here: https://dashboard.stripe.com/apikeys
Stripe.apiKey = "sk_test_4eC39HqLyjWDarjtT1zdp7dc";

PaymentIntentCreateParams params =
  PaymentIntentCreateParams.builder()
    .setAmount(1099L)
    .setCurrency("usd")
    .addPaymentMethodType("card")
    .build();

PaymentIntent paymentIntent = PaymentIntent.create(params);
```


Follow me on - [Medium](https://saurabhshcs.medium.com) | [Linkedin](https://www.linkedin.com/in/saurabhshcs/) | [YouTube](https://www.youtube.com/channel/UCSQqjPw7_tfx1Ie4yYHbcxQ?pbjreload=102) | [StackOverFlow](https://stackoverflow.com/users/10719720/saurabhshcs?tab=profile)
