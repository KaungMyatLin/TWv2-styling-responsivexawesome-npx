##  what is npx.?.

1. npx is a tool intended to help round out the experience of using packages from the npm registry.
2. Calling npx <command> when <command> isn’t already in your $PATH will automatically install a package with that name from the npm registry for you, and invoke it.
3. When it’s done, the installed package won’t be anywhere in your globals, so you won’t have to worry about pollution in the long-term.
4. This feature is ideal for things like generators, too. Tools like yeoman or create-react-app only ever get called once in a blue moon.
5. As a tool maintainer, I like this feature a lot because it means I can just put $ npx my-tool into the README.md instructions, instead of trying to get people over the hurdle of actually installing it.
ref: https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b

##  awesome-npx one-off command lists that tried, worked and impressed.
1. npx json-server https://raw.githubusercontent.com/typicode/jsonplaceholder/master/data.json (run a mock REST API server with JSON-based response configuration)
2. npx tailwindcss-cli build css/tailwind.css -o precompile/tailwind.css
3. npx npx create-next-app
4. npx tailwindcss init tailwind-full.config.js --full -p (npx tailwindcss init -h)
5. npx -p node@19 npm it
5.1. put script: {"test": "vite"} in package.json.
5.2. put "dependencies": { "autoprefixer": "^10.4.13", "postcss": "^8.4.19", "tailwindcss": "^2.0.2", "vite": "^3.2.4"
  } in package.json.
6. npx http-server                      (run a static web server in your current directory)
7. npx okimdone npm install tailwindcss (execute a long-running command and be told out loud when it's done)
8. npx goops                            (add gitignore rules heuristically based on files in your current directory)
9. npx npm-check --skip-unused --update (interactively update npm dependencies)
10. npx gitignore node(<nameofavailablelanguagesongithubpage>) (https://github.com/github/gitignore)

## postcss.config.js telling to run tailwindcss first then autoprefixer using postcss plugin.

###
base is for a series of reset for margins, default-sizes, and padding, etc.
.container is one and only component generated precompiled-tailwind.css.
utilities generate pt-0, pt-1, etc for padding-top, and other predefined classes.
when vite runs, it builds. This builds process include cssxpostcss build, then watch index.html.
all layers of tailwindcss are postcompiled like cdn+cli "npx build css/tailwind.css -o precompile/tailwind.css".
then, autoprefixed using postcss config plugin hierarchy.
then, tailwindcss is dled as css file(tailwind.css?t=xxx) after html file dled on client-side.

ref: https://www.youtube.com/watch?v=qYgogv4R8zg&list=PL5f_mz_zU5eXWYDXHUDOLBE0scnuJofO0&index=2
###

### Contributing workflow on site:github.
Here’s how we suggest you go about proposing a change to this project:
1. Fork this project to your account.
2. Create a branch for the change you intend to make.
3. Make your changes to your fork.
4. Send a pull request from your fork’s branch to our main branch.

## https://play.tailwindcss.com

## index1 is styling items.
## index2 is designing responsive.