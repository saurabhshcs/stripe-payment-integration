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
