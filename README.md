# 项目PUSH到github上(自己学习使用)

### 创建 GitHub 仓库

​		1.登录你的 [GitHub 账户](https://github.com/)。

​		2.在右上角点击 “**+**” 按钮，然后选择 “**New repository**”。

​		3.填写仓库名称、描述等信息。

​		4.设置仓库为 “**Public**”（公开）或 “**Private**”（私有）。

​		5.点击 “**Create repository**” 按钮。

​		6.这将创建一个空的 GitHub 仓库，接下来你会获得一个仓库的 URL，例如：

```
`https://github.com/username/repository-name.git`
```

### 在本地初始化 Git 仓库并上传代码

​		1.打开终端。

​		2.进入你的项目文件夹。

​		3.初始化 Git 仓库。

```
git init
```

​		4.选择不想上传的文件夹

​				在你的项目根目录下创建一个 `.gitignore` 文件（如果已经存在，则直接编辑）

```
touch .gitignore
```

​		5.在 `.gitignore` 中添加要忽略的文件夹

```
# 忽略 build 和 devel 文件夹
build/
devel/
```

​		6.添加所有文件到 Git 追踪列表		

```
git add .
```

​		7.**提交**所有添加的文件，并写一条提交信息（如“Initial commit”）

```
git commit -m "Initial commit"
```

​		8.**连接远程仓库**：将本地仓库连接到 GitHub 仓库，使用你创建的仓库 URL（如`https://github.com/username/repository-name.git`）：

```
git remote add origin https://github.com/username/repository-name.git
```

​		9.**上传代码**到 GitHub 仓库

```
git push -u origin master
```



### 生成个人访问令牌

#### 生成个人访问令牌 (PAT)

1. 登录你的 GitHub 账户。

2. 前往 **[GitHub 令牌设置页面](https://github.com/settings/tokens)**。

3. 点击 **Generate new token** 按钮。

4. 在 **Note** 中添加一个描述（例如 “Git push token”）。

5. 在 Select scopes 部分选择权限：

   ​	如果只需要基本的仓库访问，选择 `repo` 权限。

6. 点击 **Generate token**。生成后会显示令牌，将其复制并妥善保存。

> **注意**：出于安全原因，令牌只能显示一次，之后将无法查看。

#### 使用令牌进行身份认证

1. 回到终端，重新执行 `git push -u origin master`。
2. 在 `Username for 'https://github.com':` 中输入你的 GitHub 用户名。
3. 在 `Password for 'https://username@github.com':` 中粘贴刚刚生成的令牌（不要使用实际的 GitHub 密码）。



### 本地修改代码后上传

#### 	查看修改状态

​		首先，查看有哪些文件被修改或新增：

```
git status
```

#### 	添加修改文件

​		将所有修改过的文件添加到 Git 的提交列表中

```
git add .
```

​		或者，只添加特定文件：

```
git add filename
```

#### 	提交修改

​		使用 `git commit` 创建一个新的提交，并为这次提交添加描述信息（如“Updated main.cpp with timing information”）：

```
git commit -m "Your commit message here"
```

#### 	推送到 GitHub

​		将本地的最新提交推送到 GitHub 仓库：

```
git push origin master
```





### 删除github的一个项目

要删除 GitHub 上的一个项目（仓库），请按照以下步骤操作：

1. **登录 GitHub**：使用你的账户登录 GitHub 网站。
2. **前往项目仓库**：在 GitHub 首页点击你的头像，找到 **Your repositories**，选择要删除的仓库。
3. **进入仓库的设置**：
   - 在仓库页面上方的菜单中，点击 **Settings**。
   - 滚动到页面底部，找到 **Danger Zone** 区域。
4. **删除仓库**：
   - 在 **Danger Zone** 区域中，找到 **Delete this repository** 按钮并点击。
   - GitHub 会提示你输入仓库的完整名称（如 `username/repository-name`），以确认删除。
   - 输入仓库名称后，点击 **I understand the consequences, delete this repository** 按钮。
5. **确认删除**：GitHub 将永久删除此仓库，所有内容都将无法恢复。