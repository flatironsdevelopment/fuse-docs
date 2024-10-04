### Fuse Instructions
To update the swagger docs, use the script inside of the repo project at `lib/scripts/generate_fuse_docs_swagger.sh`.

### 👩‍💻 Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mintlify) to preview the documentation changes locally. To install, use the following command

```
npm i -g mintlify
```

Run the following command at the root of your documentation (where mint.json is)

```
mintlify install
```

and

```
mintlify dev
```

### Customizing Importer Styles

You can customize the appearance of the Fuse Importer using the `setCustomStyles` method. This allows you to modify colors, fonts, and other visual aspects of the importer. Here's an example of how to use it:

```typescript
importer.setCustomStyles({
  colors: {
    backgroundColor: "#F5F5F5",
    borderColor: "#3F51B5",
    contentColor: "#f7e4eb",
    primaryColor: "#3F51B5",
    secondaryColor: "#FF4081",
  },
  text: {
    h2: `
      color: #3F51B5;
      font-size: 28px;
      font-weight: 600;
    `,
    bodyFontSize: "16px",
  },
});
```

The `setCustomStyles` method accepts an object with the following properties:

- `colors`: An object containing color definitions for various UI elements.
- `text`: An object for customizing text styles.
- `logoURL`: A string URL for a custom logo (not shown in the example above).

Refer to the `CustomStyles` type in the source code for a complete list of customizable properties.

### 😎 Publishing Changes

Changes will be deployed to production automatically after pushing to the default branch.

You can also preview changes using PRs, which generates a preview link of the docs.

#### Troubleshooting

- Mintlify dev isn't running - Run `mintlify install` it'll re-install dependencies.
- Page loads as a 404 - Make sure you are running in a folder with `mint.json`
