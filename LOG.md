# Debug log

## CC-09 — "An old coupon still works"

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
