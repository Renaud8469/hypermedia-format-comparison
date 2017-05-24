# Notes

## Collection+JSON

### Pros

- Presence of a template to create another user
- Link to external resources "manager" and "team"
- URL template for a query

### Cons

- Embedded collection not included because it is another collection in itself
- Very verbose
- Not easy to convert from the original JSON object

### Additionnal notes

- Queries and templates, which add the most verbosity, are optionnal


## HAL

### Pros

- Link to external resources "manager", "skills" and "team"
- But possibility to keep the "skills" included
- Documentation links to help understand the "manager", "team" and "skills" notions as defined by the company
- URL template for a query
- Easy to convert from the original JSON object
- Easily human-readable

### Cons

- No information about the create/update/delete actions

### Additionnal notes

- The file size can be reduced by not displaying the "skills" and only providing their links.


## Siren

### Pros

- Complete and precise definition for the next actions reachable from this state, with templates
- Choice to include the embedded resources or just link them
- Documentation links to help understand the "manager", "team" and "skills" notions as defined by the company

### Cons

- Very verbose
- Links scattered around the document : not that easy to read by a human eye
- Not easy to convert from the original JSON object (still simpler than Cj)


## JSON API

### Pros

- Choice to include the embedded resources or just link them

### Cons

- Very verbose and redundancies
- No built-in support for actions : need to read the JSON-API spec to know what actions can be performed


## UBER

### Pros

- Choice to include the embedded resources or just link them
- Documentation links to help understand the "manager", "team" and "skills" notions as defined by the company
- Template may be specified for a user creation, but optional
- Method definition for actions (via the knowledge of the spec to know what "append" & others refer to)

### Cons

- Very verbose, especially because of the "name"/"value" data structure


## JSON-LD

### Pros

- Easy to convert from the original JSON object
- Easily human-readable
- Documentation links to help understand the "manager", "team" and "skills" notions as defined by the company
- Link to external resources "manager" and "team"
- Choice to include the embedded resources or just link them

### Cons

- No workflow information, about what action can be done from the current state


## Hydra

### Pros

- Easy to convert from the original JSON object (with a possible "JSON-LD only" step)
- Easily human-readable

### Cons

- Difficult to document the operation information : the only possible URL for that is the current one.
- Need to put all additionnal info in specific documentation files. I wrote an example but this "doc" is by no way complete, it should contain the entire API, but my goal here was only to compare the representations of the same resource.


## Mason

### Pros

- Easy to convert from the original JSON object
- Easily human-readable
- Documentation links to help understand the "manager", "team" and "skills" notions as defined by the company
- Link to external resources "manager" and "team"
- Choice to include the embedded resources or just link them
- Clear definition for possible actions
- Template may be specified for a user creation, but optional


### Cons

- Large, hard-to-read file if all features are used



## OData

### Pros

- Easy to convert from the original JSON object 

### Cons

- Lots of information in the OData specification, but not that much in the returned document. For example to find the skills you need to know the URL.
