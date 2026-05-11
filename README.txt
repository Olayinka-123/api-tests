Exercise 1: Exploring the Products API

S/No	Endpoint	Expected Code	Actual Code	Note
1	https://dummyjson.com/products/1	200	200 OK	Pass
2	https://dummyjson.com/products/99999	404	404 NOT FOUND	"message": "Product with id '99999' not found"
3	https://dummyjson.com/products/0	Is 0 a valid ID?	"No
"	"404 NOT FOUND
""message"": ""Product with id '0' not found"""
4	https://dummyjson.com/products/-1	What status code and message?	404 NOT FOUND	 "message": "Product with id '-1' not found"
5	https://dummyjson.com/products/abc	What status code?	404 NOT FOUND	"message": "Product with id 'abc' not found"

Exercise 5: Pagination Deep Dive
S/No	URL	Question	Answer	
1	https://dummyjson.com/users?limit=10&skip;=0	What is the total?	208	
2		How many pages exist?	"21 Pages
"	"""total"": 208,
    ""skip"": null,
    ""limit"": 10

Math.ceil(total / limit)
=208/10
=28 Pages
"
