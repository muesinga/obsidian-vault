//** HTML Form Attributes **//

Different attributes for the HTML `<form>` element.

-- The Action Attribute --

The `action` attribute defines the action to be performed when the form is submitted.

Usually, the form data is sent to a file on the server when the user clicks on the submit buttton.

-- The Target Attribute --

The `target` attribute specifies where to display the respoonse that is received after submitting the form.

The `target` attribute can have one of the following values:

• `_blank` -- The response is displayed in a new window or tab
• `_self` -- The response is displayed in the current window
• `_parent` -- The response is displayed in the parent frame
• `_top` -- The response is displayed in a named iframe
• framename -- The response is displayed in a named iframe

The default value is `_self` which means that the response will open in the current window.

-- The Method Attribute --

The `method` attribute specifies the HTTP method to be used when submitting the form data.

The form-data can be sent as URL variables (with `method="get"`) or as HTTP post transaction (with `method="post"`).

The default HTTP method when submitting form data is GET.

Notes on GET:

• Appends the form data to the URL, in name/value pairs
• NEVER use GET to send sensitive data! (the submitted form data is visible in the URL!)
• The length of a URL is limited (2048 characters)
• Useful for form submissions where a user wants to bookmark the result
• GET is good for non-secure data, like query strings in Google

Notes on POST:

• Appends the form data inside the body of the HTTP request (the submitted from data is not shown in the URL)
• POST has no size limitations, and can be used to send large amounts of data.
• Form submissions with POST cannot be bookmarked

-- The Autocomplete Attribute -- 

The `autocomplete` attribute specifies whether a form should have autocomplete on or off.

When autocomplete is on, the browser automatically complete values based on values that the user has entered before.

-- The Novalidate Attribute --

The `novalidate` attribute is a boolean attribute.

When present, it specifies that the form-data (input) should not be validated when submitted.

A form with a novalidate attribute:

`<form action="/action_page.php" novalidate>`

-- List of All `<form>` Attributes --

`<accept-charset>` -- Specifies the character encoding used for form submission
`action` -- Specifies where to send the form0data when a form is submitted
`autocomplete` -- Specifies whether a form should have autocomplete on or off
`enctype` -- Specifies how the form-data should be encoded when submitting it to the serer (only for methody="post")
`method` -- Specifies the HTTP method to use when sending form-data
`name` -- Specifies the name of the form
`novalidate` -- Specifies the the form should not be validated when submitted
`rel` -- Specifies the relationship between a linked resource and the current document
`targe` -- Specifies where to display the response that is received after submitting the form