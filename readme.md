# Pardot Form Design

***--UNDER CONSTRUCTION--***

Pardot as a platform is an incredibly powerful marketing tool, with a variety of built in functionality to make creating content such as email templates and website forms as simple as possible, for marketing specialists, developers, and designers alike.

However, much of this built in functionality, particularly in the case of form design and email template design is little documented, and can in fact make customization of this content more difficult, especially from a designer perspective.

I have put together this collection of documents, templates, and notes in an effort to better document some of this functionality, and provide quick and easy building blocks for designers to work with when creating custom Pardot content.

## Form Options

### Fields

Fields can be directly assigned CSS classes that can be specified in the 'Form' section of Layout Templates. These classes are directly added to each form field in the rendered HTML.

### Look and Feel

'Above Form' content will be injected directly above the first rendered field tag, and the ```<style>``` tag, if present.

'Below Form' content will be injected directly after the rendered 'Submit' tag.

Under the 'Styles' tab are various settings which directly modify rendered HTML. Most of these settings inject CSS styles as specified below.  

NOTE: 'Default' values pull style settings from the default Pardot CSS stylesheet, but only if the 'Include default CSS stylesheet (recommended)' checkbox is ticked in the associated Layout Template.

Any non-default values will generate a ```<style type="text/css">``` container as a child of the ```<form id="pardot-form">``` container, prior to form content. 

At default values, no ```<style type="text/css">``` container is generated.

- **Font Size**
  - Default
  - 1 (8pt)/2 (10pt)/3 (12pt)/4 (14pt)/5 (18pt)/6 (24pt)/7 (36pt)
    - ```form.form p label { font-size: *pt; }```
- **Font Family**
  - Default
  - Helvetica, Arial, Sans-serif
    - ```form.form p label { font-family: Helvetica, Arial, sans-serif; }```
  - Georgia, Times, Times New Roman, Serif
    - ```form.form p label { font-family: Gerogia, Times, 'Times New Roman', serif; }```
  - Tahoma, Trebuchet MS, Verdana, Helvetica, Arial, Sans-serif
    - ```form.form p label { font-family: Tahoma, 'Trebuchet MS', Verdana, Helvetica, Arial, sans-serif; }```
  - Courier New, Courier, Monospace
    - ```form.form p label { font-family: 'Courier New', Courier, monospace; }```
- **Font Color**
  - Sets css value under form (html>head>body>form>style)
  - ```form.form p label { color: #000000; }```
- **Label Alignment**
  - Default
  - Above
    - ```
      form.form p label { float: none; text-align: left; line-height: 1em; width: auto; }
      form.form p.submit { margin-left: 5px; }
      form.form p.no-label { margin-left: 50px; }
      form.form span.value { margin-left: 0px; }
      form.form p span.description { margin-left: 0px; }
      form.form p.required label,
      form.form span.required label { background-position: top left; padding-left 15px; }
      ```
  - Left
    - ```
      form.form p label { float: left; display: inline ;}```
- **Checkbox Alignment**
  - Default
  - Horizontal
    - ```
      form.form .pd-checkbox:after { content: " "; display: table; clear: both; }
      form.form .pd-checkbox { *zoom: 1; }
      form.form .pd-checkbox .value span { float: left !important; }
      ```
  - Stacked
    - ```
      form.form .pd-checkbox .value span { display: block !important; }
      ```
- **Radio Button Alignment**
  - Default
  - Horizontal
    - ```
      form.form .pd-radio:after { content: " "; display: table; clear: both; }
      form.form .pd-radio { *zoom:1; }
      form.form .pd-radio .value span { float: left !important; }
      ```
  - Stacked
    - ```
      form.form .pd-radio .value span {display: block !important; }
- **Required Field Character**
  - Default
  - *
    - Adds class ```required-custom``` to required fields

## Layout Templates

