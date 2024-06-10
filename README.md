# CSS stylesheets with Eleventy, Liquid & DecapCMS

### Folder structure

- templates in src/content
- documentation in src/content/doc with aside navigation
- blog in src/content/blog with pagination navigation
- layouts in src/_layouts
- includes in src/_includes
- JSON files in src/_data
- images & JS in src/assets with /admin (Decap CMS)

### CSS stylesheet

- tokens in /src/_data/tokens.json
- styles in /src/_includes/css/*.css
- style.css file creation in /src/content/css.liquid with permalink = assets/css/style.css
  imports all the /src/_includes/css/*.css files

### Page layout

- src/_layouts/base.liquid: head code + DecapCMS scripts
- src/_layouts/default.liquid: HTML5 structure with ARIA landmarks
- src/_includes/nav-primary.liquid with primary navigation
- src/_includes/nav-secondary.liquid with secondary navigation
- src/_includes/nav-pagination.liquid with pagination navigation
- src/_includes/nav-footer.liquid with footer navigation
- src/_includes/copyright.liquid to include in footer

### Navigation links

- tags: add primary, secondary or footer in frontmatter
- for secondary tags, add folder with folder's name in frontmatter

### Package.json scripts

- "start": "npx @11ty/eleventy --serve",
- "decap": "npx decap-server & npx @11ty/eleventy --serve",
- "build": "eleventy",
- "build-gp": "eleventy --pathprefix 'css'"

### Dependencies

- "@11ty/eleventy": "^2.0.1"
- ready for [Decap CMS](https://decapcms.org/) with local backend or Netlify
- ready for GitHub Pages (.github/workflows/)

### eleventy.config.js

```
module.exports = function (eleventyConfig) {
    eleventyConfig.addWatchTarget("./src/assets");
    eleventyConfig.addPassthroughCopy({ "./src/assets": "./assets" });
    return {
        dir: {
            input: "src/content", // Set the source for 11ty
            output: "_site", // This is the default
            includes: "../_includes", // This is the default
            layouts: "../_layouts", // Base page layouts
            data: "../_data" // This is the default
        }
    };
};
```
