---
title: 盘点Move的重要特性
weight: 31
---

```
* 本文由Starcoin社区原创
```

## 与Move结缘

Move 是一个面向数字资产的静态类型编程语言，它源于 2019年 Facebook 发布的 Libra，在 Starcoin 上得到了长足的发展。Starcoin 是全球第一个使用 Move 作为智能合约编程语言的公链项目，于 2021年中主网启动，其对 Move 的使用让我们看到了一个更美好的数字资产时代。

![1640831288496](https://tva1.sinaimg.cn/large/008i3skNly1gy8c645qz9j30d007mmye.jpg)



## 面向资源编程的Move

说到 Move 编程语言，不得不提的是其面向资源编程的设计理念。这一理念受到了各界的好评，甚至有人评价这是 Libra 中最亮眼的部分。Move 允许开发者编写程序，灵活地管理和转移资产，同时提供安全和保护措施，防止这些资产受到攻击。在数字资产时代，这似乎是所有平台应该给予的基本保障，但事实却令人沮丧，我们已经看到了一次又一次的资产被盗事件。Move 编程语言通过资源定义与控制权限分离、静态类型、泛型、模块系统、形式化验证等特性使得智能合约语言更适合其面向资产的场景，从智能合约层面保障数字资产的安全。



### Move的Ability

资源定义与权限控制分离，不仅明确了资源属性，更是给用户更大的操作空间。区块链给了我们重新掌控信息所有权的可能，在信息转变为资源，甚至转变为资产的过程中，我们面临的问题是如何更好的定义其属性，是普通的可以无限复制的信息，还是仅此一份归属于某人的资产。Move 编程语言抽象了资源的四个属性，可复制（copy)、可索引(key)、可丢弃(drop)、可储存(store)，通过这四个属性的不同组合，用户可以方便的定义出任何类型的资源。比如用户可以通过 key + copy + drop + store 的组合定义出一个普通的信息类型，通过 key + store 的组合定义出一个资产类型，这样的定义使得复制增发问题几乎不会存在，而现阶段流行的 EVM，则需要开发者从个人心智的角度保证资产是安全的。Move 通过对资源操作权限的抽象，用户可以明确定义资源可被操作的行为，从而将自己的注意力转移至其他更应该被关注的地方，从而提高创造性。



### 静态类型的Move

Move 采用的是静态类型系统，其本质上是一种逻辑约束。相比 EVM 来说要严格地多。现代的编程语言比如 Rust, Golang, Typescript 都不约而同采用了静态类型系统，他们的优点是，很多编程低级错误都可以在编译的时候发现，而不是拖到运行期才出现问题。对于开发者来说，这无疑是增加了一些障碍，更严格的约束要求开发者有更多的思考，Web2 对效率的极致追求使得开发者对 Bug 容忍度大大增加，但当我们意识到这是在面向资产的智能合约领域时，我们会毫无疑问的支持这一特性。



### 泛型编程

泛型的使用则使得 Move 灵活性大大增加，我们可以为数据结构和函数方法引入泛型，从而使得功能相同的代码只需要被实现一次就可以在多个类型上产生作用。比如用户想定一个保险箱，除开存储的资产类型不一致外，保险箱的其他功能基本相同，在这样的场景下，Move 可以方便的使用泛型进行实现，并且代码结构非常简洁明了。更加值得一提的是，与以太坊 EVM 平台相比，Move 模块系统不支持循环递归依赖，完美的解决合约重入漏洞。



### 成熟的形式化验证工具

Move 语言另外一个杀手级特性是支持形式化验证。形式化验证是一种基于数学和逻辑学的方法，在智能合约部署之前，对其代码和文档进行形式化建模，然后通过数学的手段对代码的安全性和功能正确性进行严格的证明，可有效检测出智能合约是否存在安全漏洞和逻辑漏洞。形式化验证必将成为智能合约编程必不可少的工具。



## Starcoin & Move

Starcoin 使用 Move 编程语言构建了 Stdlib， 各种面向资源的应用可以方便的进行构建。Move 编程语言的诸多特性保障了资源的安全，为了方便社区构建良好的生态，Starcoin 搭建了 Stdlib。这是一个集常用模块、协议模块、区块共识模块一体的工具模块，开发者可以使用它方便的定义出 Token、NFT等应用，也可以使用其进行链上治理，方便构建稳健的社区，其中甚至还包含了一个通用的流动性挖矿的模块，如果项目中需要加入这一激励特性，可以十分方便的实现。这一通用模块给了开发者极大的便利，使得开发者们能够聚焦生态建设。Move 语言给 Starcoin 带来了更安全的智能合约环境，Stdlib 则是构建了生态发展的基石，可以预见 Starcoin 上定会构建出一个更完善、更可靠的生态空间。

![1640831743862](https://tva1.sinaimg.cn/large/008i3skNly1gy8c6zlze8j30d006jjsc.jpg)

2019 年 Facebook 发布 Libra 时，Move 语言作为其中一部分被各界评价为极具未来性，那么 2021 年当下， Starcoin 正在一步步实现我们那个期待的未来。