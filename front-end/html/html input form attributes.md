//** HTML Input Form Attributes **//

This chapter describes the different `form*` attributes for the HTML `<input>` element belongs to.

The value of this attribute must be equal to the id attribute of the `<form>` element it belongs to.

-- The formaction Attribute --

The input `formaction` attribute specifies the URL of the file that will process the input when the form is submitted.

Note: This attribute overrides the `action` attribute of the `<form>` element.

The `formaction` attribute works with the following input types: submit and image.

-- The formenctype Attribute --

The input `formenctype` attribute specifies how the form-data should be encoded when submitted (only for forms with method="post")

Note: This attribute overrides the enctyype attribute of the `<form>` element.

The `formenctype` attribute works with the following input types: submit and image.

-- The formmethod Attribute --

The input `formmethod` attribute defines the HTTP method for sending form-data to the action URL.

Note: This attribute overrides the method attribute of the `<form>` element.

The `formmethod` attribute works with the following input types: submit and image.

The form-data can be sent as URL variables (method="get") or as an HTTP post transaction (method="post")

Notes on the "get" method:

• This method appends the form-data to the URL in name/value pairs
• This method is useful for form submissions where a user want to bookmark the result
• There is a limit to how much data you can place in a URL (varies between browsers), therefore, you cannot be sure that all of the form-data will be correctly transferred
• Never use the "get" method to pass sensitive information! (password of other sensitive information will be visible in the browser's address bar)

Notes on the "post" method:

• This method sends the form-data as an HTTP post transaction
• Form submissions with the "post" method cannot be bookmarked
• The "post" method is more robust and secure than "get", and "post" does not have size limitations

-- The formtarget Attribute --

The input `formtarget` attribute specifies a name or a keyword that indicates where to display the response that is received after submitting the form.

Note: This attribute overrides the target attribute of the `<form>` element.

The `formtarget` attribute works with the following input types: submit and image.

-- The formnovalidate Attrobute --

The input `formnovalidate` attribute specifies that an `<input>` element should not be validated when submitted.

Note: This attribute overrides the novalidate attribute of the `<form>` element.

The `formnovalidate` attribute works with the following input types: submit.

-- The novalidate Attribute --

The `novalidate` attrbute is a `<form>` attribute.

When present, novalidate specifies that all of the form-data should not be validated when submitted.

-- HTML Form and Input Elements --

`<form>` -- Defines an HTML form for user input
`<input>` -- Defines an input control