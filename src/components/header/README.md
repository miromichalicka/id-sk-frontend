# Header

## Introduction

The header component is used at the top of every GOV.UK page, to help users navigate.

## Guidance

Find out when to use the header component in your service in the [GOV.UK Design System](https://design-system.service.gov.uk/components/header).

## Quick start examples

## Requirements

### Build tool configuration

When compiling the Sass files you'll need to define includePaths to reference the node_modules directory. Below is a sample configuration using gulp

    .pipe(sass({
      includePaths: 'node_modules/'
    }))

### Static asset path configuration

In order to include the images used in the components, you need to configure your app to show these assets. Below is a sample configuration using Express js:

    app.use('/assets', express.static(path.join(__dirname, '/node_modules/govuk-frontend/assets')))

## Component arguments

If you are using Nunjucks,then macros take the following arguments

**If you’re using Nunjucks macros in production be aware that using `html` arguments, or ones ending with `Html` can be a [security risk](https://en.wikipedia.org/wiki/Cross-site_scripting). More about it in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).**

<table class="govuk-table">

<thead class="govuk-table__head">

<tr class="govuk-table__row">

<th class="govuk-table__header" scope="col">Name</th>

<th class="govuk-table__header" scope="col">Type</th>

<th class="govuk-table__header" scope="col">Required</th>

<th class="govuk-table__header" scope="col">Description</th>

</tr>

</thead>

<tbody class="govuk-table__body">

<tr class="govuk-table__row">

<th class="govuk-table__header" scope="row">homepageUrl</th>

<td class="govuk-table__cell ">string</td>

<td class="govuk-table__cell ">No</td>

<td class="govuk-table__cell ">The url of the homepage. Defaults to /</td>

</tr>

<tr class="govuk-table__row">

<th class="govuk-table__header" scope="row">assetsPath</th>

<td class="govuk-table__cell ">string</td>

<td class="govuk-table__cell ">No</td>

<td class="govuk-table__cell ">The public path for the assets folder. If not provided it defaults to /assets/images</td>

</tr>

<tr class="govuk-table__row">

<th class="govuk-table__header" scope="row">productName</th>

<td class="govuk-table__cell ">string</td>

<td class="govuk-table__cell ">No</td>

<td class="govuk-table__cell ">Header title that is placed next to GOV.UK. Used for product names (i.e. Pay, Verify)</td>

</tr>

<tr class="govuk-table__row">

<th class="govuk-table__header" scope="row">serviceName</th>

<td class="govuk-table__cell ">string</td>

<td class="govuk-table__cell ">No</td>

<td class="govuk-table__cell ">Header title that is placed next to GOV.UK. Used for product names (i.e. Pay, Verify)</td>

</tr>

<tr class="govuk-table__row">

<th class="govuk-table__header" scope="row">serviceUrl</th>

<td class="govuk-table__cell ">string</td>

<td class="govuk-table__cell ">No</td>

<td class="govuk-table__cell ">Url for the service name anchor.</td>

</tr>

<tr class="govuk-table__row">

<th class="govuk-table__header" scope="row">navigation</th>

<td class="govuk-table__cell ">array</td>

<td class="govuk-table__cell ">No</td>

<td class="govuk-table__cell ">An array of navigation item objects.</td>

</tr>

<tr class="govuk-table__row">

<th class="govuk-table__header" scope="row">navigation.{}.text</th>

<td class="govuk-table__cell ">string</td>

<td class="govuk-table__cell ">No</td>

<td class="govuk-table__cell ">Text of the navigation item.</td>

</tr>

<tr class="govuk-table__row">

<th class="govuk-table__header" scope="row">navigation.{}.href</th>

<td class="govuk-table__cell ">string</td>

<td class="govuk-table__cell ">No</td>

<td class="govuk-table__cell ">Url of the navigation item anchor. Both `href` and `text` attributes for navigation items need to be provided to create an item.</td>

</tr>

<tr class="govuk-table__row">

<th class="govuk-table__header" scope="row">navigationClasses</th>

<td class="govuk-table__cell ">string</td>

<td class="govuk-table__cell ">No</td>

<td class="govuk-table__cell ">Optional classes that can be added to the navigation section of the header.</td>

</tr>

<tr class="govuk-table__row">

<th class="govuk-table__header" scope="row">containerClasses</th>

<td class="govuk-table__cell ">string</td>

<td class="govuk-table__cell ">No</td>

<td class="govuk-table__cell ">Optional classes that can be added to the container, useful if you want to make the header fixed width.</td>

</tr>

<tr class="govuk-table__row">

<th class="govuk-table__header" scope="row">classes</th>

<td class="govuk-table__cell ">string</td>

<td class="govuk-table__cell ">No</td>

<td class="govuk-table__cell ">Optional additional classes to add to the header container.</td>

</tr>

<tr class="govuk-table__row">

<th class="govuk-table__header" scope="row">attributes</th>

<td class="govuk-table__cell ">object</td>

<td class="govuk-table__cell ">No</td>

<td class="govuk-table__cell ">Any extra HTML attributes (for example data attributes) to add to the header container.</td>

</tr>

</tbody>

</table>

**If you’re using Nunjucks macros in production be aware that using `html` arguments, or ones ending with `Html` can be a [security risk](https://en.wikipedia.org/wiki/Cross-site_scripting). More about it in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).**

### Setting up Nunjucks views and paths

Below is an example setup using express configure views:

    nunjucks.configure('node_modules/govuk-frontend/components', {
      autoescape: true,
      cache: false,
      express: app
    })

## Contribution

Guidelines can be found at [on our Github repository.](https://github.com/alphagov/govuk-frontend/blob/master/CONTRIBUTING.md "link to contributing guidelines on our github repository")

## License

MIT