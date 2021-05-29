# mongoexport

> Produce exports of data stored in a MongoDB instance formatted as JSON or CSV.
> More information: <https://docs.mongodb.com/database-tools/mongoexport/>.

- Export documents in JSON format to stdout:

`mongoexport --uri={{mongodb_uri}} --collection={{collection_name}}`

- Export documents that match with a query to a JSON file:

`mongoexport --db={{database_name}} --collection={{collection_name}} --query="{{query_object}}" --out={{path/to/file.json}}`

- Export documents to a JSON array instead of one object per line:

`mongoexport --collection={{collection_name}} --jsonArray`

- Export documents to a CSV file:

`mongoexport --collection={{collection_name}} --type={{csv}} --fields="{{field1,field2,...}}" --out={{path/to/file.csv}}`

- Export documents that match the query in the specified file to a CSV file, omitting a list of field names on first line:

`mongoexport --collection={{collection_name}} --type={{csv}} --fields="{{field1,field2,...}}" --queryFile={{path/to/file}} --noHeaderLine --out={{path/to/file.csv}}`

- Export documents in human-readable JSON format to stdout:

`mongoexport --uri={{mongodb_uri}} --collection={{collection_name}} --pretty`

- Display help:

`mongoexport --help`