---
ref: docs/router/framework/react/guide/custom-link.md
replace: { 'react-router': 'solid-router' }
---

[//]: # 'BasicExampleImplementation'

```tsx
import type { Component, JSX } from 'solid-js'
import { createLink, type LinkComponent } from '@tanstack/solid-router'

type BasicLinkProps = JSX.IntrinsicElements['a'] & {
  // Add any additional props you want to pass to the anchor element
}

const BasicLinkComponent: Component<BasicLinkProps> = (props) => {
  const { class: className, ...rest } = props

  return (
    <a {...rest} class={`block px-3 py-2 text-red-700 ${className ?? ''}`.trim()}>
      {props.children}
    </a>
  )
}

const CreatedLinkComponent = createLink(BasicLinkComponent)

export const CustomLink: LinkComponent<typeof BasicLinkComponent> = (props) => {
  return <CreatedLinkComponent preload={'intent'} {...props} />
}
```

[//]: # 'BasicExampleImplementation'
[//]: # 'ExamplesUsingThirdPartyLibs'

## `createLink` with third party libraries

Here are some examples of how you can use `createLink` with third-party libraries.

### Some Library example

```tsx
// TODO: Add this example.
```

[//]: # 'ExamplesUsingThirdPartyLibs'
