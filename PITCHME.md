# Load Testing with Gatling
![Gatling Logo](images/gatling.png)

Doug Fitzmaurice - Ents24 Ltd

---

## Motivation

+++

Moving from this:

+++

To this:

+++

* How do we ensure stability?
* How many users can we handle?
* What is response time like under load?
* Have we missed any common packages?

---

## Gatling?

* Users, not URLs
* Tests written in Scala
* Actor model - high concurrency from one machine
* Great control over traffic levels
* Test recorder
* Visual result summaries

---

```scala
atOnceUsers(20)
rampUsers(10) over(20 seconds)
```

---

## Log Replay

* Parse web server logs
* Produce CSV file of URLs
* Produce traffic profile:
    * How many users?
    * How many requests each?
    * How much gap between requests? 
    * How many arrive at once?
    * How many requests per second?
