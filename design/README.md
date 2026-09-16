# ENikki 界面原型

本目录提供 ENikki 的桌面端和手机端高保真 HTML 原型。

> 当前主版本：[`enikki-ui.html`](enikki-ui.html)  
> 旧版存档：[`enikki-ui-v1.html`](enikki-ui-v1.html)

## 打开方式

直接用浏览器打开 [`enikki-ui.html`](enikki-ui.html)，无需依赖或本地服务器。

可以通过 URL 参数打开指定页面：

```text
enikki-ui.html?view=plan
enikki-ui.html?view=arrange&tab=transport
enikki-ui.html?view=arrange&tab=lodging
enikki-ui.html?view=arrange&tab=meals
enikki-ui.html?view=budget
enikki-ui.html?view=settings
```

编辑窗口：

```text
enikki-ui.html?view=plan&editor=add&type=checkin
enikki-ui.html?view=budget&expense=add
```

## 信息架构

主界面只保留三个一级入口：

```text
行程
安排
  ├── 交通
  ├── 住宿
  └── 用餐
预算
```

设置固定在右上角，负责导入导出、离线准备、数据源和隐私。

拍照打卡不作为独立一级页面。它通过计划时间线中的“添加”或“编辑”进入。

## 桌面端

### 行程工作台

行程页采用“日期 → 地图 → 时间线”三栏结构：

- 左侧选择日期和查看当天进度。
- 中间查看地图、点位和路线。
- 右侧直接编辑当天时间线。

![桌面行程工作台](preview-plan.png)

### 交通

![桌面交通](preview-transport.png)

### 住宿

![桌面住宿](preview-lodging.png)

### 用餐

![桌面用餐](preview-meals.png)

### 预算

支出明细位于主区域并完整列出全部支出，支持点击编辑和拖动排序；分类预算与
占比图表位于右侧。

![桌面预算](preview-budget.png)

### 设置

![桌面设置](preview-settings.png)

桌面六页总览见 [`preview-overview.png`](preview-overview.png)。

## 编辑流程

### 在时间线中添加或编辑安排

支持巡礼点、交通、住宿、用餐、拍照打卡和休息/备注。

![添加行程安排](preview-plan-add.png)

### 拍照打卡图片对比

点击“参考图”或“实拍图”空框后，按用途提供不同来源：

参考图：

- Anitabi
- 手机相册
- 本地文件

实拍图：

- 拍照
- 手机相册
- 本地文件

![参考图来源](preview-photo-source.png)

![实拍图来源](preview-photo-source-actual.png)

支持继续添加多组“参考图 + 实拍图”对比。

### 添加支出

支持分类、原始币种、双币种换算、付款人、分摊和收据。

![添加支出](preview-budget-expense.png)

## 手机端

手机端顶部固定“添加”和“设置”，底部使用三个入口：

```text
行程 | 安排 | 预算
```

交通、住宿和用餐通过“安排”半屏面板切换。

![手机端总览](preview-mobile-overview.png)

手机端详细页面：

- [行程](preview-mobile.png)
- [交通](preview-mobile-transport.png)
- [住宿](preview-mobile-lodging.png)
- [用餐](preview-mobile-meals.png)
- [预算](preview-mobile-budget.png)
- [设置](preview-mobile-settings.png)

### 手机添加安排

![手机添加安排](preview-mobile-plan-add.png)

### 手机实拍图来源

![手机实拍图来源](preview-mobile-photo-source-actual.png)

### 手机添加支出

![手机添加支出](preview-mobile-budget-expense.png)

## 原型范围

当前原型使用示例数据，所有按钮和表单用于演示交互，不连接真实后端。
