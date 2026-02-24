---
name: hmi-scene
description: "Design and maintain industrial HMI/Scratch-like scenes for C++ projects. Create professional human-machine interface screens with drag-and-drop components, animations, data binding, and real-time interactions similar to KingView, WinCC, and other industrial HMI software."
license: MIT
---

# HMI Scene Editor - 工业人机界面场景编辑器

## 项目概述

这是一个基于C++的专业工业HMI（人机界面）场景编辑器，参考组态王、WinCC等工业自动化软件的设计理念。

### 技术架构
- **运行时UI**: Qt框架 (QGraphicsScene/QGraphicsItem)
- **场景定义**: JSON格式存储在 `scenes/*.json`
- **代码生成**: 每个场景JSON编译为C++代码在 `src/generated_scenes/`
- **组件系统**: 模块化widget设计，支持自定义扩展
- **数据绑定**: 支持PLC/SCADA数据实时绑定

### 核心功能特性

#### 0. 工具栏和交互系统
参考专业HMI编辑器的工具栏设计，提供直观的工具切换和交互体验：

**工具栏工具**
- `Select` - 选择工具（箭头），用于选择、移动和编辑组件
- `Line` - 直线绘制工具
- `Rectangle` - 矩形绘制工具
- `Ellipse` - 椭圆绘制工具
- `Text` - 文本添加工具
- `Image` - 图片添加工具
- `Industrial` - 工业组件选择器

**智能工具切换**
- **自动切换到选择模式**：绘制完成后（松开鼠标）自动切换回选择工具（箭头模式），方便立即编辑刚创建的组件
- **连续绘制**：按住Shift键可保持当前绘制工具模式，实现连续绘制
- **工具锁定**：添加工具锁定按钮，防止意外切换
- **快捷键**：支持工具切换快捷键（如V键快速切换到选择工具）

#### 1. 组件库系统
参考组态王、WinCC的丰富组件库，提供以下组件类型：

**基础组件**
- `Button` - 按钮组件，支持多种样式和交互
- `Label` - 文本标签，支持动态文本更新
- `Image` - 图像显示组件
- `Shape` - 基本图形（矩形、圆形、线条等）

**工业组件**
- `Tank` - 液位罐/容器显示
- `Valve` - 阀门控制组件
- `Pump` - 泵状态显示和控制
- `Motor` - 电机状态和控制
- `AnalogMeter` - 模拟仪表盘
- `DigitalMeter` - 数字显示表
- `Indicator` - 指示灯（红/绿/黄）
- `Gauge` - 仪表盘
- `Slider` - 滑块控制器
- `ProgressBar` - 进度条

**高级组件**
- `TrendChart` - 趋势图
- `BarChart` - 柱状图
- `PieChart` - 饼图
- `AlarmList` - 报警列表
- `DataGrid` - 数据表格
- `DateTime` - 日期时间显示
- `TabWidget` - 标签页容器
- `GroupBox` - 分组框

**逻辑组件**
- `BlockIf` - 条件判断块
- `BlockLoop` - 循环块
- `BlockTimer` - 定时器块
- `BlockCounter` - 计数器块
- `BlockMath` - 数学运算块

#### 2. 拖拽式界面设计
- **所见即所得**: 实时预览设计效果
- **智能对齐**: 自动吸附和对齐辅助线
- **网格系统**: 可配置的背景网格
- **缩放功能**: 支持画布缩放和平移
- **多选操作**: 支持框选多个组件
- **复制粘贴**: 组件复制和粘贴功能
- **撤销重做**: 完整的操作历史记录

#### 3. 属性编辑器
参考WinCC的属性面板设计：

**通用属性**
- `id` - 唯一标识符
- `name` - 显示名称
- `position` - 位置坐标 (x, y)
- `size` - 尺寸 (width, height)
- `visible` - 可见性
- `enabled` - 启用状态
- `zOrder` - 层级顺序

**外观属性**
- `backgroundColor` - 背景颜色
- `foregroundColor` - 前景颜色
- `borderColor` - 边框颜色
- `borderWidth` - 边框宽度
- `borderStyle` - 边框样式
- `font` - 字体设置
- `opacity` - 透明度
- `image` - 背景图像

