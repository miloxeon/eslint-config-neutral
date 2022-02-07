# ⚪️ eslint-config-neutral

ESLint [Shareable Config](http://eslint.org/docs/developer-guide/shareable-configs) that catches strictly the errors and nothing more. 

With that config, you can code however you want. This config is a good choice for those who don't use ESLint at all because they feel like the linter restricts them. By default, it doesn't dictate any opinionated things. Strictly the errors.

Also, this config is a good starter. Feel free to extend it to your liking.

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
