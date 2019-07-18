# 操作指南

{{indexmenu_n>4}}

## 基本操作

### 启动PostgreSQL实例

如果要启动处于关闭状态的PostgreSQL实例，首先选择需要启动的PostgreSQL实例，在右侧详情页，点击“启动”按钮，弹出的确认对话框选择确定，即可启动PostgreSQL实例。

![image](/images/pgv4start.png)

![image](/images/pgv4start1.png)

如果需要同时启动多个PostgreSQL实例，选择相应的PostgreSQL实例，选择列表页面上方的“启动”，弹出的对话框选择“确定”，即可启动多个PostgreSQL实例。

**关闭PostgreSQL实例**

操作步骤参考启动PostgreSQL实例。

### 重启PostgreSQL实例

操作步骤参考启动PostgreSQL实例。

### 删除PostgreSQL实例

操作步骤参考启动PostgreSQL实例。

## 从库管理

用户可以对PostgreSQL实例的主库（Master）创建从库（standby）。从库不支持批量创建，一次只能针对一个PostgreSQL实例的主库（Master）。

选中PostgreSQL实例，点击“创建从库”。

![image](/images/pgv4slave.png)

在弹窗中输入从库（standby）的名称。

![image](/images/pgv4slave1.png)

点击“确定”之后，进入付费页面，确认付费之后，从库（standby）购买成功并进行初始化和数据同步。

初始化时间取决于数据量大小。

## 日志管理

### 日志分类

PostgreSQL实例的日志目前只有数据库binlog日志。

### 日志下载

点击资源列表中“详情”到资源管理页面，选择备份管理-\>日志包，点击打包日志即可打包数据库日志。

![image](/images/pgv4log2.png)

## 配置升降级

选中PostgreSQL实例，在操作项中选定配置升降级进行操作。

![image](/images/pgv4updata.png)

![image](/images/pgv4updata1.png)

配置升降级开始后，PostgreSQL实例状态显示为“升级”，升级结束后，状态恢复为初始状态。

## 备份管理

### 数据备份

备份分为自动备份和手动备份两种，自动备份每天进行一次例行备份（默认备份时间为0：00-4：00的某一整点，备份可以保存7天），备份来源可以选择从主库或从库进行备份。

PostgreSQL实例支持手动备份，用户可以保存某些关键时间点的重要数据备份，当前手工备份的允许保留个数为3个，如果超过3个，会自动删除最早的手动备份。创建手动备份时，用户只需要输入备份名称，后台会立刻开始进行备份工作。

查看所有PostgreSQL实例的备份文件，点击左侧导航栏的“备份管理”即可。

对于某一实例，进入实例管理页面，点击备份管理，选择手工备份之后，弹出对话框可以输入备份名称。

![image](/images/pgv4backup.png)

![image](/images/pgv4backup1.png)

### 备份下载

用户可以下载自动备份和手工备份生成的备份文件。

查看对应PostgreSQL实例的备份文件，选择对应的PostgreSQL实例，进入实例管理页面，点击备份管理，之后即可打开PostgreSQL实例备份列表。

点击下载即可弹出下载框进行下载。

如果备份文件超过1G，建议通过wget或curl下载至云主机（UHost）。

### 备份创建PostgreSQL实例

用户可以选择备份文件创建PostgreSQL实例。创建过程可参考快速上手文档。

备份文件压缩比为5:1，建议创建时的磁盘空间大小为备份文件大小的5倍以上。初始化时间取决于数据量大小。

## 配置文件

用户可以在左侧导航栏选择配置文件，进入配置文件管理页。

配置文件是PostgreSQL实例启动所需的重要组成，涉及相关的参数配置。PostgreSQL实例都需要使用特定的配置文件，UCloud提供默认配置文件，默认配置文件不可以修改。

### 导入配置文件

除了提供的默认配置文件外，用户也可以导入自定义配置文件，以便让PostgreSQL实例使用该配置。

点击配置文件上方的“导入”按钮，在弹出的输入框中填写“配置名称”、“描述”、“DB类型”，并选择本地的配置文件，点击确定后，即可完成导入。

![image](/images/pgv4config.png)

![image](/images/pgv4config2.png)

### 创建配置文件

除导入配置文件外，也可以直接在配置文件管理页创建配置文件。

点击“创建”按钮，在弹出对话框中输入“配置名称”、“描述”、“DB类型”，并且可以选择从哪一个现有配置中进行复制，点击“确定”后即可完成配置文件的创建操作。

![image](/images/pgv4config1.png)

### 查看配置文件

在配置文件列表中选择指定的配置文件，点击“详情”，可以查看其当前的所有参数项。

![image](/images/pgv4config3.png)

“使用该配置的数据库”显示哪些PostgreSQL实例使用了该配置文件。

### 编辑配置文件

在配置文件列表中选择自定义配置文件，点击“编辑”，可以查看其当前的所有参数项并可以进行编辑。

![image](/images/pgv4config4.png)

自定义参数需参考范围和字符类型。默认配置文件不允许编辑修改。如果用户需要在默认配置文件的基础上进行修改，可以选择将默认配置文件另存为新配置文件，创建成功后即可在新配置文件上进行自定义修改。

### 更改配置文件

对于PostgreSQL实例，用户可以更改当前配置文件。

选中PostgreSQL实例，在操作项中选择“修改配置文件”，在弹出的对话框中，选择需要更改的配置文件即可。

![image](/images/pgv4config5.png)

修改配置文件需要在重启实例后生效。

### 删除配置文件

配置文件支持删除操作。在配置文件列表页选中需要删除的配置文件，选中删除即可完成删除操作。

默认配置文件不可删除。

## 操作日志

### 查看操作日志

选中PostgreSQL实例，在右侧详情页选择查看操作日志。

![image](/images/pgv4log1.png)