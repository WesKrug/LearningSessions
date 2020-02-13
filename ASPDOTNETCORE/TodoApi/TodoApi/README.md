ASP.NET CORE Tutorial
https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-3.1&tabs=visual-studio

Goes through creating a model, a Context, and then linking those up to an Entity Framework API Controller

Goes over basic CRUD operations included standard HTTP return types

Uses Postman to interact with the API (disable ssl certificate validation. Don't forget to reenable it when you're done!):

Once you have the API running, open up postman and make a GET request against the https://localhost:44375/api/TodoItems endpoint to see all of the TodoItems in the InMemory database.
Use an HTTP Post with the json body
```json
{
    "name": "walk dog",
    "isComplete": true
}
```
to create a TodoItem.

ASP.NET CORE will add a `Location` header to any successful (201) POST requests. Check the response headers for the `Location` header. 
There should be a url like https://localhost:44375/api/TodoItems/1. If you make an HTTP GET request against that url, it will return this specific entity you just created.
