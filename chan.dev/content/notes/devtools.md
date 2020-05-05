# DevTools

Have you been punched in the face for asking a question?

I have.  
I asked "can I customize my DevTools?" when Chrome's documentation reached out from the one free USB A hub on my iMac and punched me in the face.

Google, You're smart — WE GET IT.  
Maybe I'll be smart some day and and care more about accuracy than being helpful.  
But — for now — I don't know shit and I just wanted someone to show me _exactly_ how to do a thing.

These are the bloodied notes I took while getting pummeled by the Extending DevTools documentation.

## Starting

Create an empty `manifest.json` wherever you'd like to build your extension.

Navigate to `chrome://extensions/` in Chrome.

Enable `Developer mode`.

Click the (now visible) `Load unpacked` button.

Select the folder containing your `manifest.json` in the file picker.

This will fail.  
You'll get four errors.  
Fix them in order.

`Manifest is not valid JSON. Line: 1, column: 1, Unexpected token.`

- Add curly braces to `manifest.json` and make it valid
- Hit `Retry` in Chrome

`The 'manifest_version' key must be present and set to 2 (without quotes). See developer.chrome.com/extensions/manifestVersion.html for details.`

- Do precisely what it says (`manifest_version`)
- Hit `Retry` in Chrome

`Required value 'name' is missing or invalid.`

- Add a `name` field calling it whatever you want (you can rename it)
- Hit `Retry` in Chrome

`Required value 'version' is missing or invalid. It must be between 1-4 dot-separated integers each between 0 and 65536.`

- Add `version` according to the spec. I start with `"0.0.1"`
- Hit `Retry` in Chrome

Success.  
You should now see your extension loaded.

My `manifest.json` looks like this.

```
{
  "name": "Clever Extension Name",
  "manifest_version": 2,
  "version": "0.0.1"
}
```

What did you get?

### Why did you make me see all the errors?

Because you're gonna have to get used depending on this page for errors.  
It's the only place you're likely to see them as you develop.

---

Coming later...  
Follow my ass on twitter: https://twitter.com/chantastic

## (add a devtools page/app)

## (add a sidebar pane to Elements)

## (chrome.storage)

## (inspectedWindow.eval)

## (content scripts)

## (why the fuck doesn't console log work?)

## (add styles)

## (add light/dark-mode theming)

## (add React)

## (update the badge)

## (use tabs to scope updates)

## (update the DOM)