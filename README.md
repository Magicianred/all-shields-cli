[![all-shields-cli](https://raw.githubusercontent.com/ptkdev/all-shields-cli/main/.github/assets/ptkdev-all-shields-cli-logo.png)](https://www.npmjs.com/package/@ptkdev/all-shields-cli)

# 🦌 all-shields-cli - badges generator

<!-- all-shields/header-badges:START -->

[![v2.0.1](https://img.shields.io/badge/version-v2.0.1-lightgray.svg?style=flat&logo=)](https://github.com/ptkdev/all-shields-cli/blob/main/CHANGELOG.md) [![](https://img.shields.io/npm/v/@ptkdev/all-shields-cli?color=CC3534&logo=npm)](https://www.npmjs.com/package/@ptkdev/all-shields-cli) [![License: MIT](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat&logo=license)](https://github.com/ptkdev/all-shields-cli/blob/main/LICENSE.md) [![Language: TypeScript](https://img.shields.io/badge/language-typescript-blue.svg?style=flat&logo=typescript)](https://www.typescriptlang.org/) [![ECMAScript: 2019](https://img.shields.io/badge/ES-9-F7DF1E.svg?style=flat&logo=javascript)](https://github.com/tc39/ecma262) [![Discord Server](https://discordapp.com/api/guilds/383373985666301975/embed.png)](https://discord.ptkdev.io)

<!-- all-shields/header-badges:END -->

Tool to help automate your badges of shields.io, badgen.net, fury.io, github action and snyk.io from `.all-shieldsrc` dotfile for your markdown files. You can use Liquid variables like `{{name}}` or `{{version}}` which refer to your `package.json`. Inspired by [all-contributors-cli](https://www.npmjs.com/package/all-contributors-cli)

## 🎁 Support: Donate

> This project is **free**, **open source** and I try to provide excellent **free support**. Why donate? I work on this project several hours in my spare time and try to keep it up to date and working. **THANK YOU!**

<!-- all-shields/sponsors-badges:START -->

[![Donate Paypal](https://img.shields.io/badge/donate-paypal-005EA6.svg?style=for-the-badge&logo=paypal)](https://www.paypal.me/ptkdev) [![Donate Ko-Fi](https://img.shields.io/badge/donate-ko--fi-29abe0.svg?style=for-the-badge&logo=ko-fi)](https://ko-fi.com/ptkdev) [![Donate Github Sponsors](https://img.shields.io/badge/donate-sponsors-ea4aaa.svg?style=for-the-badge&logo=github)](https://github.com/sponsors/ptkdev) [![Donate Patreon](https://img.shields.io/badge/donate-patreon-F87668.svg?style=for-the-badge&logo=patreon)](https://www.patreon.com/join/ptkdev) [![Donate Bitcoin](https://img.shields.io/badge/BTC-35jQmZCy4nsxoMM3QPFrnZePDVhdKaHMRH-E38B29.svg?style=flat-square&logo=bitcoin)](https://ptk.dev/img/icons/menu/bitcoin_wallet.png) [![Donate Ethereum](https://img.shields.io/badge/ETH-0x8b8171661bEb032828e82baBb0B5B98Ba8fBEBFc-4E8EE9.svg?style=flat-square&logo=ethereum)](https://ptk.dev/img/icons/menu/ethereum_wallet.png)

<!-- all-shields/sponsors-badges:END -->

## 📎 Menu

-   💡 [Features](#-features)
-   👔 [Screenshot](#-screenshot)
-   🚀 [How to use](#-how-to-use)
-   -   🔧 [installation](#-installation)
-   -   ⚙️ [CLI](#-cli)
-   📚 [Documentation](#-documentation)
-   -   🔑 [Liquid Variables](#-liquid-variables)
-   -   🐶 [With Husky](#-work-with-husky)
-   -   🧰 [Options](#-options-badges-array)
-   🔨 [Developer Mode](#-developer-mode)
-   -   🏁 [Run Project](#-run-project)
-   👨‍💻 [Contributing](#-contributing)
-   🐛 [Known Bugs](https://github.com/ptkdev/all-shields-cli/issues?q=is%3Aopen+is%3Aissue+label%3Abug)
-   🍻 Community:
    -   <img src="https://raw.githubusercontent.com/ptkdev/all-shields-cli/main/.github/assets/social_telegram.png" height="18px"> Telegram ([🇬🇧 English](http://t.me/ptkdev_support) | [🇮🇹 Italian](http://t.me/ptkdev_support_italian))
    -   <img src="https://raw.githubusercontent.com/ptkdev/all-shields-cli/main/.github/assets/social_discord.png" height="18px"> [Discord](http://discord.ptkdev.io) ([🇬🇧 English](https://discord.gg/jqUSGPKdmA) | [🇮🇹 Italian](https://discord.gg/SJFcbvG6RU) | [🇵🇱 Polish](https://discord.gg/25vg4VFhb7))
    -   <img src="https://raw.githubusercontent.com/ptkdev/all-shields-cli/main/.github/assets/social_twitter.png" height="18px"> [Twitter](http://twitter.com/ptkdevio)

## 💡 Features

-   [✔️] Easy to use
-   [✔️] MIT License
-   [✔️] Support: shields.io
-   [✔️] Support: fury.io
-   [✔️] Support: snyk.io
-   [✔️] Support: badgen.net
-   [✔️] Support: github action
-   [✔️] Full customizations!
-   [✔️] Liquid Variables
-   [✔️] Tool to help automate your badges on markdown.
-   [✔️] Badges generator from dotfiles for any markdown

## 👔 Screenshot

[![all-shields-cli](https://raw.githubusercontent.com/ptkdev/all-shields-cli/main/.github/assets/screenshot.png)](https://raw.githubusercontent.com/ptkdev/all-shields-cli/main/.github/assets/screenshot.png)

## 🚀 How to use

#### 🔧 Installation

1. In your node project run: `npm install @ptkdev/all-shields-cli --save-dev`
2. In your `package.json` add script:

```json
	...
	"scripts": {
		"all-shields-generate": "all-shields-cli"
	}
	...
```

3. Create `.all-shieldsrc` and paste sample:

```json
{
	"files": ["README.md"],
	"shields": [
		{
			"id": "my-badges",
			"badges": [
				{
					"url": "https://www.npmjs.com/package/@ptkdev/all-shields-cli",
					"color": "#D3D3D3",
					"label": "package name",
					"title": "package name",
					"message": "{{name}}",
					"style": "flat",
					"logo": "",
					"platform": "shields"
				}
			]
		}
	]
}
```

4. Add in your `README.md` the html comment (`my-badges` is `id` from the previous step):

```html
<!-- all-shields/my-badges:START -->
<!-- all-shields/my-badges:END -->
```

5. Run `npm run all-shields-generate`

See folder `examples`, run with `npm run example`. Below is available a description of `options` values.

##### ⚙️ CLI

1. Install cli package globally: `npm install @ptkdev/all-shields-cli -g`
2. Run anywhere: `all-shields-cli`

You can use npx, example: `npx @ptkdev/all-shields-cli`

## 🔑 Liquid variables

In your `.all-shieldsrc` dotfile you can use liquid variables like {{name}} or {{version}} which refer to your `package.json`. Key of `package.json` is name of liquid variable `{{key_from_package.json}}`

## 🐶 Work with Husky

1. In your node project run: `npm install husky --save-dev` ([docs](https://www.npmjs.com/package/husky))
2. Setup husky with: `npx husky install`
3. Add hook: `npx husky add .husky/pre-commit "npm run all-shields-generate"`

## 🧰 Options: Badges Array

| Parameter | Description                                                                 | Values                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Default value | Available on platforms                                   | Available since |
| --------- | --------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- | -------------------------------------------------------- | --------------- |
| platform  | Define platform                                                             | `discord` / `shields` / `fury` / `snyk` / `badgen` / `github`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | `shields`     |                                                          | **v1.0.0**      |
| custom    | Set custom string of image url (appended after domain url of badge service) | `string`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | empty         | `discord`, `shields`, `fury`, `snyk`, `badgen`, `github` | **v1.1.0**      |
| url       | If you click on badge open this url                                         | `URI`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | empty         | `discord`, `shields`, `fury`, `snyk`, `badgen`, `github` | **v1.0.0**      |
| color     | Badge hexcode color (right side). NOTE: Overwrited if `custom` is set.      | `string` / `hexcode`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | `lightgray`   | `shields`, `badgen`                                      | **v1.0.0**      |
| label     | Badge text (left side). NOTE: Overwrited if `custom` is set.                | `string`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | empty         | `shields`, `badgen`                                      | **v1.0.0**      |
| title     | Mouse hover alt text                                                        | `string`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | empty         | `discord`, `shields`, `fury`, `snyk`, `badgen`, `github` | **v1.0.0**      |
| message   | Badge text (right side). NOTE: Overwrited if `custom` is set.               | `string`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | empty         | `discord`, `shields`, `fury`, `snyk`, `badgen`, `github` | **v1.0.0**      |
| style     | Look of badge. NOTE: Overwrited if `custom` is set.                         | `plastic` / `flat` / `flat-square` / `for-the-badge` / `social`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | `flat`        | `shields`                                                | **v1.0.0**      |
| logo      | Show logo (left side). NOTE: Overwrited if `custom` is set.                 | shields: `bitcoin` , `dependabot` , `discord` , `gitlab` , `npm` , `paypal` , `serverfault` , `stackexchange` , `superuser` , `telegram` , `travis` and more on [docs](https://shields.io/). <br><br> badgen: `airbnb`, `apple`, `appveyor`, `atom`, `awesome`, `azure`, `azurepipelines`, `bitcoin`, `buymeacoffee`, `chrome`, `circleci`, `cocoapods`, `codacy`, `codebeat`, `codeclimate`, `codecov`, `codeship`, `commonwl`, `deepscan`, `dependabot`, `discord`, `dockbit`, `docker`, `eclipse`, `firefox`, `flow`, `git`, `github`, `gitlab`, `gitter`, `googleplay`, `graphql`, `haskell`, `jsdelivr` and more on [docs](https://badgen.net/) | empty         | `shields`, `badgen`                                      | **v1.0.0**      |
| server_id | if platform is discord, set your discord server_id                          | `DISCORD_SERVER_ID`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | empty         | `discord`                                                | **v1.0.0**      |

## 🔨 Developer Mode

#### 🏁 Run Project

1. Clone this repository or download [nightly](https://github.com/ptkdev/all-shields-cli/archive/nightly.zip), [beta](https://github.com/ptkdev/all-shields-cli/archive/beta.zip) or [stable](https://github.com/ptkdev/all-shields-cli/archive/main.zip).
2. Run `npm run init`
3. Run `npm run build && npm run link` (unix require `sudo`)
4. Run `all-shields-cli` anywhere for execute command line tool

or run `npm run dev` for watch mode.

## 📚 Documentation

Run `npm run docs`

## 👑 Backers and Sponsors

Thanks to all our backers! 🙏 Donate 3$ or more on [paypal](https://www.paypal.me/ptkdev), [ko-fi](https://ko-fi.com/ptkdev), [github](https://github.com/sponsors/ptkdev) or [patreon](https://www.patreon.com/join/ptkdev) and send me [email](mailto:support@ptkdev.io) with your avatar and url.

[![](https://api.ptkdev.io/backers/sponsor1.png?)](https://api.ptkdev.io/backers/sponsor1.html) [![](https://api.ptkdev.io/backers/sponsor2.png?)](https://api.ptkdev.io/backers/sponsor2.html) [![](https://api.ptkdev.io/backers/sponsor-kofi1.png?)](https://api.ptkdev.io/backers/sponsor-kofi1.html) [![](https://api.ptkdev.io/backers/sponsor-kofi2.png?)](https://api.ptkdev.io/backers/sponsor-kofi2.html) [![](https://api.ptkdev.io/backers/sponsor-kofi3.png?)](https://api.ptkdev.io/backers/sponsor-kofi3.html) [![](https://api.ptkdev.io/backers/sponsor3.png?)](https://api.ptkdev.io/backers/sponsor3.html) [![](https://api.ptkdev.io/backers/sponsor4.png?)](https://api.ptkdev.io/backers/sponsor4.html) [![](https://api.ptkdev.io/backers/sponsor5.png?)](https://api.ptkdev.io/backers/sponsor5.html) [![](https://api.ptkdev.io/backers/sponsor6.png?)](https://api.ptkdev.io/backers/sponsor6.html) [![](https://api.ptkdev.io/backers/sponsor7.png?)](https://api.ptkdev.io/backers/sponsor7.html) [![](https://api.ptkdev.io/backers/sponsor8.png?)](https://api.ptkdev.io/backers/sponsor8.html) [![](https://api.ptkdev.io/backers/sponsor9.png?)](https://api.ptkdev.io/backers/sponsor9.html) [![](https://api.ptkdev.io/backers/sponsor10.png?)](https://api.ptkdev.io/backers/sponsor10.html) [![](https://api.ptkdev.io/backers/sponsor11.png?)](https://api.ptkdev.io/backers/sponsor11.html) [![](https://api.ptkdev.io/backers/sponsor12.png?)](https://api.ptkdev.io/backers/sponsor12.html) [![](https://api.ptkdev.io/backers/sponsor13.png?)](https://api.ptkdev.io/backers/sponsor13.html) [![](https://api.ptkdev.io/backers/sponsor14.png?)](https://api.ptkdev.io/backers/sponsor14.html) [![](https://api.ptkdev.io/backers/sponsor15.png?)](https://api.ptkdev.io/backers/sponsor15.html) [![](https://api.ptkdev.io/backers/backer1.png?)](https://api.ptkdev.io/backers/backer1.html) [![](https://api.ptkdev.io/backers/backer2.png?)](https://api.ptkdev.io/backers/backer2.html) [![](https://api.ptkdev.io/backers/backer3.png?)](https://api.ptkdev.io/backers/backer3.html) [![](https://api.ptkdev.io/backers/backer4.png?)](https://api.ptkdev.io/backers/backer4.html) [![](https://api.ptkdev.io/backers/backer5.png?)](https://api.ptkdev.io/backers/backer5.html) [![](https://api.ptkdev.io/backers/backer6.png?)](https://api.ptkdev.io/backers/backer6.html) [![](https://api.ptkdev.io/backers/backer7.png?)](https://api.ptkdev.io/backers/backer7.html) [![](https://api.ptkdev.io/backers/backer8.png?)](https://api.ptkdev.io/backers/backer8.html) [![](https://api.ptkdev.io/backers/backer9.png?)](https://api.ptkdev.io/backers/backer9.html) [![](https://api.ptkdev.io/backers/backer10.png?)](https://api.ptkdev.io/backers/backer10.html) [![](https://api.ptkdev.io/backers/backer11.png?)](https://api.ptkdev.io/backers/backer11.html) [![](https://api.ptkdev.io/backers/backer12.png?)](https://api.ptkdev.io/backers/backer12.html) [![](https://api.ptkdev.io/backers/backer13.png?)](https://api.ptkdev.io/backers/backer13.html) [![](https://api.ptkdev.io/backers/backer14.png?)](https://api.ptkdev.io/backers/backer14.html) [![](https://api.ptkdev.io/backers/backer15.png?)](https://api.ptkdev.io/backers/backer15.html) [![](https://api.ptkdev.io/backers/backer16.png?)](https://api.ptkdev.io/backers/backer16.html) [![](https://api.ptkdev.io/backers/backer17.png?)](https://api.ptkdev.io/backers/backer17.html) [![](https://api.ptkdev.io/backers/backer18.png?)](https://api.ptkdev.io/backers/backer18.html) [![](https://api.ptkdev.io/backers/backer19.png?)](https://api.ptkdev.io/backers/backer19.html) [![](https://api.ptkdev.io/backers/backer20.png?)](https://api.ptkdev.io/backers/backer20.html) [![](https://api.ptkdev.io/backers/backer21.png?)](https://api.ptkdev.io/backers/backer21.html) [![](https://api.ptkdev.io/backers/backer22.png?)](https://api.ptkdev.io/backers/backer22.html) [![](https://api.ptkdev.io/backers/backer23.png?)](https://api.ptkdev.io/backers/backer23.html) [![](https://api.ptkdev.io/backers/backer24.png?)](https://api.ptkdev.io/backers/backer24.html) [![](https://api.ptkdev.io/backers/backer25.png?)](https://api.ptkdev.io/backers/backer25.html) [![](https://api.ptkdev.io/backers/backer26.png?)](https://api.ptkdev.io/backers/backer26.html) [![](https://api.ptkdev.io/backers/backer27.png?)](https://api.ptkdev.io/backers/backer27.html) [![](https://api.ptkdev.io/backers/backer28.png?)](https://api.ptkdev.io/backers/backer28.html) [![](https://api.ptkdev.io/backers/backer29.png?)](https://api.ptkdev.io/backers/backer29.html)

## 👨‍💻 Contributing

I ❤️ contributions! I will happily accept your pull request! Translations, grammatical corrections (GrammarNazi you are welcome! Yes my English is bad, sorry), etc... Do not be afraid, if the code is not perfect we will work together 👯 and remember to insert your name in `.all-contributorsrc` and `package.json` file.

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://ptk.dev"><img src="https://avatars1.githubusercontent.com/u/442844?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Patryk Rzucidło</b></sub></a><br /><a href="https://github.com/ptkdev/ptkdev/all-shields-cli/commits?author=ptkdev" title="Code">💻</a> <a href="#translation-ptkdev" title="Translation">🌍</a> <a href="https://github.com/ptkdev/ptkdev/all-shields-cli/commits?author=ptkdev" title="Documentation">📖</a> <a href="https://github.com/ptkdev/ptkdev/all-shields-cli/issues?q=author%3Aptkdev" title="Bug reports">🐛</a></td>
    <td align="center"><a href="https://github.com/di4urp"><img src="https://avatars1.githubusercontent.com/u/44859500?v=4?s=100" width="100px;" alt=""/><br /><sub><b>di4urp</b></sub></a><br /><a href="https://github.com/ptkdev/ptkdev/all-shields-cli/commits?author=di4urp" title="Code">💻</a> <a href="https://github.com/ptkdev/ptkdev/all-shields-cli/issues?q=author%3Adi4urp" title="Bug reports">🐛</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

> 💰 In the future, if the donations allow it, I would like to share some of the success with those who helped me the most. For me open source is share of code, share development knowledges and share donations!

## 🦄 Other Projects

<!-- all-shields/projects-badges1:START -->

[![](https://img.shields.io/badge/%F0%9F%92%BB%20My-Portfolio-3498db.svg?style=flat&logo=)](https://ptk.dev/)

<!-- all-shields/projects-badges1:END -->

<!-- all-shields/projects-badges2:START -->

[![](https://img.shields.io/badge/%F0%9F%A6%92%20Tools-Node%20Logger-9b59b6.svg?style=flat&logo=)](https://github.com/ptkdev/ptkdev-logger) [![](https://img.shields.io/badge/%F0%9F%A6%8C%20Tools-All%20Shields%20CLI-9b59b6.svg?style=flat&logo=)](https://github.com/ptkdev/all-shields-cli) [![](https://img.shields.io/badge/%F0%9F%96%A5%EF%B8%8F%20Tools-Aspect%20Ratio%2021%3A9-9b59b6.svg?style=flat&logo=)](https://github.com/ptkdev/chrome-extension-aspectratio219) [![](https://img.shields.io/badge/%F0%9F%9B%A1%20Tools-Badges%3A%20Available%20on-9b59b6.svg?style=flat&logo=)](https://availableon.badge.ptkdev.io/) [![](https://img.shields.io/badge/%F0%9F%90%BE%20Tools-JSON%20Token%20Replace-9b59b6.svg?style=flat&logo=)](https://github.com/ptkdev/json-token-replace) [![](https://img.shields.io/badge/%F0%9F%90%8D%20Tools-ESLint%3A%20snakecasejs-9b59b6.svg?style=flat&logo=)](https://github.com/ptkdev/eslint-plugin-snakecasejs)

<!-- all-shields/projects-badges2:END -->

<!-- all-shields/projects-badges3:START -->

[![](https://img.shields.io/badge/%F0%9F%93%B8%20WebComponent-Instagram%20Widget-e74c3c.svg?style=flat&logo=)](https://github.com/ptkdev-components/webcomponent-instagram-widget) [![](https://img.shields.io/badge/%F0%9F%91%91%20WebComponent-My%20Patreon%20Box-e74c3c.svg?style=flat&logo=)](https://github.com/ptkdev-components/webcomponent-patreon-box) [![](https://img.shields.io/badge/%F0%9F%8F%9E%20WebComponent-Carousel%20Slideshow-e74c3c.svg?style=flat&logo=)](https://github.com/ptkdev-components/webcomponent-carousel-slideshow)

<!-- all-shields/projects-badges3:END -->

<!-- all-shields/projects-badges4:START -->

[![](https://img.shields.io/badge/%F0%9F%8E%A8%20Themes-VSCode-f1c40f.svg?style=flat&logo=)](https://github.com/ptkdev/vscode-theme-dark-blood) [![](https://img.shields.io/badge/%F0%9F%93%9A%20Bot-GameBookChat-34495e.svg?style=flat&logo=)](https://t.me/gamebookchatbot) [![](https://img.shields.io/badge/%F0%9F%91%94%20Boilerplate-Svelte-f368e0.svg?style=flat&logo=)](https://github.com/ptkdev?q=svelte) [![](https://img.shields.io/badge/%F0%9F%91%94%20Boilerplate-WebComponents-f368e0.svg?style=flat&logo=)](https://github.com/ptkdev?q=webcomponent) [![](https://img.shields.io/badge/%F0%9F%91%94%20Boilerplate-BOT-f368e0.svg?style=flat&logo=)](https://github.com/ptkdev?q=bot) [![](https://img.shields.io/badge/%F0%9F%91%94%20Boilerplate-Node-f368e0.svg?style=flat&logo=)](https://github.com/ptkdev?q=node) [![](https://img.shields.io/badge/%F0%9F%92%85%20App-Me%20in%20Gifs-2ecc71.svg?style=flat&logo=)](https://meingifs.pics/) [![](https://img.shields.io/badge/%F0%9F%93%B1%20App-Stickers-2ecc71.svg?style=flat&logo=)](https://github.com/ptkdev/ptkdev-stickers#-install-free)

<!-- all-shields/projects-badges4:END -->

## 💫 License

-   Code and Contributions have **MIT License**
-   Images and logos have **CC BY-NC 4.0 License** ([Freepik](https://it.freepik.com/) Premium License)
-   Documentations and Translations have **CC BY 4.0 License**

###### Copyleft (c) 2021 [Patryk Rzucidło](https://ptk.dev) ([@PTKDev](https://twitter.com/ptkdev)) <[support@ptkdev.io](mailto:support@ptkdev.io)>
