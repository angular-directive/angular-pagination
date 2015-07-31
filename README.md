#angular-pagination


### 关于
* 基于angular 编写的可复用分页指令



### 安装

- 项目使用可以直接 `bower install angular-paginationjs` 下载 ，学习的同学可参照下面步骤
```
克隆项目到本地
git clone https://github.com/febobo/angular-pagination.git

要跑demo环境要求
node , bower , npm , gulp

安装
npm install && bower install

运行
gulp serve

```

### 使用
#### demo用法
#### html
```
<body ng-app="demo" ng-controller="demoCtro" class="row text-center">
    <div ui-pagination conf="conf"></div>
  </body>

```

#### js
```
var app = angular.module('demo' , ['pagination']);

  app.controller('demoCtro' , function($scope){

      $scope.title = 'pagination-directive';

      $scope.conf = {
        total : 1190,
        currentPage : 1,
        itemPageLimit : 1,
        isSelectPage : false,
        isLinkPage : false
      }

      // 监控你的页码 ， 发生改变既请求
      $scope.$watch('conf.currentPage + conf.itemPageLimit' , function(news){
         // 把你的http请求放到这里
         console.log($scope.conf.currentPage , $scope.conf.itemPageLimit)
      })
  })

```
### 参数说明
`total` : Number list总条数 必填 <br />
`currentPage` : Number 当前页 必填 <br />
`itemPageLimit` : Number 一页展示多少条 选填 默认为10<br />
`itemSelectPage` : 是否显示一页选择多少条下拉框  选填 默认为false展示 <br />
`isLinkPage` : 是否显示快速跳转框  选填 默认为false展示 <br />

#### Q&A
@febobo

