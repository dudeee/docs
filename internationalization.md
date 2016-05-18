# Internationalization

 We love our local languages, that's why we give you the ability to translate Dude to your language.
 
 You can find our [`locales` folder](https://github.com/dudeee/dude/tree/master/locales) in the repository and contribute by translating the strings from English to your language.
 
 Plugins can also provide localized strings by creating their own `locales` folder and loading it. To do so, you have to load your locales folder in your plugin:
 
 ```javascript
 export default async bot => {
   await bot.i18n.load(path.join(__dirname, '../locales/'));
 }
 ```
 
 Your folder must follow the structure specified by [`i18next-node-fs-backend`](https://github.com/i18next/i18next-node-fs-backend).

 Please follow the Dude Style Guide in your JSON keys.
 
 ## Substitutions
 
 If you take a look at the files, you might see strings like this:
 
 ```json
 {
   "notfound": "Could not find user *%username%*."
 }
 ```
 
 The `%username%` is a variable which is replaced by bot when using this string. Using variables you can make sure the localization process is as flexible as possible.
 
 To use variables in your code, you should use `bot.t` like this:
  
 
 For more information see [`i18next`](http://i18next.com/).