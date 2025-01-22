#Modifications made

## /cart/init
### The code has been updated to reduce the number of database requests:

### Batch Product Fetching:

### Collected all product IDs from the cart in a single loop.
### Used a hypothetical get_products_by_ids method to fetch all products in one call.
### Mapping for Efficient Access:

### Created a dictionary (products_map) to map product IDs to product objects, reducing repetitive lookups in the get_cart function.
### These changes minimize redundant computations and database requests. 

## /product/init

###Changed the function list_products:
###optimizes performance by leveraging a list comprehension, which is faster than a traditional loop because it is implemented at the C level in Python. 
###It avoids the overhead of repeatedly calling append() on the result list, making the code both memory-efficient and faster in execution.
