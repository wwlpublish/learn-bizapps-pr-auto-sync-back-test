Similar to any traditional programming language, Liquid has a defined syntax, can use variable definitions, and includes constructs such as output and logic. Liquid constructs are recognizable by two sets of delimiters: the double curly brace delimiters `{{ }}`, which denote output from the objects and variables, and the curly brace percentage delimiters `{% %}`, which denote logic and control flow.

> [!TIP]
> Page content and content snippets help make it easier for you to "practice" Liquid by entering the Liquid content by using the Power Apps portals Studio source code editor. As you consume this learning content, try any of the sample Liquid fragments by copying and pasting the code directly into a page on your portal.

### Output

An output statement is a set of double curly braces that contain an expression. When the output is rendered, it is replaced with the value of that expression. The expression can include Liquid objects, their properties, and variables. The following example shows a simple output statement:

```php
Hello {{ user.firstname }} from {{ 'Power Apps portals' }}
```

This output statement produces the following result (assuming that the user's first name is Doug):

> Hello Doug from Power Apps portals

### Filters

Output markup can take filters, which modify the result of the output statement. You can add filters by following the output expression with a pipe character (`|`), the name of the filter, and optional parameters after a colon (`:`).

```php
Hello {{ user.firstname | upcase }} from {{ 'Power Apps portals' }}. The time is {{ 'now' | date: 'g' }}
```

This filter statement generates the following result:

> Hello DOUG from Power Apps portals. The time is 6/24/2020 11:33 AM.

### Tags

Tags are used for the logic and control flow in your template, for example (HTML has been added to the example as well):

```php
{% assign product = 'Power Apps portals' %}

<p>
    {% if user %}
        Hello, {{ user.firstname | upcase }}, from <strong>{{ product }}</strong>.
    {% else %}
        Greetings, <em>visitor</em>, from <strong>{{ product }}</strong>!
    {% endif %}
</p>

<p>The time is {{ 'now' | date: 'g' }}</p>
```

In this fragment, the `assign` tag creates a new variable, and the `if... else` construct generates output that depends on whether the user has been defined or not (in other words, whether a portal user has signed in). The output for an anonymous user is as follows:

> Greetings, *visitor*, from **Power Apps portals**!
>
> The time is 6/24/2022 11:33 AM

Watch the following video for an overview of Liquid and some of its common concepts.

> [!Video https://www.microsoft.com/videoplayer/embed/RE4As9N]

Liquid includes several built-in objects and tags that make it versatile and flexible. The real benefits come from the Liquid extensions that are implemented by Power Apps portals.
