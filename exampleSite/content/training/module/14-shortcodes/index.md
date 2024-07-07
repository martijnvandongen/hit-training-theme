---
title: "Shortcodes"
---

## Collapse

{{% collapse "Hint" %}}
This is a hint, or maybe an answer to a practice question.
{{% /collapse %}}

{{< code >}}
{{%/* collapse "Hint" */%}}
This is a hint, or maybe an answer to a practice question.
{{%/* /collapse */%}}
{{< /code >}}

## Callout

{{% callout %}}
Default

```python 
# test
def test(event, context):
    return "adsfasdfa
```
{{% /callout %}}

{{% callout "danger" %}}
Danger or Red
{{% /callout %}}

{{% callout "warning" %}}
Warning or Orange
{{% /callout %}}

{{% callout "yellow" %}}
Yellow
{{% /callout %}}

{{% callout "success" %}}
Success or green
{{% /callout %}}

{{% callout "info" %}}
Info or Blue
{{% /callout %}}

{{% callout "purple" %}}
Purple
{{% /callout %}}

## Tabs 

{{< tabs >}}
{{% tab name="Python" %}}
```python 
# test
def test(event, context):
    return "adsfasdfa
```
{{% /tab %}}
{{% tab name="Terraform" %}}
```text [] 
resource "aws_vpc" "vpc" {
    cidr_block = "10.0.0.0/16"
}
```
{{% /tab %}}
{{< /tabs >}}

{{< code >}}
{{</* tabs */>}}
{{%/* tab name="Python" */%}}
Here tab content, can be markdown, html, any shortcodes.
{{%/* /tab */%}}
{{</* /tabs */>}}
{{< /code >}}

### Audience

With this feature you can add content in the source which is only visible if you run the website with a specific configuration. Now you can have inline tips for the instructor.

{{% audience "instructor" %}}
> The text you're now reading is only visible if "instructor" is in the list .Params.audience in the config file of hugo.
{{% /audience %}}

```text
{{</* audience "instructor" */>}}
Renders html, for example inner shortcodes.
{{</* /audience */>}}
```

```text
{{%/* audience "instructor" */%>}}
Renders markdown but not inner shortcodes.
{{%/* /audience */%}}
```

### Practice Questions

With this shortcode you can add a practice question. Basically a quick validation of the trainees' knowledge while learning. Of course you can also create a special page with 20 questions on it as a practice test. Features:

* Mandatory is a `question` and at least a few `answers`. One of the answers should have a `correct: True`, but you can have multiple correct answers in the list and it will turn the radio buttons into checkboxes. You can use markdown, but  limit this in the `answers` to avoid confusion.
* `explanation` is the text that will appear after the answer is given.
* `shuffle_answers` the default is `True`, that means the answers will be shuffled (based on some kind of mathematical logic). With `False`, it will keep the order of the list.
* `answer_validation` the default is `True`, that means if you have not selected the exact amount of answers that are correct, it will show a warning. For example there are 2 correct answers, but you only gave 1. Or, there are 2 correct answers and you gave 3. Or, you accidently clicked check while you didn't select any answer.

{{% question %}}
question: |
    Which is not a planet?
explanation: |
    Pluto is not a planet anymore. [Check this news](https://www.britannica.com/story/why-is-pluto-no-longer-a-planet)
answers:
    - answer: "Pluto"
      correct: True
    - answer: "Jupiter"
    - answer: "Mars"
    - answer: "Earth"
{{% /question %}}

```text []
{{%/* question */%}}
question: |
    Which is not a planet?
explanation: |
    Pluto is not a planet anymore. [Check this news](https://www.britannica.com/story/why-is-pluto-no-longer-a-planet)
answers:
    - answer: "Pluto"
      correct: True
    - answer: "Jupiter"
    - answer: "Mars"
    - answer: "Earth"
{{%/* /question */%}}
```

{{% question %}}
question: |
    Which which are planets?
explanation: |
    Pluto is not a planet anymore. [Check this news](https://www.britannica.com/story/why-is-pluto-no-longer-a-planet)
shuffle_answers: False
answer_validation: False
answers:
    - answer: "Pluto"
    - answer: "Jupiter"
      correct: True
    - answer: "Mars"
      correct: True
    - answer: "Earth"
      correct: True
{{% /question %}}

```text []
{{%/* question */%}}
question: |
    Which which are planets?
explanation: |
    Pluto is not a planet anymore. [Source](https://...)
shuffle_answers: False
answer_validation: False
answers:
    - answer: "Pluto"
    - answer: "Jupiter"
      correct: True
    - answer: "Mars"
      correct: True
    - answer: "Earth"
      correct: True
{{%/* /question */%}}
```

### Partial

The feature **partial** in hugo is only available in templates. With this hack, you can also include partials in your content. The sentence below is just an example.

{{< partial "content/example" >}}
<br/>
```text
{{</* partial "content/example" */>}}
```

1. Create a partial file in: layouts/partials/content/example.html
2. Add content or logic to the file
3. Use the shortcode `partial` to include the partial where you like