# Managing your documents

### Listing all documents
```
GET /documents

Auth: YOUR_AUTH_TOKEN
```


### Create new document
```
POST /document/new

Auth: YOUR_AUTH_TOKEN
```

This simply creates a document entry under the user in our database. Title and contents are set through the [edit document section](#edit-document). 

This request returns the id of the document.


### Edit document
#### Content
```
POST /document/edit/:document_id

Auth: YOUR_AUTH_TOKEN


{
    "target":"content",
    "content": LATEX_CODE
}
```

#### Name
```
POST /document/edit/:document_id

Auth: YOUR_AUTH_TOKEN


{
    "target":"name",
    "content": NAME
}
```

### Read document
```
GET /document/:document_id

Auth: YOUR_AUTH_TOKEN
```

### Delete document
```
POST /document/:document_id/delete

Auth: YOUR_AUTH_TOKEN

```

### Share document
```
POST /document/:document_id/share

Auth: YOUR_AUTH_TOKEN

{
	"invited": EMAIL,
	"role": "editor" | "reader"
}
```
