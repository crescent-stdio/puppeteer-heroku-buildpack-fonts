# puppeteer-heroku-buildback-fonts

Heroku buildpack adding missing fonts for [jontewks/puppeteer-heroku-buildpack](https://elements.heroku.com/buildpacks/jontewks/puppeteer-heroku-buildpack)

It aims to support Chinese, Korean, and Japanese characters. [gnuletik/puppeteer-heroku-buildpack-fonts](https://github.com/gnuletik/puppeteer-heroku-buildpack-fonts)
This buildpack  also add Korean font, 'Pretendard'
If you are facing missing character sets, feel free to open a PR.

## Usage

```sh-session
# clear cache and current buildpacks
heroku builds:cache:purge
heroku buildpacks:clear

# puppeteer
heroku buildpacks:add -i 1 jontewks/puppeteer

# fonts
heroku buildpacks:add -i 2 https://github.com/crescent-stdio/puppeteer-heroku-buildpack-fonts

# other buildpack
heroku buildpacks:add -i 3 heroku/nodejs
```