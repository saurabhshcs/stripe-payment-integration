FROM java:11

EXPOSE 9006

ADD target/stripe-payment-authorisation.jar

ENTRYPOINT ["java", "-jar", "stripe-payment-authorisation.jar"]