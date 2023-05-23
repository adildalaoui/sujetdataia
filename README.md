## Getting started 

To set up and run this project, follow the instructions below.

Requires [npm](https://www.npmjs.com/).

Dependencies:
- Node v16.13.0

One can leverage [NVM](https://github.com/nvm-sh/nvm) to install Node before proceeding to start the application by running the following commands:

```bash
# Run this to install Node 16.13.0
nvm install 16.13.0

# Run this to use the installed Node version 
nvm use 16.13.0
```

Run the following commands to start this application:

```bash
# Run the `cd` command to change the current directory to the path of project.
MacBook-Pro-de-adil:Sujet3 adil$ cd ~/adil/sujet3

# Run this to set everything up
npm install

# Run this to start your application and open it up in a new browser window
npm start
```

## Usage

### Updating configuration

The project is configured via a JSON [config file](src/config/engine.json).

### Configuration options <a id="config"></a>

The following is a complete list of options available for configuration in [engine.json](src/config/engine.json).

| option               | value type    | required/optional | source                                                                                                                                                                                          |
| -------------------- | ------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `engineName`         | String        | required          | Found in your App Search Dashboard.                                                                                                                                                             |
| `endpointBase`       | String        | required*         | (*) Elastic Enterprise Search deployment URL, example: "http://127.0.0.1:3002".                                                                                                                 |
| `searchKey`          | String        | required          | Found in your App Search Dashboard.                                                                                                                                                             |
| `searchFields`       | Array[String] | required          | A list of fields that will be searched with your search term.                                                                                                                                   |
| `resultFields`       | Array[String] | required          | A list of fields that will be displayed within your results.                                                                                                                                    |
| `querySuggestFields` | Array[String] | optional          | A list of fields that will be searched and displayed as query suggestions.                                                                                                                      |
| `titleField`         | String        | optional          | The field to display as the title in results.                                                                                                                                                   |
| `urlField`           | String        | optional          | A field with a url to use as a link in results.                                                                                                                                                 |
| `sortFields`         | Array[String] | optional          | A list of fields that will be used for sort options.                                                                                                                                            |
| `facets`             | Array[String] | optional          | A list of fields that will be available as "facet" filters. Read more about facets within the [App Search documentation](https://www.elastic.co/guide/en/app-search/current/facets-guide.html). |



## Deploy and Share

This app can be easily published to any server as static assets and served. 

To deploy:

```
npm run build
npm install netlify-cli -g
netlify deploy # enter ./build as the deploy path
```
