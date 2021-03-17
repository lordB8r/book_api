# BooksApi

> Based on the tutorial found here: https://www.dairon.org/2020/07/06/simple-rest-api-with-elixir-phoenix.html

  * Install dependencies with `mix deps.get`
  * Create and migrate your database with `mix ecto.setup`
  * Start Phoenix endpoint with `mix phx.server`

Visit [`localhost:4000`](http://localhost:4000)

You should see 
```{"errors":{"detail":"Not Found"}}```

Navigate to [`localhost:4000/api/books`](http://localhost:4000/api/books) to see the list of books in your database

Use curl to add more books with the following command: 

```
curl -X POST -H "Content-Type: application/json" \
    -d '{"book": {"title": "Whale huntng", "isbn": "9-2134q523-23532-235", \
    			  "price": 11.10, "description": "jobs left for less boring people",\ 
    			  "authors": ["Alfred Neuman", "Abraham Lincoln"] }}' \
    http://localhost:4000/api/books
    ```