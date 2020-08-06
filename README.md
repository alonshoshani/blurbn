### Flight app

This microservice responsible manage flights, checkins, baggage and sales

![Alt Text](https://media.giphy.com/media/vFKqnCdLPNOKc/giphy.gif)

To easily running this microservice:
1. clone it :)
2. run `mvn clean install`
3. run `sh build_image.sh`
4. run `sh run_image.sh`


The microservice will run on your localhost and exposed on :80 port.
For querying the service do the following:

#### Checkins

Use the `GET` Method to check if check in exists, destinationId is numeric and bag is string.

`http://localhost/flights/checkin/destination/{destinationId}/baggage/{bag}`

#### Coupons

Use the `POST` Method to redeem your coupon.

`http://localhost/flights/coupon/redeem`

The body of the request should be as follow:
```
{ 
"couponId":3,
"price": 100
}
```

#### Tickets

For checking if ticket is available.

Use `GET` Method to check id ticket exists, ticketId should be numeric.

`http://localhostflights/tickets/{ticketId}/available`


Have a good flight!



