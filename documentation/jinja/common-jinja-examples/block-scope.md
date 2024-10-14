# Block Scope

## Introduction

In Jinja, block scope refers to the scope in which a variable exists and is accessible. This guide will explain how block scope works in Jinja and provide examples to illustrate its behavior.

### What is Block Scope?

Block scope in Jinja is best understood by looking at an example. Consider the following code snippet:

```django
{% raw %}
{% set var = 0 %}
{%- for number in range(1, 10) -%}
    {% set var = var + 1 %}
{% endfor %}
{% endraw %}
{{ var }}
```

In many programming languages, you might expect the result to be 9, but in Jinja, the output will be 0. This is because, in Jinja, anything defined within a `for` loop stays within that loop. When you use the `{% set %}` feature within a loop, you're actually creating a new variable with the same name, and this variable is destroyed when the loop ends.

### Exception: Appending to a List

There is an exception to this block scope rule, which is when you are appending to a list that already exists. This works because you are modifying the actual variable that was created before the loop is called, rather than creating a new variable with the same name within the loop. Here's an example:

```django
{% raw %}
{% set var = [] %}
{%- for number in range(1, 10) -%}
    {% do var.append(number) %}
{% endfor %}
{% endraw %}
{{ var }}
```

In this case, the code will result in a list containing the numbers 1 to 9.

### Persistent Scope

To maintain a persistent scope in Jinja and have variables that persist across multiple blocks or loops, you can create a namespace. Think of this namespace as a data structure that holds your variables. Here's an example:

```django
{% raw %}
{% set var = namespace(value=0) %}
{%- for number in range(1, 10) -%}
    {% set var.value = var.value + 1 %}
{% endfor %}
{% endraw %}
{{ var.value }}
```

In this code, we create a namespace named `var` with an initial value of 0. Inside the loop, we can access and modify `var.value`, and the changes persist outside the loop. This code will result in the expected value of 9.

{% hint style="info" %}
It's important to note that in the example above, `value` in `namespace(value=0)`is another variable that exists within the var namespace, meaning it's an arbitrary name. Something like this would function in the same exact way:

```django
{% raw %}
{% set var = namespace(data=0) %}
{%- for number in range(1, 10) -%}
    {% set var.data = var.data + 1 %}
{% endfor %}
{% endraw %}
{{ var.data }}
```

You're also not restricted to a single variable within the namespace. You can mix datatypes within the namespace, just like you can in other data structures. Something like this would work as well:&#x20;

```django
{% raw %}
{% set var = namespace(data=0, value=1) %}
{%- for number in range(1, 10) -%}
    {% set var.data = var.data + 1 %}
    {% set var.value = var.value + 1 %}
{% endfor %}
{% endraw %}
{{ var.data }}
{{ var.value }}
```
{% endhint %}

### Conclusion

Understanding block scope in Jinja is crucial for effectively working with variables within templates. Remember that variables defined within a block, such as a `for` loop, are limited to that block's scope. To maintain persistent scope or modify variables across blocks, consider using namespaces as demonstrated in this documentation.
