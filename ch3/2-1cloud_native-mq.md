---
authors: [""]
company: ["腾讯云"]
reviewers: ["刘如明"]
---

# (二)	云原生编排及管理

## 1.	云原生消息队列

**消息队列是指利用高效可靠的消息传递机制进行与平台无关的数据交流，并基于数据通信来进行分布式系统的集成。** 传统应用架构设计中**系统组件与应用紧耦合，** 消费者出现任何问题（升级停服、宕机、不可用等），都会影响生产者的业务；**系统可用性和效率低，** 突发的海量消息压力，消费者无法实时高效的处理消息时，容易产生雪崩效应；**缺少持久化机制，** 系统发生故障会丢失消息；**消息本地存储难扩展，** 单机的处理能力和内存容量都是有限的，不具备可扩展性，同时系统组件高度耦合，扩展难度大。

为解决传统架构中的种种问题，云原生消息队列服务应运而生，它为微服务和事件驱动架构提供核心的解耦、异步和削峰的能力。通过消息队列能够让用户很容易架构出分布式的、高性能的、弹性的、鲁棒的应用程序。

**程序组件与应用解耦分离独立运行，** 同时还可以简化组件间的消息管理。分布式应用程序的任何组件均可将消息存储在队列中， 云  云消息服务 确保每条消息至少传送一次，并且支持多次读取和写入。单个队列可由多个分布式应用程序组件同时使 用而无需这些组件之间的互相协作。所有组件均可使用云消息服务API以编程方式检索和操作消息。

**可靠的基于消息的异步通信机制，** 能够将分布式部署的不同应用（或同一应用的不同组件）之间的收发消息，存储在可靠有效的  消息队列中，防止消息丢失。云原生消息队列支持多进程同时读写，收发互不干扰，无需各应用或组件始终处于运行状态。

**消息同步多副本落盘保障消息高可靠，** 通过分布式 Raft 等算法保证消息强一致，提供消息队列、发布订阅、消息回溯、延时消息、顺序消息、消息轨迹等服务。具有高可靠、高可用、高性能、动态伸缩等优势。

云消息服务不仅具备处理系统解耦，异步通信等传统消息队列所必备的能力，而且在数据的可靠传递，性能，快速部署等方面提供有力的支持，满足使用者针对特定场景下的消息的高可靠堆积，动态扩缩容，系统监控，消息轨迹查询等方面的需求。