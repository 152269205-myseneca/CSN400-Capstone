# Organizing information with collapsed sections

You can streamline your Markdown by creating a collapsed section with the `<details>` tag.

## Creating a collapsed section

You can temporarily obscure sections of your Markdown by creating a collapsed section that the reader can choose to expand. For example, when you want to include technical details in an issue comment that may not be relevant or interesting to every reader, you can put those details in a collapsed section.

Any Markdown within the `<details>` block will be collapsed until the reader clicks to expand the details.

Within the `<details>` block, use the `<summary>` tag to let readers know what is inside. The label appears to the right of.

```markdown
<details>

<summary>Tips for collapsed sections</summary>

### You can add a header

You can add text within a collapsed section.

You can add an image or a code block, too.

</details>
```

### Example One: Collapsed Section including Header

<details>

<summary><b>Tips for collapsed sections</b></summary>

### You can add a header

You can add text within a collapsed section. The collapsed section can be expanded or collapsed 

You can add an image or a code block, too.

```ruby
   puts "Hello World"
```

</details>

### Example Two: Collapsed Section with Python Code



## How does this work?
The Markdown inside the `<summary>` label will be collapsed by default:

After a reader clicks on the **expand** icon, the details are expanded:
