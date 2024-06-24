---
title: "Markdown"
---

<p class="lead">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus suscipit semper ante. Curabitur eget elementum erat. Maecenas eget pulvinar lacus. In porta libero sed urna faucibus, vitae posuere nunc tincidunt. Aenean laoreet feugiat tortor. Nulla sollicitudin egestas magna, quis eleifend ipsum tincidunt at. Duis accumsan, dui a suscipit maximus, nunc justo finibus tellus, et tempor diam ante in risus. Phasellus cursus posuere libero, vel luctus massa suscipit vel.
</p>

{{< code >}}
<p class="lead">
Leading text here
</p>
{{< /code >}}

## Text

<div class="card p-4 mb-3">

# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

</div>

Lorem ipsum [dolor](https://google.nl) sit [amet](/), consectetur adipiscing elit. Phasellus suscipit semper ante. Curabitur eget elementum erat. Maecenas eget pulvinar lacus. In porta libero sed urna faucibus, vitae posuere nunc tincidunt. Aenean laoreet feugiat tortor. Nulla sollicitudin egestas magna, quis eleifend ipsum tincidunt at. Duis accumsan, dui a suscipit maximus, nunc justo finibus tellus, et tempor diam ante in risus. Phasellus cursus posuere libero, vel luctus massa suscipit vel.

## Images

Images get by default a `width: 100%`, which avoids an overflow outside of the page. If it's impossible to read text in the image, you could also decide to use [overflow](#overflow).

![Image](https://d1.awsstatic.com/Solutions/Solutions%20Category%20Template%20Draft/Solution%20Architecture%20Diagrams/workload-discovery-arch-diagram.eb4dc7103881f75c196bd11b46f0cd90a41ea2bc.png)

[Open this image in full screen](https://d1.awsstatic.com/Solutions/Solutions%20Category%20Template%20Draft/Solution%20Architecture%20Diagrams/workload-discovery-arch-diagram.eb4dc7103881f75c196bd11b46f0cd90a41ea2bc.png)

## Tables

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus suscipit semper ante. Curabitur eget elementum erat. Maecenas eget pulvinar lacus. In porta libero sed urna faucibus, vitae posuere nunc tincidunt. Aenean laoreet feugiat tortor. Nulla sollicitudin egestas magna, quis eleifend ipsum tincidunt at. Duis accumsan, dui a suscipit maximus, nunc justo finibus tellus, et tempor diam ante in risus. Phasellus cursus posuere libero, vel luctus massa suscipit vel.
1 | 2 | 3

## Blockquote

> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus suscipit semper ante. Curabitur eget elementum erat. Maecenas eget pulvinar lacus. In porta libero sed urna faucibus, vitae posuere nunc tincidunt. Aenean laoreet feugiat tortor. Nulla sollicitudin egestas magna, quis eleifend ipsum tincidunt at. Duis accumsan, dui a suscipit maximus, nunc justo finibus tellus, et tempor diam ante in risus. Phasellus cursus posuere libero, vel luctus massa suscipit vel.

# Code Samples

Some `inline code` example.

```python 
# test
def test(event, context):
    return "adsfasdfas f sdf sdf "
print("blaat")
print("blaat")

```

{{< youtube 0RKpf3rK57I >}}

## Overflow

Wrap a table or image in `<div class="overflow">...</div>` to render tables and images with a horizontal scroll bar.

<div class="overflow">

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus suscipit semper ante. Curabitur eget elementum erat. 
1 | 2 | 3

</div>

{{< code >}}<div class="overflow">

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely** 
1 | 2 | 3

</div>
{{< /code >}}