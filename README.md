![build code](https://github.com/bayramucuncu/B3.Extensions.Data/workflows/build%20code/badge.svg)
![nuget push](https://github.com/bayramucuncu/B3.Extensions.Data/workflows/nuget%20push/badge.svg)
# B3.Extensions.Data
B3.Extensions.Data includes data extensions for Entity Framework Core
## DbContextExtensions

## ExecuteQuery

Execute raw sql query without casting any type.
```csharp
public async Task<IActionResult> GetToplamMetraj()
{
   var sql = "SELECT type, SUM(length) FROM ways GROUP BY type";
   var queryResult = await _context.ExecuteQueryAsync(sql);
            
   return Ok(response);
}
```
