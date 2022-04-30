//** HTML Forms **//

An HTML form is used to collect user input. The user input is most often sent to a server for processing.

-- The `<form>` Element --

The HTML `<form>` element is used to create an HTML form for user input.

The `<form>` element is a container for different types of input elements, such as: text fields, checkboxes, radio buttons, submit buttons, etc.

All the different form elements are covered in this chaper: HTM Form Elements.

-- The `<input>` Element --

The HTML `<input>` elements is the most used form element.

An `<input>` element can be displayed in many ways, depending on the `<type>` attribute.

• `<input type="text">` -- displays a single-line text input field
• `<input type="radio">` -- displays a radio button (for selecting one of the many choices)
• `<input type="checkbox">` -- displays a checkbox (for selecting zero or more of many choices)
• `<input type="submit">` -- displays a submit button (for submitting the form)
• `<input type="button">` -- displays a clickable button

-- Text Fields --

The `<input type="text">` defines a single-line input field for text input.

-- The `<label>` Element --

The `<label>` tag definds a label for many form elements.

The `<label>` element is useful for screen-reader users, because the screen-reader will read out loud the label when the user focus on the input element.

The `<label>` element also help users who have difficulty clicking on very small regions (such as radio buttons or checkboxes) - because when the user clicks the text within the `<label>` element, it toggles the radio button/checkbox

The `for` attribute for the `<label>` tag should be equal to the `id` attribute of the `<input>` element to bind them together.

-- Checkboxes --

The `<input type="checkbox">` defines a checkbox

Checkboxes let a user select ZERO or MORE options of a limited number of choices.

-- The Submit Button --

The `<input type="submit">` defines a button for submitting the form data to a form-handler.

The form-handler is typically a file on the server with a script for processing input data.

The form-handler is specified in the form's `action` attribute.

-- The Name Attribute for `<input>` --

Notice that each input field must have a `<name>` attribute to be submitted.

If the `name` attribute is omitted, the value of the input field will not be sent at all.

