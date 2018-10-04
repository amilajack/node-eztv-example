node-eztv-example
=================
[![Build Status](https://travis-ci.com/amilajack/node-eztv-example.svg?branch=master)](https://travis-ci.com/amilajack/node-eztv-example) [![Greenkeeper badge](https://badges.greenkeeper.io/amilajack/node-eztv-example.svg)](https://greenkeeper.io/)


A clonable and runnable example repo for the [eztv npm package](https://github.com/moesalih/node-eztv)

## Setup
```bash
git clone https://github.com/amilajack/node-eztv-example
cd node-eztv-example
yarn
yarn start
```

## Example
```js
import eztv from 'eztv';

(async () => {
  const [firstShow, ...shows] = await eztv.getShows();
  console.log(firstShow, shows);

  const show = await eztv.getShows({ query: 'big bang' });
  console.log(show);

  const showWithEpisodes = await eztv.getShowEpisodes(376, 'sherlock');
  console.log(showWithEpisodes.episodes);
})();
```