**交互属性**
- `clickable` - 可点击
- `draggable` - 可拖拽
- `hoverEffect` - 悬停效果
- `cursor` - 鼠标样式

**数据绑定属性**
- `dataSource` - 数据源地址
- `dataType` - 数据类型
- `updateInterval` - 更新间隔
- `dataFormat` - 数据格式化
- `alarmThreshold` - 报警阈值

**动画属性**
- `animationType` - 动画类型
- `animationDuration` - 动画持续时间
- `animationLoop` - 循环播放
- `animationTrigger` - 触发条件

#### 4. 数据绑定系统
参考组态王的数据绑定机制：

**数据源类型**
- `PLC` - PLC寄存器地址
- `Database` - 数据库字段
- `Variable` - 内部变量
- `Expression` - 表达式计算
- `OPC` - OPC服务器节点
- `Modbus` - Modbus寄存器

**绑定模式**
- `Read` - 只读绑定
- `Write` - 只写绑定
- `ReadWrite` - 读写绑定
- `Event` - 事件触发

**数据转换**
- `Scaling` - 线性转换
- `Mapping` - 映射表转换
- `Formula` - 公式转换
- `Lookup` - 查找表转换

#### 5. 动画和效果
参考WinCC的动画系统：

**动画类型**
- `Fade` - 淡入淡出
- `Slide` - 滑动效果
- `Rotate` - 旋转动画
- `Scale` - 缩放动画
- `Blink` - 闪烁效果
- `ColorChange` - 颜色变化
- `Move` - 位置移动
- `Path` - 路径动画

**触发条件**
- `DataChange` - 数据变化
- `Timer` - 定时触发
- `UserAction` - 用户操作
- `Alarm` - 报警触发
- `Condition` - 条件满足

#### 6. 脚本系统
支持类似Scratch的积木式编程：

**事件积木**
- `OnStart` - 启动事件
- `OnClick` - 点击事件
- `OnDataChange` - 数据变化事件
- `OnTimer` - 定时器事件
- `OnAlarm` - 报警事件

**动作积木**
- `SetValue` - 设置值
- `GetValue` - 获取值
- `Show` - 显示
- `Hide` - 隐藏
- `Move` - 移动
- `Rotate` - 旋转
- `PlaySound` - 播放声音
- `LogMessage` - 记录消息
- `SendCommand` - 发送命令

**控制积木**
- `If` - 条件判断
- `Loop` - 循环
- `Wait` - 等待
- `Break` - 跳出循环
- `Return` - 返回

#### 7. 图层管理
- **图层列表**: 显示所有图层
- **图层顺序**: 调整图层前后顺序
- **图层锁定**: 锁定/解锁图层
- **图层可见性**: 显示/隐藏图层
- **图层分组**: 组件分组管理

#### 8. 模板和库管理
- **组件库**: 预定义组件库
- **场景模板**: 常用场景模板
- **自定义组件**: 用户自定义组件
- **导入导出**: 组件和场景的导入导出

## 如何帮助用户

当用户请求HMI/Scratch-like屏幕的更改时：

### 步骤1: 分析需求
1. 理解用户要创建的HMI场景类型
2. 确定需要的组件类型和数量
3. 识别数据绑定需求
4. 确定动画和交互要求

### 步骤2: 读取现有场景
1. 打开并阅读相关的场景JSON文件（位于 `scenes/`）
2. 分析现有组件结构和布局
3. 识别需要修改的部分

### 步骤3: 设计JSON差异
提出一个JSON差异，包括：
- 只涉及相关的组件/块
- 尽可能保留现有ID和布局
- 添加新组件时使用唯一ID
- 确保组件属性完整和正确

### 步骤4: 更新生成的C++文件
更新 `src/generated_scenes/` 下对应的生成C++文件，遵循该目录中的现有模式：
- 构造函数初始化
- 信号/槽连接
- 动画设置
- 数据绑定配置
- 事件处理

### 步骤5: 验证完整性
确保所有新组件/块都有：
- 唯一的ID
- 运行时交互的适当信号/槽连接
- 正确的z-order和对齐
- 完整的属性配置
- 数据绑定配置（如需要）

## 约定和规范

### 命名约定

