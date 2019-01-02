# gatsby-plugin-exclude

exclude pages from gatsby

## usage

### install

```bash
$ npm install --save gatsby-plugin-exclude
```

### configure

`gatsby-config.js`

```js
{
  resolve: 'gatsby-plugin-exclude',
  options: { paths: ['/app/**', '!/app/demo/*'] },
}
```

In this example, all paths prefixed by `/app/` will be excluded, **except for `app/demo/`**.

---

Note: [multimatch](https://github.com/sindresorhus/multimatch) specifies `*` matches any number of characters, but not `/`, whereas `**` does.

therefore to match `/abc/123/xyz`, `/abc/**` is the appropriate pattern, not `/abc/*`.

---

> based on [gatsby-plugin-create-client-paths](https://github.com/gatsbyjs/gatsby/tree/master/packages/gatsby-plugin-create-client-paths)
