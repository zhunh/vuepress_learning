# 安装caliper

1. 将caliper拉取到本地

   ```
   git clone https://github.com/hyperledger/caliper.git
   ```

2. 构建环境

   ```
   cd caliper
   npm install
   #如果本机是Python3环境，换成Python2
   npm run repoclean  
   #备份当前目录下package.json
   npm run bootstrap  
   #这一步卡住的话ctr+c终止，将备份的package.json覆盖当前pakage.json再执行npm run bootstrap
   ```

   

3. benchmark环境构建，安装caliper-cli

   ```
   cd ./packages/caliper-tests-integration
   npm run start_verdaccio
   #我的是macos，这一步会卡住，pm2启动不了verdaccio，那么直接执行以下命令：
   pm2 start verdaccio -- -l 0.0.0.0:4873 -c scripts/config.yaml
   此时启动成功，接着发布包：
   npm run publish_packages
   安装包：
   npm run install_cli
   ```

   

4. 测试

   ```
   BENCHMARK=fabric npm run run_tests
   ```

   

   

   

