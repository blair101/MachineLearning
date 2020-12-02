
# "App Get Coupons" Robot Assistant

聊天机器人（chatbot），也被称为会话代理或对话系统，现已成为了一个热门话题。微软在聊天机器人上押上了重注，Facebook（M）、苹果（Siri）、谷歌 和 Slack 等公司也是如此。 新一波创业者们正在尝试改变消费者与服务的交互方式。

# 技术方案详细设计一期

## 1. 整体架构和流程

### 各模块交互关系

## 2. 机器人后端

2.1 表结构定义

## 3. 数据服务

### 3.1 语言理解模块

#### 3.1.1 词法分析（分词及词性标注）

### 3.2 问答模块

一期只做单轮问答，根据用户输入语句进行一次性回答，识别到推荐语义时搜索领券内部数据生成回答返回给用户。
后期可扩展此模块，可搜索其他数据（比如卡券，客服系统等）支持更多业务，也可深入研究进行多轮问答。
内部数据需要新增多个索引方便搜索数据，


#### 3.1.2 意图理解

根据词法分析结果，理解用户意图，具体详见流程图部分

3.1.2.1 否定语义理解

判断语句是否包含否定词，若包含则属于否定语义，进行否定场景回复

3.1.2.2 推荐语义理解

判断语句是否包含优惠词，若包含则提取优惠词，属于推荐语义
遍历语句所有名词，形容词，判断是否命中分类词 category
遍历语句所有名词，判断是否命中券店关键词 coupon, shop etc.
--提前排序规则，分类，券店关键词

3.1.2.3 闲聊

其他情况认为闲聊


## 4. 聊天模块

### 4.1 方案选择

1. 图灵机器人(tuling123)
2. 基于深度学习的seq2seq模型

> 一期: tuling 123
> 二期: seq2seq

## 5. 历史数据


