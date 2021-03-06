---
description: >-
  Learn more about how use Parsley's "Include" syntax which allows you insert a
  snippet within the view you are in.
---

# Include

"Include" lets you insert snippets and endpoints within the view you are in.

## Globally Available Views, Snippets, and Endpoints

When you create a snippet in the Editor, whether it be an HTML snippet, HTML Ajax, or JSON Ajax, these snippets are available globally. To insert this snippet, you'll need to use the "include" Parsley call and the name of your snippet.

```text
{{ include my-snippet }}
```

While the include prompt is commonly used for [snippets](https://zesty.org/glossary#snippet), users can also use the include prompt for including a view file within another view. For example, if you have a view with a Display Name of Contact Us and a Reference Name of contact\_us the include prompt would take the form of `{{ include contact_us }}`.

```text
{{ include reference_name }}
```

If the piece of code that that's being included is an endpoint be sure to use the full name of the endpoint.

```text
{{ include  /my/file.html }}
```

### Common Usage

One common use is to create a globally available header and footer. In our example below we have two separate HTML snippets: one called **header** and the other called **footer**. We want these to load in every page of our instance therefore we add them to the Loader file. In the Loader file, we add calls for the header and footer snippet calls as follows:

```text
{{ include header }]
{{ current_view }}
{{ include footer }}
```