**组件ID**
- 使用小写字母和下划线
- 描述性名称，如 `tank_water_level`, `valve_main`, `button_start`
- 避免使用保留字和特殊字符

**C++命名**
- 类名: `Scene_<SceneName>` (如 `Scene_MainControl`, `Scene_AlarmPanel`)
- 成员变量: `m_<widgetId>` (如 `m_tank_water_level`, `m_valve_main`)
- 方法名: `on<WidgetId><Event>` (如 `onButtonStartClicked`)

**文件命名**
- 场景JSON: `<SceneName>.json` (如 `MainControl.json`, `AlarmPanel.json`)
- 生成的C++: `scene_<scene_name>.cpp` 和 `scene_<scene_name>.h`

### 坐标系统
- 原点: 左上角 (0, 0)
- 单位: 像素
- X轴: 从左到右增加
- Y轴: 从上到下增加

### 组件类型规范

#### Tank（液位罐）
```json
{
  "type": "Tank",
  "id": "tank_water_level",
  "position": {"x": 100, "y": 100},
  "size": {"width": 200, "height": 300},
  "properties": {
    "maxLevel": 100,
    "currentLevel": 75,
    "color": "#4A90E2",
    "showScale": true,
    "showValue": true
  },
  "dataBinding": {
    "source": "PLC.D100",
    "type": "ReadWrite",
    "updateInterval": 1000
  }
}
```

#### Valve（阀门）
```json
{
  "type": "Valve",
  "id": "valve_main",
  "position": {"x": 350, "y": 150},
  "size": {"width": 80, "height": 80},
  "properties": {
    "valveType": "butterfly",
    "state": "closed",
    "color": "#FF6B6B",
    "showLabel": true
  },
  "dataBinding": {
    "source": "PLC.D200",
    "type": "ReadWrite",
    "updateInterval": 500
  },
  "events": {
    "onClick": "toggleValve"
  }
}
```

#### AnalogMeter（模拟仪表）
```json
{
  "type": "AnalogMeter",
  "id": "meter_pressure",
  "position": {"x": 500, "y": 100},
  "size": {"width": 150, "height": 150},
  "properties": {
    "minValue": 0,
    "maxValue": 100,
    "currentValue": 65,
    "unit": "bar",
    "color": "#50C878",
    "showValue": true
  },
  "dataBinding": {
    "source": "PLC.D300",
    "type": "Read",
    "updateInterval": 2000
  }
}
```

#### Button（按钮）
```json
{
  "type": "Button",
  "id": "button_start",
  "position": {"x": 100, "y": 450},
  "size": {"width": 120, "height": 40},
  "properties": {
    "text": "启动",
    "backgroundColor": "#4CAF50",
    "textColor": "#FFFFFF",
    "borderRadius": 5,
    "fontSize": 16
  },
  "events": {
    "onClick": "startSystem"
  }
}
```

#### Indicator（指示灯）
```json
{
  "type": "Indicator",
  "id": "indicator_status",
  "position": {"x": 250, "y": 460},
  "size": {"width": 30, "height": 30},
  "properties": {
    "state": "green",
    "blink": false,
    "shape": "circle"
  },
  "dataBinding": {
    "source": "PLC.D400",
    "type": "Read",
    "updateInterval": 1000
  }
}
```

### 工具栏状态管理实现

#### 技术实现细节

