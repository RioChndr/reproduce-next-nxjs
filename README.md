
## Reproduce Nx & next js bugs

this repository for issue https://github.com/nrwl/nx/issues/11582.

### Step Reproduce

- Clone
- `yarn install` && `nx serve next`
- Open page `http://localhost:4200/`
- It should redirect to `/login`

but it show error 
```
error - TypeError [ERR_INVALID_URL]: Invalid URL
    at new NodeError (node:internal/errors:371:5)
    at onParseError (node:internal/url:552:9)
    at new URL (node:internal/url:628:5)
    at Object.relativizeURL (/home/riochndr/project/react-learn/reproduce-next-2/node_modules/next/dist/shared/lib/router/utils/relativize-url.js:7:48)
    at Object.fn (/home/riochndr/project/react-learn/reproduce-next-2/node_modules/next/dist/server/next-server.js:922:53)
    at async Router.execute (/home/riochndr/project/react-learn/reproduce-next-2/node_modules/next/dist/server/router.js:213:36)
    at async DevServer.run (/home/riochndr/project/react-learn/reproduce-next-2/node_modules/next/dist/server/base-server.js:619:29)
    at async DevServer.run (/home/riochndr/project/react-learn/reproduce-next-2/node_modules/next/dist/server/dev/next-dev-server.js:536:20)
    at async DevServer.handleRequest (/home/riochndr/project/react-learn/reproduce-next-2/node_modules/next/dist/server/base-server.js:320:20) {
  input: '/_next/static/chunks/react-refresh.js?ts=1660469080724',
  code: 'ERR_INVALID_URL'
}
```