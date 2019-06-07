## npm install
## npm run dev 或者 npm run build

### 说明
#### 因为dist文件再生成文件时，比如带有hash值的文件，就会累加。这时，dist文件就会生成很多文件。所以要清楚后再生成。

### 步骤
#### npm i -d clean-webpack-plugin
#### webpack.config.js配置
```javascript
const { CleanWebpackPlugin } = require('clean-webpack-plugin');
plugins: [
  new CleanWebpackPlugin()   // 这个建议放在一般插件的上面，作用是先删除dist目录再创建新的dist目录。
]
```