```cpp
// 工具栏类
class HMIToolbar : public QToolBar {
private:
    QAction* selectToolAction;
    QAction* lineToolAction;
    QAction* rectToolAction;
    QAction* ellipseToolAction;
    QAction* textToolAction;
    QAction* imageToolAction;
    QAction* industrialToolAction;
    
    QString currentTool;
    bool toolLocked;
    
public:
    HMIToolbar(QWidget* parent = nullptr);
    
    // 切换到指定工具
    void switchToTool(const QString& toolName);
    
    // 获取当前工具
    QString getCurrentTool() const { return currentTool; }
    
    // 工具锁定状态
    void setToolLocked(bool locked) { toolLocked = locked; }
    bool isToolLocked() const { return toolLocked; }
};

// 绘制工具基类
class DrawingTool {
protected:
    HMIToolbar* toolbar;
    QGraphicsScene* scene;
    bool shiftPressed;
    
public:
    void setToolbar(HMIToolbar* tb) { toolbar = tb; }
    void setScene(QGraphicsScene* s) { scene = s; }
    
    // 键盘事件处理
    void onKeyPress(QKeyEvent* event) {
        if (event->key() == Qt::Key_Shift) {
            shiftPressed = true;
        }
    }
    
    void onKeyRelease(QKeyEvent* event) {
        if (event->key() == Qt::Key_Shift) {
            shiftPressed = false;
        }
    }
    
    // 绘制完成后调用此方法
    void finishDrawing() {
        // 检查是否需要切换工具
        if (toolbar && !toolbar->isToolLocked() && !shiftPressed) {
            toolbar->switchToTool("select");
        }
    }
};

// 直线工具示例
class LineTool : public DrawingTool {
private:
    QGraphicsLineItem* currentLine;
    QPointF startPoint;
    
public:
    void onMousePress(QMouseEvent* event) {
        startPoint = scene->mouseGrabberItem() ? 
            scene->mouseGrabberItem()->scenePos() : 
            scene->mapFromScene(event->pos());
        
        currentLine = new QGraphicsLineItem();
        currentLine->setLine(QLineF(startPoint, startPoint));
        scene->addItem(currentLine);
    }
    
    void onMouseMove(QMouseEvent* event) {
        if (currentLine) {
            QPointF endPoint = scene->mapFromScene(event->pos());
            currentLine->setLine(QLineF(startPoint, endPoint));
        }
    }
    
    void onMouseRelease(QMouseEvent* event) {
        if (currentLine) {
            // 完成直线绘制
            QPointF endPoint = scene->mapFromScene(event->pos());
            currentLine->setLine(QLineF(startPoint, endPoint));
            
            // 自动切换回选择工具
            finishDrawing();
        }
    }
};
```

#### 工具栏配置示例

```json
{
  "toolbar": {
    "tools": [
      {
        "id": "select",
        "name": "选择工具",
        "icon": "select.png",
        "shortcut": "V",
        "default": true
      },
      {
        "id": "line",
        "name": "直线工具",
        "icon": "line.png",
        "shortcut": "L"
      },
      {
        "id": "rectangle",
        "name": "矩形工具",
        "icon": "rect.png",
        "shortcut": "R"
      },
      {
        "id": "ellipse",
        "name": "椭圆工具",
        "icon": "ellipse.png",
        "shortcut": "E"
      },
      {
        "id": "text",
        "name": "文本工具",
        "icon": "text.png",
        "shortcut": "T"
      },
      {
        "id": "image",
        "name": "图片工具",
        "icon": "image.png",
        "shortcut": "I"
      },
      {
        "id": "industrial",
        "name": "工业组件",
        "icon": "industrial.png",
        "shortcut": "C"
      }
    ],
    "autoSwitchToSelect": true,
    "showTooltips": true,
    "enableShortcuts": true
  }
}
```

### 场景结构示例

```json
{
  "scene": {
    "name": "MainControl",
    "version": "1.0",
    "description": "主控制面板",
    "size": {"width": 1024, "height": 768},
    "backgroundColor": "#F5F5F5",
    "grid": {
      "enabled": true,
      "size": 20,
      "color": "#E0E0E0"
    },
    "widgets": [
      {
        "type": "Tank",
        "id": "tank_water_level",
        "position": {"x": 100, "y": 100},
        "size": {"width": 200, "height": 300},
        "properties": {...}
      },
      {
        "type": "Valve",
        "id": "valve_main",
        "position": {"x": 350, "y": 150},
        "size": {"width": 80, "height": 80},
        "properties": {...}
      }
    ],
    "connections": [
      {
        "from": "valve_main",
        "to": "tank_water_level",
        "type": "control"
      }
    ],
    "scripts": [
      {
        "event": "onClick",
        "target": "button_start",
        "actions": [
          {
            "type": "SetValue",
            "target": "valve_main.state",
            "value": "open"
          }
        ]
      }
    ]
  }
}
```

## 常见使用场景

