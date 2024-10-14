# Jinja Macros

## What are Macros?

In Jinja, macros are a way to encapsulate reusable pieces of code, similar to functions in other programming languages. However, there are some important distinctions to note when working with macros in Jinja.

### Scope of Macros

Unlike global functions in many programming languages, macros in Jinja are not global by default. They exist within the specific Jinja context in which they are instantiated. This means that you cannot define a macro at the top of your workflow and then use it throughout the entire workflow. Instead, you must re-instantiate the macro in each location where you intend to use it. Alternatively, you can use a template to achieve global access to macros.

### Creating and Running Macros

To create a macro in Jinja, you must define it using the following syntax:

```django
{% raw %}
{% macro macro_name %}
    <!-- Macro code goes here -->
{% endmacro %}
{% endraw %}
```

In this syntax, `macro_name` is the name you assign to your macro. To execute a macro, you simply call it by name and pass in any values it requires. For example, consider the following code snippet that defines a `rm_null` macro to remove null values from a list:

```django
{% raw %}
{% macro rm_null(test_list) %}
    {{ [item for item in test_list if item] }}
{% endmacro %}

{% set new_list = [1, 2, 4, null, 5, null] %}
{% endraw %}
{{ rm_null(new_list) }}
```

### Default Values in Macros

For users familiar with Python and its default values in functions, Jinja macros also support default values. You can specify a default value for a variable within a macro. If a value is not provided when calling the macro, it will default to the specified value. In the following code example, the `check_last_day` macro utilizes a default value for `current_date`:

```django
{% raw %}
{% macro check_last_day(current_date = now('utc', '%Y-%m-%dT%H:%M:%SZ')) %}
    <!-- Macro code goes here -->
{% endmacro %}
{% endraw %}

{{ check_last_day() }}
```

In this case, if `current_date` is not explicitly provided when calling `check_last_day()`, it defaults to the current date. However, if you do provide an alternate date, it will override the default value and modify the behavior of the macro.

### Conclusion

Understanding macros in Jinja is essential for creating reusable code components within your templates. Keep in mind that macros are not global by default, and you must re-instantiate them within the appropriate Jinja context. Additionally, macros support default values, allowing for flexible and customizable behavior.
