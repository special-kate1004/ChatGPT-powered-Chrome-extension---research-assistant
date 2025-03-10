A browser extension to display ChatGPT response alongside Search Engine results, supports Chrome/Edge/Firefox/Safari(macOS) and
Android.

Support most search engines, including Google, Bing, Yahoo, DuckDuckGo, StartPage, Baidu, Kagi, Yandex, Naver, Brave,
Searx, Ecosia, Neeva in total.

## Diff with upstream

<details>
<summary>Details:</summary>

- Support StartPage, Ecosia, Neeva, Searx(searx.tiekoetter.com, searx.fmac.xyz, searx.be and more)
- Android support
- Safari(macOS) support
- Custom mount point (e.g. for some unsupported engines)
- Preview your setting (e.g. theme, mount point) in realtime
- Linkify in ReactMarkdown
  separate sessions for each page
- Fix answer being overwritten due to "network error" or other errors
- Collapse answers
- Popup Setting Window (Upstream has switched to a standalone options page)
- Allow `Insert chatGPT at the top of search results` in Setting Window
- Switch to webpack
- Javascript

</details>

## Upstream supports, but not here

<details>
<summary>Details:</summary>

(I don't think these contents are very valuable, but I could be wrong, so if you think of some suitable application
scenario or related need, please create an issue)

1. Upstream supports setting the desired language, and will force the relevant words to be inserted at the end after you
   enter the question

    - but I think, users always expect to get the language corresponding to their question, when you want to get a
      different language, you should take the initiative to specify when searching, which is also consistent with the
      habits of using search engines, and this fork supports interactive mode, you can also continue to tell chatGPT
      what you want. Once you set up forced insertion, it will change the actual content of the user's question, for
      example, when you configure French and search in English, chatGPT will always reply to you in French, when you
      expect a reply in English, you will have to open the settings page, make changes, then refresh and ask the
      question again, which I think is a very bad process

2. The upstream extension popup window has an embedded chatGPT page (iframe)

    - but you have to open the chatGPT website and log in to use it, so I think, in that case, why not use it directly
      on the official website? In addition, interactive mode is already supported here, and each page can be used as a
      separate session, so this feature is less necessary

</details>

## Preview

- [SearchEngines](screenshot/engines/README.md)
- Code highlight, interactive mode, dark mode, copy/collapse answers, theme switcher and more

  (Click on the extension icon to open the setting window)
  ![code-highlight](screenshot/code-highlight.png)
- LaTeX
  ![latex](screenshot/latex.png)
- Android
  ![android](screenshot/android.jpg)


## Build from source

1. Clone the repo
2. Install dependencies with `npm install`
3. `npm run build`
4. Load `build/chromium/` or `build/firefox/` directory to your browser
