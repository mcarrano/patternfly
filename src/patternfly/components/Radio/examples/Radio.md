---
id: Radio
section: components
subsection: forms
cssPrefix: pf-v5-c-radio
---

## Examples
### Basic
```hbs
{{#> radio}}
  {{#> radio-input radio-input--attribute='id="radio-simple" name="exampleRadioSimple"'}}{{/radio-input}}
  {{#> radio-label radio-label--attribute='for="radio-simple"'}}Radio{{/radio-label}}
{{/radio}}
```

### Checked
```hbs
{{#> radio}}
  {{#> radio-input radio-input--attribute='id="radio-checked" name="exampleRadioChecked" checked'}}{{/radio-input}}
  {{#> radio-label radio-label--attribute='for="radio-checked"'}}Radio checked{{/radio-label}}
{{/radio}}
```

### Label wrapping input
```hbs
{{#> radio radio--type="label" radio--attribute='for="radio-wrap"'}}
  {{#> radio-input radio-input--attribute='id="radio-wrap" name="exampleRadioWrap"'}}{{/radio-input}}
  {{#> radio-label radio-label--type="span"}}Radio label wraps input{{/radio-label}}
{{/radio}}
```

### Reversed
```hbs
{{#> radio}}
  {{#> radio-label radio-label--attribute='for="radio-rev"'}}Radio reversed{{/radio-label}}
  {{#> radio-input radio-input--attribute='id="radio-rev" name="exampleRadioReversed"'}}{{/radio-input}}
{{/radio}}
```

### Disabled
```hbs
{{#> radio}}
  {{#> radio-input radio-input--attribute='id="radio-disabled" name="exampleRadioDisabled" disabled'}}{{/radio-input}}
  {{#> radio-label radio-label--modifier="pf-m-disabled" radio-label--attribute='for="radio-disabled"'}}Radio disabled{{/radio-label}}
{{/radio}}

{{#> radio}}
  {{#> radio-input radio-input--attribute='id="radio-disabled-checked" name="exampleRadioDisabledChecked" disabled checked'}}{{/radio-input}}
  {{#> radio-label radio-label--modifier="pf-m-disabled" radio-label--attribute='for="radio-disabled-checked"'}}Radio disabled checked{{/radio-label}}
{{/radio}}
```

### With description
```hbs
{{#> radio}}
  {{#> radio-input radio-input--attribute='id="radio-description" name="exampleRadioDescription"'}}{{/radio-input}}
  {{#> radio-label radio-label--attribute='for="radio-description"'}}Radio with description{{/radio-label}}
  {{#> radio-description}}
    Single-tenant cloud service hosted and managed by Red Hat that offers high-availability enterprise-grade clusters in a virtual private cloud on AWS od GCP.
  {{/radio-description}}
{{/radio}}
```

### With body
```hbs
{{#> radio}}
  {{#> radio-input radio-input--attribute='id="radio-body" name="exampleRadioBody"'}}{{/radio-input}}
  {{#> radio-label radio-label--attribute='for="radio-body"'}}Radio with body{{/radio-label}}
  {{#> radio-body}}
    This is where custom content goes.
  {{/radio-body}}
{{/radio}}
```

### With description and body
```hbs
{{#> radio}}
  {{#> radio-input radio-input--attribute='id="radio-description-body" name="exampleRadioDescriptionBody"'}}{{/radio-input}}
  {{#> radio-label radio-label--attribute='for="radio-description-body"'}}Radio with description and body{{/radio-label}}
  {{#> radio-description}}
    Single-tenant cloud service hosted and managed by Red Hat that offers high-availability enterprise-grade clusters in a virtual private cloud on AWS od GCP.
  {{/radio-description}}
  {{#> radio-body}}
    This is where custom content goes.
  {{/radio-body}}
{{/radio}}
```

### Standalone input
```hbs
{{#> radio radio--modifier="pf-m-standalone"}}
  {{#> radio-input radio-input--attribute='id="radio-standalone" name="exampleRadioStandalone" aria-label="Standalone input"'}}{{/radio-input}}
{{/radio}}
```

## Documentation
### Overview
The Radio component is provided for use cases outside of forms. If it is used without label text ensure some sort of label for assistive technologies. (for example: `aria-label`)

If you extend this component or modify the styles of this component, then make sure any hover styles defined are applied to the clickable elements, like `<input>` or `<label>` since hover styles are used to convey the clickable target area of an element. To maximize the target area, use the example html where the `<label>` is the wrapping element.

### Accessibility
| Attribute | Applied to | Outcome |
| -- | -- | -- |
| `disabled` | `<input type="radio">` | Indicates that the element is unavailable and removes it from keyboard focus. **Required when input is disabled** |

### Usage
| Class | Applied to | Outcome |
| -- | -- | -- |
| `.pf-v5-c-radio` | `<div>`, `<label>` |  Initiates the radio component. **Required**  |
| `.pf-v5-c-radio__input` | `<input type="radio">` |  Initiates a radio input. **Required**  |
| `.pf-v5-c-radio__label` | `<label>`, `<span>` |  Initiates a label. **Required**  |
| `.pf-v5-c-radio__description` | `<span>` | Initiates a radio description. |
| `.pf-v5-c-radio__body` | `<span>` | Initiates a radio body. |
| `.pf-m-standalone` | `.pf-v5-c-radio` |  Modifies the radio component for use with a standalone `<input type="radio">`. **Required when there is no label** |
| `.pf-m-disabled` | `.pf-v5-c-radio__label` |  Modifies the radio component for the disabled state. **Required when input is disabled** |
