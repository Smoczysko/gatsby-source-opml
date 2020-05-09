# gatsby-source-opml

Gatsby source plugin exposing content of [OPML file](https://en.wikipedia.org/wiki/OPML) as GraphQL resource.

## Install

`npm install --save gatsby-source-opml`

## How to use

In order to use this plugin you must have a valid OPML file in your Gatsby project workspace. Typically, those files are exported by podcast players (like Pocket Casts).

```javascript
// In your gatsby-config.js
module.exports = {
  plugins: [
    {
      resolve: "gatsby-source-opml",
      options: {
        // Url to opml file, relative to project root directory
        file: `data/podcasts.opml`,
      },
    },
  ]
};
```

## How to query

```graphql
allOpmlPodcast {
  edges {
    node {
      id
      name
      description
      url
      image {
        url
      }
    }
  }
}
```
