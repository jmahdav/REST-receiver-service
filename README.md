REST-receiver-service
=====================

 
;;writing test for the REST receiver service

when ((Authentication == off || Authentication : true),
	  Key-Attribute != empty,
	  number-of-events (< 100)     ;; if not, it will Exceeded rate limit
	  
    ;;when syntax is correct and follows the following form 
    when ( , is at the end of the all lines except the last one,
    		all the contents are inside the { }
    		left content is inside the " ",
    		right content is inside the " ",
    		left contents are separated by : from right sides 
    	)
 
)

 ;; timeout and contributing maybe should be considered here 
 
 when (syntax != true || key-Attribute = empty ||  (Authentication = on  &  Authentication = empty ) ||  (Authentication = on  & Authentication : false ) ||  number-of-events > 100 )
    println ("an error has occurred")
