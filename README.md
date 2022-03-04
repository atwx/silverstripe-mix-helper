# silverstripe-mix-helper
Utilities for using Laravel Mix inside Silverstripe CMS

## Suggested Project Structure

We suggest that your mix output is rendered into /app/client/dist. 
If not, you can put another path in the Mix command in your templates.

## Using The Template Helper

The `$Mix()` command can be used inside your templates to include e.g. css or js compiled by Laravel Mix. 
It automatically checks, if it should include the path to the compiled asset or if hot reloading is needed 
during development mode.

To include css or js put the following commands in your templates:

CSS inside the `<head>` tag:
```
<link rel="stylesheet" href="$Mix("/css/styles.min.css")">
```

JavaScript at the end of your page's `<body>`:
```
<script src="$Mix("/js/main.js")"></script>
```
