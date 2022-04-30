//** HTML Input Attributes **//

This chapter describes the different attributes for the HTML `<input>` element.

-- The value Attribute --

The input `value` attribute specifies an initial value for an input field.

-- The readonly Attribute --

The input `readonly` attribute specifies that an input field is read-only.

A read-only input field cannot be modified (however, a user can tab to it, highlight it, and copy the text from it).

The value of a read-only input field will be sent when submitting the form.

-- The disabled Attribute --

The input `disabled` attribute specifies that an input field should be disabled.

A disabled input field is unusable and un-clickable.

The value of a disabled input field will not be sent when submitting the form.

-- The size Attribute --

The input `size` attribute speifies the visible width, in characters, of an input field.

The default value for `size` is 20.

Note: The `size` attribute works with the following input types: text, search, tel, url, email, and password.

-- The maxlength Attribute --

The input `maxlength` attribute specifies the maximum number of characters allowed in an input field.

Note: When a `maxlength` is set, the input field will not accept more than the specified number of characters. However, this attribute does not provide any feedback. So, if you want to alert the user, you must write JavaScript code.

-- The min and max Attributes --

The input `min` and `max` attributes specify the minimum and maximum values for an input field.

The `min` and `max` attributes work with the following input types: number, range, date, datetime-local, month, time and week.

Tip: Use the max and min attributes together to create a range of legal values.

-- The multiple Attribute --

The input `multiple` attribute specifies that the user is allowed to enter more than one valuein an input field.

The `multiple` attribute works with the following input types: email, and file.

-- The pattern Attribute --

The input `pattern` attribute specifies a regular expression that the input field's value is checked against, when the form is submitted.

The `pattern` attribute works with the following input types: text, date, search, url, tel, email, and password.

Tip: Use the global title attribute to describe the pattern to help the user.

-- The placeholder Attribute --

The input `placeholder` attribute specifies a short hint that describes the expected value of an input field (a sample value or a short description ofo the expected format).

The short hint is displayed in the input field before the user enters a value.

The `placeholder` attribute works with the following input types: text, search, url, tel, email, and password.

-- The required Attribute --

The inpute `required` attribute specifies that an input ield must be filled out before submitting the form.

The `required` attribute works with the following input types: text, search, url, tel, email, password, date pickets, number, checkbox, radio, and file.

-- The step Attribute --

The input `step` attribute specifies the legal number intervals for input field.

Example: if step="3", legal numbers could be -3, 0, 3, 6, etc.

Tip: This attribute can be used together with the max and min attributes to create a range of legal values.

The `step` attribute works with the following input types: number, range, date, datetime-local, month, time and week.

-- The autofocus Attribute --

The input `autofocus` attribute specifies that an input field should automatically get focus when the page loads.

-- The height and width Attributes --

The input `height` and `width` attributes specify the height and width of an `<input type="image">` element.

Tip: Always specify both the height and width attributes for images. If height and width are set, the space required for the image is reserved when the page is loaded. Without these attributes, the browser does not know the size of the image, and cannot reserve the appropriate space to it. The effect will be that the page layout will change during loading (while the images load).

-- The list Attribute --

The input `list attribute` refers to a `<datalist>` element that contains pre-defined options for an `<input>` element.

-- The input `autocomplete` attribute specifies whether a form or an input field should have autocomplete on or off.

Autocomplete allows the browser to predict the value. When a user starts to type in a field, the browser should display options to fill in the field, based on earlier typed values.

The `autocomplete` attribute works with `<form>` and the following `<input>` types: text, search, url, tel, email, password, datepickers, range, and color.