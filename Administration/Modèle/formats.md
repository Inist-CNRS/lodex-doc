# Formats

A column may have a _format_. A format modifies the way a column is displayed in the HTML application, or exported by an exporter.

For example, the `extendednquads` exporter uses the `istex` format, by taking the value of the column \(namely, an ISTEX query\), and pulling API's results into the exported file.

## chart

The Contextual Chart format is used to display charts from data in the column.

## email

The `email` format add a link to the email given. For example, if the value is `chuck.norris@nowhere.org`, a link will be added in the web application: `mailto:chuck.norris@nowhere.org`.

This should not affect exporters.

## html

The `html` format takes the value in the column, and displays it as is, without encoding anything, in the web application.

## image

The `image` format takes the URL of an image, and displays it in the web application.

Parameter: width percentage.

## istex

The `istex` format takes an ISTEX query \(e.g.: `language:eng`\), gets the 10 first results from the API, and displays their titles, abstracts, years of publication, and add links to the matching PDFs.![](/assets/istex-format-2.png)

The `extendednquads` exporter uses it to get all matching documents, and export the asked triples.

## link

The `link` format adds an `href` link to the URL given in the column. This works with any URL, on the contrary to the `uri` format. Plus, an array of URLs will produce an unordered list of clickable URLs.

## list

The `list` format takes a columns' value, which contains a JSON array, to display the items in a bulleted list.

To get a JSON array from a tabular file, you need to use the `SPLIT` transformer.

## markdown

The `markdown` format converts the column value using the [MarkDown](http://daringfireball.net/projects/markdown/syntax) syntax to display it in the web application.

This allows to add links, headings, lists, ... into a text.

## paragraph

The paragraph format justifies the column value when displaying it in the web application.

Parameter: width percentage.

## title

The `title` format displays the column value using a title style.

![](/assets/title-format.png)

Parameter: level of the title \(like HTML `h1`, `h2`, `h3`,...\)

## trello-timeline

The `trello-timeline` format displays a timeline using a trello board. BUT WE NEED AN EXPLANATION FROM THE AUTHOR ;\)

## uri

The `uri` format makes a link to an _internal_ URI: it has to be an URI from the same lodex.

