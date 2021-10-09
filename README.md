I have created a simple e-commerce application using Spring Boot, Thymeleaf and Stripe's APIs.
The simple e-commerce application is built in Java and the reason I have chosen Java is because
I feel much more comfortable even though I have experience in other languages such as Kotlin, Scala, Python, NodeJS, C/C++ and many more.

First of all, I would want to emphasize that I have never used the Stripe APIs before and it was extremely easy to understand the APIs which are also well documented.

The stack that I felt most comfortable in order to accomplish this in few hours is composed of the listed above technology tools such as Spring Boot and Thymeleaf.

The structure of the code is segregated into packages starting with com.theagileside with child packages named controller which hosts the controllers such as ChargeController and CheckoutController. Dedicated package for StripeService which acts as a proxy to the Stripe APIs.

The complete working solution source code is located at:
https://github.com/naimimami/stripe-example

In the application.properties file you can change the server.port = 8084 to the port of your choice.

-	After running the StripeApplication open a web browser of your choice and type http://localhost:8084/
-	Click on the button Pay with Card
-	Enter email
-	Enter Card Number (can select test card numbers from the Stripe site)
-	Enter MM/YY (as long as it is a future date)
-	Enter CVC (any three digits)
-	Finally Click on the Pay button

Stripe API used is the charge.
In subsequent versions we can add other functionality such as retrieving payment, updating payment, and others.

The way I have approached the problem first I have developed the html and the controllers which the UI is supported and then created the StripeServices proxy which acts as a wrapper to the Stripe APIs.

Note: I have also followed the steps in creating the Stripe Public and Secret Keys, which are placed in the configuration file only for the demo.
