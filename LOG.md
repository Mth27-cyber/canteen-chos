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
