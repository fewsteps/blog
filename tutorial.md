# Create 2 GitHub Projects: 
- Project name: blog
- Feature: Public, NO readme.md file
- URL: https://github.com/fewsteps/blog.git

- Project name: /justtesting.github.com
- Fetures: Public, readme.md file create
- URL: https://github.com/fewsteps/justtesting.github.com

# Create HUGO site named as blog
`hugo new site blog`

`echo "# blog" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/fewsteps/blog.git
git push -u origin main`

# Create gitignore File
- Go to https://www.toptal.com/developers/gitignore and Type: `VisualStudioCode, Hugo, macOS` => generate file
- crate a `.gitignore` and paste the code form that site
- add `node_modules/*` on the file on line 27

# Add Themes Blist
- https://jamstackthemes.dev/theme/hugo-blist/
- github: https://github.com/apvarun/blist-hugo-theme

- run `git submodule add https://github.com/apvarun/blist-hugo-theme.git themes/blist`
- Copy `package.json` and `package-lock.json` to the root folder of your the website
- Run `npm install` to install required packages for theme
- Run `npm i -g postcss-cli` to use PostCSS with Hugo build
- Set `theme = 'blist'` in config.toml
- Run npm start to start your local server
- copy the config file content from blist/example direcory and put it in config. remove unncesssary things like lagnuge et.
- fix the base url with `https://github.com/fewsteps/blog.git`
- run `hugo server` to test and go to browser 'http://localhost:1313/fewsteps/justtesting.github.com/' 
-


Remove `public` folder and add the following lines
git submodule add -f https://github.com/fewsteps/justtesting.github.com.git public

git submodule add https://github.com/fewsteps/justtesting.github.com.git public
git submodule add -f https://github.com/fewsteps/justtesting.github.com.git public