### 场景1: 创建液位控制系统
1. 添加Tank组件显示液位
2. 添加Valve组件控制进出水
3. 添加Button组件手动控制
4. 配置数据绑定到PLC
5. 添加报警指示灯

### 场景2: 创建仪表盘面板
1. 添加多个AnalogMeter显示不同参数
2. 添加DigitalMeter显示精确数值
3. 配置数据源和更新频率
4. 设置报警阈值和颜色变化

### 场景3: 创建报警系统
1. 添加AlarmList组件显示报警
2. 配置报警条件和优先级
3. 添加声音和视觉报警
4. 创建报警确认按钮

### 场景4: 创建趋势图
1. 添加TrendChart组件
2. 配置数据源和时间范围
3. 设置多条曲线显示
4. 添加缩放和滚动功能

## 最佳实践

### 组件设计
- **一致性**: 使用统一的颜色方案和字体
- **层次性**: 重要信息突出显示
- **可读性**: 确保文本清晰可读
- **响应性**: 组件响应及时更新

### 工具栏使用技巧
- **自动选择模式**: 绘制完成后自动切换到选择模式，方便立即编辑刚创建的组件
- **连续绘制**: 按住Shift键可以保持在当前绘制工具模式，实现连续绘制
- **快速切换**: 使用快捷键V快速切换到选择工具
- **工具锁定**: 对于需要频繁使用的工具，可以锁定工具状态，防止意外切换
- **视觉反馈**: 注意工具栏按钮的状态变化，了解当前激活的工具

### 性能优化
- **批量更新**: 避免频繁的单独更新
- **懒加载**: 大型场景按需加载
- **缓存**: 缓存常用数据和图像
- **异步**: 使用异步数据更新

### 安全考虑
- **权限控制**: 实现用户权限管理
- **数据验证**: 验证所有输入数据
- **错误处理**: 完善的错误处理机制
- **日志记录**: 记录重要操作和事件

### 可维护性
- **模块化**: 组件设计模块化
- **文档化**: 完整的代码注释
- **版本控制**: 使用版本控制系统
- **测试**: 充分的单元测试和集成测试

## 故障排除

### 常见问题

**问题**: 组件不显示
- 检查visible属性
- 检查z-order设置
- 验证坐标是否在场景范围内

**问题**: 数据不更新
- 检查dataBinding配置
- 验证数据源地址
- 检查updateInterval设置

**问题**: 动画不播放
- 检查animationType设置
- 验证触发条件
- 检查animationDuration设置

**问题**: 点击事件不响应
- 检查clickable属性
- 验证events配置
- 检查信号/槽连接

## 扩展开发

### 添加自定义组件
1. 继承基础Widget类
2. 实现必要的虚函数
3. 添加自定义属性
4. 注册组件类型
5. 更新JSON序列化

### 添加新动画类型
1. 实现动画接口
2. 定义动画参数
3. 实现动画逻辑
4. 注册动画类型
5. 更新UI编辑器

### 集成新数据源
1. 实现数据源接口
2. 配置连接参数
3. 实现数据读写
4. 添加错误处理
5. 更新绑定系统

## 参考资源

### 工业HMI软件参考
- **组态王**: 丰富的组件库和脚本系统
- **WinCC**: 强大的数据绑定和报警系统
- **Intouch**: 优秀的图形编辑和动画功能
- **FactoryTalk View**: 全面的SCADA集成
- **Ignition**: 现代化的Web-based HMI

### Qt框架资源
- **QGraphicsScene**: 2D图形场景管理
- **QGraphicsItem**: 图形项基类
- **QPropertyAnimation**: 属性动画
- **QStateMachine**: 状态机
- **QDataWidgetMapper**: 数据绑定

### 设计模式
- **MVC模式**: 模型-视图-控制器分离
- **观察者模式**: 数据变化通知
- **工厂模式**: 组件创建
- **策略模式**: 动画策略
- **命令模式**: 撤销/重做

---

## 总结

这个HMI场景编辑器skill提供了创建专业工业人机界面的完整解决方案，结合了组态王、WinCC等成熟HMI软件的优秀特性，使用现代C++和Qt框架实现。通过拖拽式界面、丰富的组件库、强大的数据绑定和灵活的脚本系统，用户可以快速创建功能强大、美观实用的HMI应用。