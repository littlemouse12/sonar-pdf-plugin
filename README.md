编译:mvn clean package -Dmaven.test.skip=true

Sonar PDF Report Plugin
=========================

适用SonarQube版本 : 5.5--7.5。

- 2.0.X：适用SONARQUBE5.5--5.6.7版本
- 2.1.x：适用SONARQUBE6.0-6.2版本
- 3.0.x：适用SONARQUBE6.3+

## Description / Features

本插件生成PDF格式的sonarqube报告.

报告包括以下内容:

* 概要

* 静态分析

* 动态分析

* 编码问题

* 热点:
  * 违反最多的规则TOP10
  * 违规最多的文件TOP5
  * 复杂度最高的文件TOP5
  * 重复行最多的文件TOP5

* 违规详情

* 子模块信息（只有在存在时生成）


## Installation

1. 下载对应的版本，将插件复制到SONARQUBE_HOME/extensions/plugins 目录
1. 重启SonarQube

## Usage

SonarQube PDF是一个 post-job任务. 因此，PDF 报告将在SonarQube分析结束后生成.

### Configuration

配置Skip为“否”时生成PDF报告功能启用。

配置Username和Password。如果出现HTTP error: 401或者HTTP error: 403, msg: Forbidden，请查看该配置。

![Plugin Configuration](configuration.jpg?raw=true "Plugin Configuration")

### Download the report

5.x版本：PDF在仪表盘中下载，如果没有下载界面，需要在“配置控件”中添加该控件

![PDF Report example](output.jpg?raw=true "PDF Report example")

6.x以及7.x版本：因为UI变化无仪表盘页面，在工程中More菜单下查看![1546412064834](output6.png)



