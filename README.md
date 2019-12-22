Most of the time I use Dapper (in some form or another, mainly through my [Postulate](https://github.com/adamosoftware/Postulate) library or [Dapper.CX](https://github.com/adamosoftware/Dapper.CX) library) for all data access. Sometimes, I need to use ADO.NET DataTables for really dynamic things, such as in my [SqlIntegration](https://github.com/adamosoftware/SqlIntegration) project. The syntax for querying DataTables isn't terribly convenient, so that's why this library exists.

Nuget package: **DataTables.Library** (formerly AdoUtil.Library)

Version 2.x of this library offers these extension methods:

- [QueryTable](https://github.com/adamosoftware/DataTables.Library/blob/master/DataTables.Library/SqlConnectionExtensions.cs#L11) `(this SqlConnection)`
- [QueryTableAsync](https://github.com/adamosoftware/DataTables.Library/blob/master/DataTables.Library/SqlConnectionExtensions.cs#L24)`(this SqlConnection)`
- [ToDataTable](https://github.com/adamosoftware/DataTables.Library/blob/master/DataTables.Library/IEnumerableExtensions.cs#L13)`(this IEnumerable<T>)`

The `Query-` methods support Dapper-style anonymous object parameters, as seen [here](https://github.com/adamosoftware/AdoUtil/blob/master/Testing/QueryTableTests.cs#L29) and [here](https://github.com/adamosoftware/AdoUtil/blob/master/Testing/QueryTableTests.cs#L49). You can also pass a dictionary as query parameters, as seen [here](https://github.com/adamosoftware/AdoUtil/blob/master/Testing/QueryTableTests.cs#L59) and [here](https://github.com/adamosoftware/AdoUtil/blob/master/Testing/QueryTableTests.cs#L72).

The version 1.x library has some other methods I never really used, and the parameter handling wasn't very pretty. Version 2 boiled it down to essentials, added tests, and improved parameter handling.
