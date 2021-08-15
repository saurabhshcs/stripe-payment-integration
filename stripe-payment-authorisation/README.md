## Authorizations
> Learn how to handle authorization requests.
> When a card is used to make a purchase, an authorization request is made which is approved or declined based on the following steps:

- Stripe checks that the Issuing balance has sufficient funds, that the card is active, and that your spending controls allow the authorization
- Stripe sends an issuing_authorization.request webhook event, letting you know we’re awaiting a decision about an authorization
- Before closing the issuing_authorization.request event, you can approve or decline the authorization
- If you do not approve or decline the authorization within 2 seconds, Stripe uses your default settings to approve or decline the authorization
- Stripe sends an issuing_authorization.created webhook event, letting you know the Authorization has been created

Follow me on - [Medium](https://saurabhshcs.medium.com) | [Linkedin](https://www.linkedin.com/in/saurabhshcs/) | [YouTube](https://www.youtube.com/channel/UCSQqjPw7_tfx1Ie4yYHbcxQ?pbjreload=102) | [StackOverFlow](https://stackoverflow.com/users/10719720/saurabhshcs?tab=profile)
