!SLIDE 
# Craft 1933 #

!SLIDE bullets incremental
# The Use Case #

* Flash Sales Site
* User has 10 minutes to complete purchase.
* If user doesn't purchase, items are removed from cart.
* Timeout and cleanup should happen even if user leaves session.

!SLIDE bullets incremental
# The Set Up #

* Magento is already validating the quote on each page load.
* Active browsing no problemo.

!SLIDE bullets incremental
# The Problem #

* Users abandoning the session.
* No page load... no cart validation.
* Need a cleanup process!

!SLIDE bullets incremental
# The Problem #

* "I need a cup of coffee."
* "Mmmm.. wine. Great idea!"
* "Squirrel!"

!SLIDE 
# Possible Solutions #


!SLIDE bullets incremental
# Polling Cart Items #

* Query quote items table for expired items.
* Timeout if old quote found.

!SLIDE bullets incremental
# Polling Cart Items #

Advantages

* The "traditional" way
* Easy - just set up a cron.

!SLIDE bullets incremental
# Polling Cart Items #

Disadvantages

* Will never be real time
* Resource Intensive
* "I feel dirty"


!SLIDE bullets incremental
# Event Driven Model with Node.js #

Advantages

* Real time
* Very lightweight
* Familiar. We know JavaScript
* Bling! Bling!

!SLIDE bullets incremental
# Event Driven Model with Node.js #

Disadvantages

* Fledgling Technology
* Documentation?
* New service to support

!SLIDE 
# Decisions #

* Eventing is the better way
* Progressive client
* Not a "mission-critical" service.
