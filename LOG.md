# Debug log

## CC-08 — "An old coupon still works"

**Reproduced:**
"FRESHERS24 was last year's offer and it expired ages ago. Someone used it yesterday and got the discount?!!"

**Cause:**
There was no function that decides whether the used coupon is expired or not

**Fix:**
i have added a if condition so that if the coupon code expiry date have been passed the coupon will be expired

**Checked:**
 I have entered FRESHERS24 in coupon code it now shows the coupon is expired
**Time:**
about 20 minuted debug the js file and analyse the code after that adding a if condition and then checking if the condition works fine now

## CC-06 — "I ordered more than they had"

**Reproduced:**
"The counter says only 2 samosas were left but it let me order 5, and the order went through fine. When I got there they only had 2?"

**Cause:**
there was no parameter to check the quantity left or can be ordered

**Fix:**
in availability.js i have added a parameter qty for checking quantity
in validation.js added qty in blockedReason function 
in reserve.js i have  changed reserve stock function in that i have changed the error condition
in menu.routes.js added parameter qty for checking quantity
**Checked:**
 I have set limit of samosa to 2 and try to order3 but now it will show error
**Time:**
about 2 hrs chceking and debugging files and one after other i was getting erros like all items got sold out the condition of stock when stock is 2 i was able to order3 after that i hve checked most files then do the necessary changes
## CC-07 — "Cancelling makes it worse"

**Reproduced:**
"A student cancelled an order and the number of plates we have left went down again instead of coming back. Do that a few times and the system thinks we have none left when the kitchen is full"

**Cause:**
in cancellation the quantity was get decrease because we reduce the qqty from stock 

**Fix:**
in validation.js in release notes i have changed - to + such that when order get cancelled the qty goes back to stock

**Checked:**
 I have ordered samosa and then cancelledit the qty goes back to stock
**Time:**
about 10 minutes as  i have corrected it previous commit while debugging the CC-06 Problem