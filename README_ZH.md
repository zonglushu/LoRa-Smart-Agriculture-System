# LoRa 智慧农业系统 🌾🌱

<p align="center">
  <a href="your-build-link"><img src="https://img.shields.io/badge/build-passing-brightgreen" alt="Build Status"></a>
  <a href="your-license-link"><img src="https://img.shields.io/badge/license-MIT-blue" alt="License"></a>
  <a href="your-docs-link"><img src="https://img.shields.io/badge/docs-latest-blue" alt="Documentation"></a>
  <a href="your-spring-boot-link"><img src="https://img.shields.io/badge/Spring%20Boot-🚀-orange" alt="Spring Boot"></a>
  <a href="your-emq-link"><img src="https://img.shields.io/badge/EMQ-📈-blue" alt="EMQ"></a>
  <a href="your-vue3-link"><img src="https://img.shields.io/badge/Vue3-📊-green" alt="Vue3"></a>
  <a href="your-mybatis-link"><img src="https://img.shields.io/badge/MyBatis-📚-orange" alt="MyBatis-plus"></a>
  <a href="your-design-pattern-link"><img src="https://img.shields.io/badge/设计模式-🛠️-yellow" alt="设计模式"></a>
</p>

<p align="center">
  <a href="your-docs-link">📚 Documentation</a> |
  <a href="your-installation-link">🔧 Installation</a> |
  <a href="your-features-link">🌟 Features</a> |
  <a href="your-updates-link">📝 Updates</a> |
  <a href="your-contribute-link">🤝 Contribute</a>
</p>

## 介绍 📚

LoRa 智慧农业系统是一个创新的物联网架构，用于异构传感器集成与智能自动化。它以三个核心技术理念为指导，定义了其独特性与灵活性：

- **软件定义硬件**：通过动态配置文件定义硬件行为，实现硬件功能的灵活调整与扩展。 
- **业务流与执行流相分离**：解耦业务逻辑与执行流程，提升系统的灵活性与可维护性。 
- **元数据编程**：以元数据驱动系统逻辑，统一设备抽象、交互规则和数据标准。 

## 核心技术理念 🔩

### 1. 软件定义硬件 🛠️

硬件的行为（包括设备何时及如何交互、功能定义）通过配置文件动态定义，而非硬编码在软件或硬件中。

**实现方式** 📝

- **应用配置文件**：定义传感器与设备之间的交互规则，例如触发条件和协作工作流。 
- **插件描述文件**：动态注册硬件功能，实现热插拔和无缝硬件集成。 

**优势** 🌟

- 提高系统适应多样化农业场景需求的能力。
- 加速新设备的集成，降低开发和维护成本。 
- 构建可扩展的架构，支持未来的技术升级与硬件发展。 

---

### 2. 业务流与执行流相分离 🔄

通过将业务逻辑（“做什么”）与执行流程（“如何做”）解耦，系统避免了传统架构中业务逻辑嵌入硬件操作的局限性。这种设计促进了协作并增强了灵活性。

**实现方式** 📊

- 业务流专注于描述系统逻辑与目标。 
- 执行流负责设备驱动与底层命令执行，确保硬件操作j容性。 

**优势** 🌟

- 当元数据更新时，系统的业务逻辑可随之调整，同时保持逻辑框架的稳定性。 
- 简化开发流程，减少硬编码依赖，增强系统的可配置性与扩展能力。 
- 提供统一的基础支持，覆盖业务流、执行流和硬件抽象。 

---

### 3. 元数据编程 📊

元数据驱动系统逻辑，是实现软件定义硬件和业务流与执行流分离的基础支撑。元数据封装了系统运行所需的核心信息。

**关键元数据元素** 🔑

1. **插件描述文件**：在软件中抽象硬件，支持多种设备的动态注册与操作。 
2. **应用配置文件**：定义硬件组件间的协作规则，实现无缝交互。 
3. **Schema 文件**：规范数据格式和命令结构，确保系统内的标准化。 
4. **转换文件**：通过标准化集成，实现外部设备与系统的兼容性。 

**优势** 🌟

- 当元数据更新时，系统的业务逻辑可随之调整，同时保持逻辑框架的稳定性。 
- 简化开发流程，减少硬编码依赖，增强系统的可配置性与扩展能力。 
- 提供统一的基础支持，覆盖业务流、执行流和硬件抽象。 

## 实现方案 📈

![](doc/images/achievement.png)

### 业务流 📊

- **指令解释单元**：将配置文件转换为对象，解析其中的内容，存储为系统可感知的数据结构。 
- **代理工厂**：根据配置文件生成代理对象，代理对象包含全部业务信息，包括硬件协作规则。 
- **自适应代码生成器**：为代理对象生成控制代码，完成业务流的具体逻辑操作。 

### 执行流 🔄

- **插件层**：将硬件抽象为插件，由插件管理层统一管理。 
- **硬件抽象层（HAL）**：定义硬件的标准化 API，供插件层调用。 
- **硬件插件层（HPL）**：封装具体硬件的驱动代码和功能实现。 
- **通信层**：基于 MQTT 协议，实现软硬件间的高效通信。 

### 数据格式与兼容性 📈

- **Schema Encoder**：将外部设备数据转换为系统 Schema 格式。 
- **Schema Decoder**：将系统生成的数据转换为外部设备兼容格式。 
- **数据转换文件**：定义外部与内部数据格式的映射规则。 

---

## 更新动态 📝

### 通信层：基于MQTT的消息处理架构 📱

通信层是 LoRa 智慧农业系统的关键模块，基于 MQTT 协议实现高效的消息收发流程。其架构如下：


![MQTT 通信层架构](doc/images/architecture-diagram-zh.png)

**架构组件** 🧩

1. **MQTTReq 生成中心**：生成发送至硬件设备的消息对象。 
2. **MQTT 消息发送中心**：将生成的消息发送到 MQTT 服务器。 
3. **MQTT 消息接收中心**：接收从硬件设备返回的消息。 
4. **消息分配中心**：根据接收到的 JSON 消息，将其分发到不同的消息解析单元。 
5. **Redis 缓存中心**：存储所有的消息数据，作为消息存储中心。 
6. **消息解析中心**：解析 MQTTRes 对象，并将结果分发到对应的服务。 
7. **服务分配中心**：将解析后的消息交由动态代理工厂生成所需的服务对象。 
8. **代理工厂**：动态生成服务代理对象，用于执行具体的数据库业务操作。 
9. **前端处理**：最终将处理结果返回至前端。 

**优势** 🌟

- **高效通信**：基于 MQTT 的消息收发模式确保消息传递的实时性和可靠性。 
- **模块化设计**：通过分层结构，确保系统的灵活性和可扩展性。 
- **数据持久化**：利用 Redis 缓存消息数据，提高系统的容错性。 

## 许可证 📜

此项目采用 MIT 许可证。 📜
