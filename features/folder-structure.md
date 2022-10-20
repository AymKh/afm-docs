# 🔫 Folder Structure

Each folder / file has the following interface

```javascript
{
    name: string,
    template: string,
    parent: number,
    type: string,
    id: number,
    lastModified: Date,
    detailedDate: Date,
    url: string
}
```

A valid entity would look like this

```javascript
{
    "name": "CV",
    "template": "N.A", // entity.type === folder
    "parent": 0,
    "type": "folder", // or "file"
    "id": 1,
    "lastModified": "10/14/2022",
    "detailedDate": "Oct 14, 2022 1:34 PM",
    "url": "https://FIREBASE_URL" // files only
}
```



Folders with "0" as parent will be displayed within the most outer level (home view).

Once a folder is clicked, a query param will be passed, which is the folder's id.

The current view will refresh displaying the all entities which parent === the current id passed as the query param.
