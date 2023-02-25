# ArkUI子系统JS API变更

OpenHarmony 3.1 Release版本相较于OpenHarmony 3.0 LTS版本，ArkUI子系统的API变更如下:

## 接口变更

| 组件类型   | 组件名称                      | 变更类型 | 变更说明                                                     |
| ---------- | ----------------------------- | -------- | ------------------------------------------------------------ |
| 通用事件   | 焦点事件 onFocus/onBlur       | 新增     | 新增焦点事件。                                               |
| 通用事件   | 鼠标事件 onHover/onMouse      | 新增     | 新增鼠标事件。                                               |
| 通用事件   | 组件区域变化事件 onAreaChange | 新增     | 新增组件区域（包括大小和位置）变化事件。                     |
| 通用属性   | 设置多态样式 stateStyles      | 新增     | 新增组件多态样式设置。                                       |
| 通用属性   | 触摸热区设置 responseRegion   | 新增     | 新增组件触摸热区设置。                                       |
| 通用属性   | 点击控制 touchable            | 新增     | 新增设置组件是否可以被触摸。                                 |
| 通用属性   | 焦点控制 focusable            | 新增     | 新增设置当前组件是否可以获焦。                               |
| 通用属性   | Popup控制 bindPopup           | 新增     | 新增popup自定义布局能力。                                    |
| 通用属性   | Menu控制 bindMenu             | 新增     | 新增menu自定义布局能力。                                     |
| 通用属性   | 悬浮态效果 hoverEffect        | 新增     | 新增设置当前组件悬停态下的悬浮效果。                         |
| 通用手势   | SwipeGesture                  | 新增     | 新增滑动手势。                                               |
| 基础组件   | Image                         | 新增     | 新增syncLoad属性设置是否同步加载。                           |
| 基础组件   | Swiper                        | 新增     | 新增cachedCount属性设置预加载子组件个数。                    |
| 基础组件   | Swiper                        | 新增     | 新增disableSwipe属性禁用组件滑动切换功能。                   |
| 基础组件   | Slider                        | 新增     | 新增垂直方向的滑动条。                                       |
| 基础组件   | TabContent                    | 新增     | 新增tabbar属性自定义布局能力。                               |
| 基础组件   | Marquee                       | 新增     | 新增跑马灯组件。                                             |
| 基础组件   | Gauge                         | 新增     | 新增数据量规图表组件。                                       |
| 基础组件   | PluginComponent               | 新增     | 新增插件组件。                                               |
| 基础组件   | TextArea                      | 新增     | 新增输入区域组件。                                           |
| 基础组件   | TextInput                     | 新增     | 新增输入框组件。                                             |
| 基础组件   | Toggle                        | 新增     | 新增状态组件。                                               |
| 容器组件   | List                          | 新增     | 新增列表项拖拽事件。                                         |
| 容器组件   | ScrollBar                     | 新增     | 新增滚动条组件。                                             |
| 容器组件   | Navigation                    | 新增     | 新增页面导航组件。                                           |
| 容器组件   | Stepper                       | 新增     | 新增步骤导航器组件。                                         |
| 容器组件   | StepperItem                   | 新增     | 新增步骤导航器导航项组件。                                   |
| 画布组件   | Canvas                        | 新增     | 新增画布组件。                                               |
| 画布组件   | Lottie                        | 新增     | 新增Lottie库的支持。                                         |
| 全局UI方法 | ActionSheet                   | 新增     | 新增列表选择弹窗。                                           |
| 基础组件   | Web                           | 新增     | 新增加载网页组件。                                           |
| 基础组件   | Checkbox                      | 新增     | 新增多选框组件，通常用于某选项的打开或关闭。                 |
| 基础组件   | CheckboxGroup                 | 新增     | 新增多选框群组组件，用于控制多选框全选或者不全选状态。       |
| 基础组件   | DatePicker                    | 新增     | 新增选择日期的滑动选择器组件。                               |
| 基础组件   | TextPicker                    | 新增     | 新增文本类滑动选择器组件。                                   |
| 基础组件   | PatternLock                   | 新增     | 新增图案密码锁组件，以宫格图案的方式输入密码，用于密码验证。 |
| 基础组件   | RichText                      | 新增     | 新增富文本组件，解析并显示HTML格式文本。                     |
| 基础组件   | Search                        | 新增     | 新增搜索框组件，用于提供用户搜索内容的输入区域。             |
| 基础组件   | Select                        | 新增     | 新增下拉选择菜单组件，可以让用户在多个选项之间选择。         |
| 基础组件   | TextClock                     | 新增     | 新增文本时钟组件。                                           |
| 容器组件   | Refresh                       | 新增     | 新增下拉刷新容器组件。                                       |
| 容器组件   | SideBarContainer              | 新增     | 新增侧边栏容器组件。                                         |
| 全局UI方法 | TextPickerDialog              | 新增     | 新增文本滑动选择器弹窗。                                     |
| 全局UI方法 | TimePickerDialog              | 新增     | 新增时间滑动选择器弹窗。                                     |
| 全局UI方法 | DatePickerDialog              | 新增     | 新增日期滑动选择器弹窗。                                     |