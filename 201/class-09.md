# Forms and Events

## Read 09

### Joshua McCluskey

#### Ch. 7 Forms

- Adding text
  - text input
  - Password input
  - text area
- Making Choices
  - Radio Buttons
  - Checkboxws
  - Dropdown boxes
- Submit Form
  - Submit Button
  - Image Button
  - Uploading button


`<form action="URL for page on server recieveing responses">`

- get for short forms 
- post for long forms

`<input>` allows form input to have a field for typing.

`<input="password">` used for password

`<textarea>` text field for multiline text input

`<inout type="radio" checked="checked">'

- replace radiio with chekcbox for checkbox in put
- `select>option` emmet shorthand for dropdown menu
  - for multiple add multiple.
  - `<input type="file">` for file input
    - replace file for submit or upload of uploaded files
    - same for submit as upload.

- `<input type="image" src="URL">`

`<button>` used with image
- hidden are for values you want hidden from user and form for their submission

- `<label>` is used for labeling the fields

- `fieldset>legend+label+input` emmet shorthand for grouping elements in a form

` required="required" ` in input field that you want validated for useer

`type="date"` used for date input

`type="email"`

`type="url"`

`type="search"`

Use placeholder in input for gohst text that disapppears when user clicks in input field.


#### Ch. 14 Lists, Tables, & Forms

- list style position inside is inside the box of the content and outside sits outside fo the box of content.

- Table properties allow you to make the tbale look more like an exccel sheet if desired

- If you have empty cells then you can have a border

- You can style the text input fieilds and buttons
- You can change the cursor style 

#### Ch.06 Events

- Events trigge code
- Interactions create events
- code responds to useer

- there are numerous event types including load, keydown, click, dblclick
- Mutation event wihent he DOM is modified

- select element> event > code anted to run
- select element > event > call code

- DOM event handlers
- DOM level 2 event listeners
  - element > .addEventListener ('event', function name [boolean])
- Don't use HTML event handlers


The flow of events when your code has handlers on an element

Event object tells you about the information on the event

Use event delegation can speed up a page by delegating events from the parent event in your flow


Focus and blur is needed an event trigger when elements gain or lose focus.

Mouse events use the click variations

You will need to understand positioning using this event 

Keyboard event are on the keys

Form events submit change input

Mutation events

HTML 5 events.

















[<== BACK](../README.md)
