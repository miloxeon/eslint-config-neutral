# ⚪️ eslint-config-neutral

ESLint [Shareable Config](http://eslint.org/docs/developer-guide/shareable-configs) that catches strictly the errors and nothing more. 

With that config, you can use whatever code style you want. By default, it doesn't dictate any opinionated things. trictly the errors.

This config is a good starter. Feel free to extend it to your liking.

## Usage

```bash
npm install --save-dev eslint-config-neutral
```

Then, add this to your `.eslintrc` file:

```JSON
{
   "extends": "neutral"
}
```

You can override rules or add yours directly in `.eslintrc` file.

## License

BSL-1.0. © [Miloslav Voloskov](https://miloslav.website).
