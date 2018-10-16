# AOForm JS Library

Simple responsive Forms generator with JSON Schema, without dependencies (Pure JS). We want to continue improving our open source library, so any changes or additions of new elements will be found in the documentation. 😃

AOForm is completly compatible with Webkit, Gecko and IE9+.

## Usage

For start using add to <head>:

```javascript
<script src="https://example.com/js/aoform.js"></script>
``` 
For create form need understand the simple JSON Schema. More types of form elements in [Wiki](https://github.com/spexnetworks/aoform/wiki/JSON-Schema).

```javascript
var jsonForm = [
{
 "type": "input",
 "name": "name",
 "label": "Name",
 "values": ""
},
{
 "type": "textarea",
 "name": "history",
 "label": "History of you",
 "values": "Default text like example"
},
{
 "type": "select",
 "name": "color",
 "label": "Favorite Color",
 "values": [
	{"label":"Blue","value":"blue"},
	{"label":"Yellow","value":"yellow"},
	{"label":"Orange","value":"orange"}
 ]
},
{
 "type": "radio",
 "name": "contactmethod",
 "label": "Method for contact you",
 "values": [
	{"label":"Email","value":"email"},
	{"label":"Phone","value":"phone"},
	{"label":"Videocall","value":"videocall"}
 ]
},
{
 "type": "checkbox",
 "name": "pet",
 "label": "Your Pets:",
 "values": [
	{"label":"Dog","value":"dog"},
	{"label":"Cat","value":"cat"},
	{"label":"Turtle","value":"turtle"}
 ]
},
{
 "type": "multiselect",
 "name": "language",
 "label": "Select languages you speak",
 "values": [
	{"label":"Spanish","value":"spanish"},
	{"label":"English","value":"english"},
	{"label":"Russian","value":"russian"}
 ]
}];
```

After JSON Schema, can create new Form with:

```javascript
var myForm = new AOForm(jsonForm, document.querySelector('body'));
```

## Get Form Data

```javascript
myForm.data;
```

## Screenshot

Normal             |  Responsive
:-------------------------:|:-------------------------:
![AOForm Example Screenshot](https://i.imgur.com/ia2s8ZD.png)  |  ![AOForm Example Screenshot](https://i.imgur.com/YHZzMx0.png)

## License

[Licensed under the MIT license](https://github.com/spexnetworks/aoform/blob/master/LICENSE).
