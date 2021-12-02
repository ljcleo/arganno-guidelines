# 标注逻辑

![标注示例](标注示例.png)

- 目标：为句子中的成分标注其语义角色；
- 方法：以**谓词 Predicate** 为中心，根据谓词的语境义选择对应的**角色集 Roleset**，再查阅角色集对句子中的语义成分进行参数 Argument 标注。

## 谓词 Predicate

描述客体性质、特征或者客体之间关系的词项，可以理解为“主题词”或“关系词”；不一定为谓语动词，也可以名词、动名词形容词或词组的形态出现。

例如，right 作为名词的角色集如下所示：

![谓词](谓词.png)

## 角色集 Roleset

一个谓词可能对应多个语义，一个语义可以限定一组语义角色（编号参数）集合，我们称之为“角色集”。每个谓词至少拥有一个角色集，标注者需要进行角色集选择。

例如，leave 的两个角色集如下所示：

![角色集](角色集.png)

## 参数 Argument

语义角色的分类标签，包括编号参数（Numbered Arguments）和修饰参数（ARG-M）。

### 编号参数 Numbered Arguments（ARG0, ARG1, ..., ARGA）

反映需要与谓词搭配的特定元素，或通常与谓词一起出现的成分，例如一个动作的发出者、接收者和受益者，动作的起始点、终止点等。通常而言，ARG0是原型动因（Prototypical Agent），ARG1 是原型受动者（Prototypical Patient）或者主题（Theme）。角色集就是编号参数的集合，可以理解为谓词某一用法下的语义主干单元。

通常每个角色集都针对其应用场景定义了所有相关的编号参数，但在极少数情况下，一个谓词在句中可能对应超过一个原型动因，但相关义项的角色集只定义了其中一个。此时，可以用 ARGA 表示剩余的所有原型动因。

![参数标签](参数标签.png)

### 修饰参数 Modifier（ARGM-*）

编号参数组成主干语义，而修饰参数对谓词进行功能性修饰。一般是不同功能的定语
或状语修饰语，如下表所示。

| 标签 | 注释                           |
| ---- | ------------------------------ |
| ADJ  | 通用形容词 Adjective           |
| ADV  | 通用副词 Adverb                |
| CAU  | 起因 Cause                     |
| COM  | 共格者 Comitative              |
| CXN  | 形容词结构 Construction        |
| DIR  | 方向 Directional               |
| DIS  | 连接词 Discourse               |
| EXT  | 范围 Extent                    |
| GOL  | 目标 Goal                      |
| LOC  | 地点 Locative                  |
| LVB  | 轻动词 Light verb              |
| MNR  | 方式 Manner                    |
| MOD  | 情态动词 Modal                 |
| NEG  | 否定词 Negation                |
| PRD  | 第二谓语 Secondary Predication |
| PRP  | 动机 Purpose                   |
| REC  | 反身词 Reciprocal              |
| TMP  | 时间 Temporal                  |

*注：类别标签的详细说明与用例请查阅[修饰参数用例](modifier.md)。*
