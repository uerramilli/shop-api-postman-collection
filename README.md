Useful OCAPI Shop API calls.
Download both api and environment postman collections and import into Postman workspace.

To make this solution work for your Commerce Cloud Sandbox, do the following:
1. Update host_server prop per your env on OCAPI Jaguars Env Vars collection
2. Update OCAPI_HOST prop per your env on OCAPI Jaguars Env Vars collection
3. Copy settings from https://github.com/uerramilli/shop-api-postman-collection/blob/master/ocapi-shop-settings.json into your Shop API OCAPI settings in BM.
4. Create a shopper account on your SFRA storefront site. The following credentials are used to generate registered customer JWT. 
   - Username:legend@sleepyhollow.com
   - Password:!20Summer

Sequence of OCAPI calls to create an order for a registered user in your sandbox:
1. Run 2a.Register new customer
2. Run 2b.Create basket for registered customer
3. Run 2c.Add item to basket for registered customer
4. Run 2d.Create order for registered customer
Note: If run into CustomerBasketsQuotaExceededException - The maximum number of baskets per customer was exceeded, then 
run 3a.Delete a basket 
