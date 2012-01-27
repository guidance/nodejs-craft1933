!SLIDE 
# Procrastinaor #

!SLIDE bullets incremental
# Procrastinator #

* Delay Queue
* VERY simple service
* Send it a message with a timeout value
* It will callback when time's up.
* No external business knowledge.


!SLIDE bullets incremental
# API #

* RESTFUL
* Simple Endpoints, HTTP verbs

!SLIDE code
POST http://127.0.0.1:8000/items
content-type: application/json

{ 
"callbackUrl": "http://127.0.0.1:8008/callback/item/{{id}}",
"interval" : 5000,
"data" : {"e":1, "a":0}
}


!SLIDE smbullets incremental
# In Action #

* User adds to cart.
* Magento handler sends message to Node.
* Node creates async timeout with callback URL.
* Times Up!
* Node pings callback url with data packet.
* Magento handles callback. 

