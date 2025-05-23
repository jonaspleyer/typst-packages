# Typst efilrst
A simple referenceable list library for Typst. If you ever wanted to reference elements in a list by a key, this library is for you. The name comes from "reflist" but sorted alphabetically because we are not allowed to use descriptive names for packages in Typst 🤷🏻‍♂️.

## Example

```typst

#import "@preview/efilrst:0.1.0" as efilrst
#show ref: efilrst.show-rule

#let constraint = efilrst.reflist.with(
  name: "Constraint", 
  list-style: "C1)", 
  ref-style: "C1")

#constraint(
  [My cool constraint A],<c:a>,
  [My also cool constraint B],<c:b>,
  [My non-refernceable constraint C],
)

See how my @c:a is better than @c:b but not as cool as @c:e.

#constraint(
  [We continue the list with D],<c:d>,
  [And then add constraint E],<c:e>,
)

#constraint(
  counter-name: "new-list",
  [This is a new list!],<c:f>,
)
```

This generates the following output:

![Example of the typst output. The last sentence reads "See how my Constraint C1 is better than Constraint C2"](img/image.png)


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## TODO

- [x] Add continuation of lists through the `counter` function
- [ ] Allow resetting the counter on context (e.g. a new chapter).

## Changelog

### 0.1.0

- Initial release

### 0.2.0

- Add continuation of lists through the `counter` function



