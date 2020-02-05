# Gridsome Storyblok Blog

This is the project you get when you run `gridsome create https://github.com/Edmund1645/gridsome-storyblok-blog`.

### 1. Install Gridsome CLI tool if you don't have

`npm install --global @gridsome/cli`

### 2. Create a Gridsome project

1. `gridsome create https://github.com/Edmund1645/gridsome-storyblok-blog` to install this starter
2. `cd gridsome-storyblok-blog` to open the folder
3. `gridsome develop` to start a local dev server at `http://localhost:8080`
4. Happy coding 🎉🙌

### 3. Configuring Storyblok plugin

In `gridsome.config.js` add your Storyblok space public access token like this:

```js
plugins: [
  {
    use: 'gridsome-source-storyblok',
    options: {
      client: {
        accessToken: process.env.STORYBLOK_ACCESS_TOKEN // access token here
      },
      version: 'published',
      typeName: 'StoryblokEntry'
    }
  }
];
```
