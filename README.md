node-eztv-example
=================

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
