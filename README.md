# taro-f2-react

> 支持在使用 Taro React 开发小程序中，按 React 组件书写方式使用 F2 。
<br>使用 [@antv/f2](https://f2.antv.vision/zh/docs/tutorial/getting-started) 版本 4.x

# Install

```bash
# via npm
$ npm i taro-f2-react

# via yarn
$ yarn add taro-f2-react
```

# Usage

不需要额外配置 usingComponents 小程序原生组件，直接通过 import 引入 React 组件即可。
<br>详细使用请参考 [@antv/f2](https://f2.antv.vision/zh/docs/tutorial/getting-started)

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import { View } from '@tarojs/components';
import F2Canvas from 'taro-f2-react';
import { Chart, Interval } from '@antv/f2';

const data = [
  { genre: 'Sports', sold: 275 },
  { genre: 'Strategy', sold: 115 },
  { genre: 'Action', sold: 120 },
  { genre: 'Shooter', sold: 350 },
  { genre: 'Other', sold: 150 },
];

ReactDOM.render(
  <View style={{ width: '100%', height: '260px' }}>
    <F2Canvas>
      <Chart data={data}>
        <Interval x="genre" y="sold" />
      </Chart>
    </F2Canvas>
  </View>,
  document.getElementById('root')
);
```

## Support

Taro > 3.x

## LICENSE [MIT](LICENSE)

Copyright © 2022 Daniel Zhao.
