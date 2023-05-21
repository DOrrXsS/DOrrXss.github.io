# webpack安装与使用

1. 基本目录

   ```
   project-name
     |- package.json
     |- package-lock.json
     |- webpack.config.js
     |- /dist
      |- index.html
     |- /src
       |- index.js
   ```

   

2. webpack库

   ```
   npm init -y    //初始化npm环境，生成package.json（若没有）| -y配置默认
   npm install webpack webpack-cli --save-dev
   ```

   

3. build捷径(package.json)

   ```
    {
      ...
      "scripts": {
       ...
       "build": "webpack"
      },
      ...
    }
   ```

   

4. webpack.config.js基本设置

   ```
    const path = require('path');
   
    module.exports = {
      entry: './src/index.js',
      output: {
        filename: 'bundle.js',
        path: path.resolve(__dirname, 'dist'),
      },
    };
   ```

   