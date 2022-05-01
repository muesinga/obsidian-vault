//** Box Shadow **//

The CSS `box shadow` property applies shadow to elements.

In its simplest use, you only specify the horizontal shadow and the vertical shadow:

Example:

`div { box-shadow: 10px 10px; }`

Next, add a blur effect to the shadow:

`div { box-shadow: 10px 10px 5px grey; }`

-- Cards --

You can also use the `box-shadow` property to create paper-like cards:

```
div.card {
  width: 250px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  text-align: center;
}
```

-- CSS Shadow Properties --

`box-shadow` -- Adds one or more shadows to an element
`text-shadow` -- Adds one or more shadows to a text
