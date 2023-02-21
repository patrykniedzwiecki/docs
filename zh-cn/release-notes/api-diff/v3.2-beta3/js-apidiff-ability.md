# 元能力子系统JS API变更

OpenHarmony 3.2 Beta3版本相较于OpenHarmony 3.2 Beta2版本，元能力子系统的API变更如下:

## 接口变更

| 模块名 | 类名 | 方法/属性/枚举/常量 | 变更类型 |
|---|---|---|---|
| abilityDelegator                          | AbilityDelegator          | waitAbilityStageMonitor(monitor: AbilityStageMonitor, callback: AsyncCallback\<AbilityStage>): void;<br>waitAbilityStageMonitor(monitor: AbilityStageMonitor, timeout: number, callback: AsyncCallback\<AbilityStage>): void;<br>waitAbilityStageMonitor(monitor: AbilityStageMonitor, timeout?: number): Promise\<AbilityStage>; | 新增 |
| abilityDelegator                          | AbilityDelegator          | removeAbilityStageMonitor(monitor: AbilityStageMonitor, callback: AsyncCallback\<void>): void;<br>removeAbilityStageMonitor(monitor: AbilityStageMonitor): Promise\<void>;                                                                                                                                                    | 新增 |
| abilityDelegator                          | AbilityDelegator          | addAbilityStageMonitor(monitor: AbilityStageMonitor, callback: AsyncCallback\<void>): void;<br>addAbilityStageMonitor(monitor: AbilityStageMonitor): Promise\<void>;                                                                                                                                                          | 新增 |
| abilityStageMonitor                       | AbilityStageMonitor       | srcEntrance: string;                                                                                                                                                                                                                                                                                                           | 新增 |
| abilityStageMonitor                       | AbilityStageMonitor       | moduleName: string;                                                                                                                                                                                                                                                                                                            | 新增 |
| applicationInfo                           | ApplicationInfo           | readonly iconIndex: number;                                                                                                                                                                                                                                                                                                    | 新增 |
| applicationInfo                           | ApplicationInfo           | readonly labelIndex: number;                                                                                                                                                                                                                                                                                                   | 新增 |
| ApplicationStateObserver                  | ApplicationStateObserver  | onProcessStateChanged(processData: ProcessData): void;                                                                                                                                                                                                                                                                         | 新增 |
| context                                   | Context                   | getExternalCacheDir(callback: AsyncCallback\<string>): void<br>getExternalCacheDir(): Promise\<string>;                                                                                                                                                                                                                       | 新增 |
| lifecycle                                 | LifecycleForm             | onShare?(formId: string): {[key: string]: any};                                                                                                                                                                                                                                                                                | 新增 |
| MissionListener                           | MissionListener           | onMissionClosed(mission: number): void;                                                                                                                                                                                                                                                                                        | 新增 |
| ohos.ability.wantConstant                 | Action                    | DLP_PARAMS_INDEX = "ohos.dlp.params.index"                                                                                                                                                                                                                                                                                     | 新增 |
| ohos.ability.wantConstant                 | Action                    | DLP_PARAMS_ABILITY_NAME = "ohos.dlp.params.abilityName"                                                                                                                                                                                                                                                                        | 新增 |
| ohos.ability.wantConstant                 | Action                    | DLP_PARAMS_MODULE_NAME = "ohos.dlp.params.moduleName"                                                                                                                                                                                                                                                                          | 新增 |
| ohos.ability.wantConstant                 | Action                    | DLP_PARAMS_BUNDLE_NAME = "ohos.dlp.params.bundleName"                                                                                                                                                                                                                                                                          | 新增 |
| ohos.ability.wantConstant                 | Action                    | DLP_PARAMS_SANDBOX = "ohos.dlp.params.sandbox"                                                                                                                                                                                                                                                                                 | 新增 |
| ohos.ability.wantConstant                 | Action                    | ACTION_MARKET_CROWDTEST = "ohos.want.action.marketCrowdTest"                                                                                                                                                                                                                                                                   | 新增 |
| ohos.ability.wantConstant                 | Action                    | ACTION_MARKET_DOWNLOAD = "ohos.want.action.marketDownload"                                                                                                                                                                                                                                                                     | 新增 |
| ohos.abilityAccessCtrl                    | PermissionStateChangeInfo | permissionName: string;                                                                                                                                                                                                                                                                                                        | 新增 |
| ohos.abilityAccessCtrl                    | PermissionStateChangeInfo | tokenID: number;                                                                                                                                                                                                                                                                                                               | 新增 |
| ohos.abilityAccessCtrl                    | PermissionStateChangeInfo | change: PermissionStateChangeType;                                                                                                                                                                                                                                                                                             | 新增 |
| ohos.abilityAccessCtrl                    | PermissionStateChangeType | PERMISSION_GRANTED_OPER = 1                                                                                                                                                                                                                                                                                                    | 新增 |
| ohos.abilityAccessCtrl                    | PermissionStateChangeType | PERMISSION_REVOKED_OPER = 0                                                                                                                                                                                                                                                                                                    | 新增 |
| ohos.abilityAccessCtrl                    | AtManager                 | off(type: 'permissionStateChange', tokenIDList: Array\<number>, permissionNameList: Array\<string>, callback?: Callback\<PermissionStateChangeInfo>): void;                                                                                                                                                                    | 新增 |
| ohos.abilityAccessCtrl                    | AtManager                 | on(type: 'permissionStateChange', tokenIDList: Array\<number>, permissionNameList: Array\<string>, callback: Callback\<PermissionStateChangeInfo>): void;                                                                                                                                                                      | 新增 |
| ohos.abilityAccessCtrl                    | AtManager                 | getVersion(): Promise\<number>;                                                                                                                                                                                                                                                                                                | 新增 |
| ohos.application.Ability                  | Ability                   | onMemoryLevel(level: AbilityConstant.MemoryLevel): void;                                                                                                                                                                                                                                                                       | 新增 |
| ohos.application.AbilityConstant          | WindowMode                | WINDOW_MODE_FLOATING = 102                                                                                                                                                                                                                                                                                                     | 新增 |
| ohos.application.AbilityConstant          | WindowMode                | WINDOW_MODE_SPLIT_SECONDARY = 101                                                                                                                                                                                                                                                                                              | 新增 |
| ohos.application.AbilityConstant          | WindowMode                | WINDOW_MODE_SPLIT_PRIMARY = 100                                                                                                                                                                                                                                                                                                | 新增 |
| ohos.application.AbilityConstant          | WindowMode                | WINDOW_MODE_FULLSCREEN = 1                                                                                                                                                                                                                                                                                                     | 新增 |
| ohos.application.AbilityConstant          | WindowMode                | WINDOW_MODE_UNDEFINED = 0                                                                                                                                                                                                                                                                                                      | 新增 |
| ohos.application.AbilityConstant          | MemoryLevel               | MEMORY_LEVEL_CRITICAL = 2                                                                                                                                                                                                                                                                                                      | 新增 |
| ohos.application.AbilityConstant          | MemoryLevel               | MEMORY_LEVEL_LOW = 1                                                                                                                                                                                                                                                                                                           | 新增 |
| ohos.application.AbilityConstant          | MemoryLevel               | MEMORY_LEVEL_MODERATE = 0                                                                                                                                                                                                                                                                                                      | 新增 |
| ohos.application.AbilityLifecycleCallback | AbilityLifecycleCallback  | onWindowStageDestroy(ability: Ability, windowStage: window.WindowStage): void;                                                                                                                                                                                                                                                 | 新增 |
| ohos.application.AbilityLifecycleCallback | AbilityLifecycleCallback  | onWindowStageInactive(ability: Ability, windowStage: window.WindowStage): void;                                                                                                                                                                                                                                                | 新增 |
| ohos.application.AbilityLifecycleCallback | AbilityLifecycleCallback  | onWindowStageActive(ability: Ability, windowStage: window.WindowStage): void;                                                                                                                                                                                                                                                  | 新增 |
| ohos.application.AbilityLifecycleCallback | AbilityLifecycleCallback  | onWindowStageCreate(ability: Ability, windowStage: window.WindowStage): void;                                                                                                                                                                                                                                                  | 新增 |
| ohos.application.AbilityStage             | AbilityStage              | onMemoryLevel(level: AbilityConstant.MemoryLevel): void;                                                                                                                                                                                                                                                                       | 新增 |
| ohos.application.appManager               | ProcessState              | STATE_DESTROY                                                                                                                                                                                                                                                                                                                  | 新增 |
| ohos.application.appManager               | ProcessState              | STATE_BACKGROUND                                                                                                                                                                                                                                                                                                               | 新增 |
| ohos.application.appManager               | ProcessState              | STATE_ACTIVE                                                                                                                                                                                                                                                                                                                   | 新增 |
| ohos.application.appManager               | ProcessState              | STATE_FOREGROUND                                                                                                                                                                                                                                                                                                               | 新增 |
| ohos.application.appManager               | ProcessState              | STATE_CREATE                                                                                                                                                                                                                                                                                                                   | 新增 |
| ohos.application.appManager               | ApplicationState          | STATE_DESTROY                                                                                                                                                                                                                                                                                                                  | 新增 |
| ohos.application.appManager               | ApplicationState          | STATE_BACKGROUND                                                                                                                                                                                                                                                                                                               | 新增 |
| ohos.application.appManager               | ApplicationState          | STATE_ACTIVE                                                                                                                                                                                                                                                                                                                   | 新增 |
| ohos.application.appManager               | ApplicationState          | STATE_FOREGROUND                                                                                                                                                                                                                                                                                                               | 新增 |
| ohos.application.appManager               | ApplicationState          | STATE_CREATE                                                                                                                                                                                                                                                                                                                   | 新增 |
| ohos.application.Configuration            | Configuration             | hasPointerDevice?: boolean;                                                                                                                                                                                                                                                                                                    | 新增 |
| ohos.application.context                  | AreaMode                  | EL2 = 1                                                                                                                                                                                                                                                                                                                        | 新增 |
| ohos.application.context                  | AreaMode                  | EL1 = 0                                                                                                                                                                                                                                                                                                                        | 新增 |
| ohos.application.formError                | FormError                 | ERR_DISTRIBUTED_SCHEDULE_FAILED = 37                                                                                                                                                                                                                                                                                           | 新增 |
| ohos.application.FormExtension            | FormExtension             | onShare?(formId: string): {[key: string]: any};                                                                                                                                                                                                                                                                                | 新增 |
| ohos.application.formHost                 | formHost                  | function shareForm(formId: string, deviceId: string, callback: AsyncCallback\<void>): void;<br>function shareForm(formId: string, deviceId: string): Promise\<void>;                                                                                                                                                          | 新增 |
| ohos.application.formInfo                 | VisibilityType            | FORM_INVISIBLE: number                                                                                                                                                                                                                                                                                                         | 新增 |
| ohos.application.formInfo                 | VisibilityType            | FORM_VISIBLE: number,                                                                                                                                                                                                                                                                                                          | 新增 |
| ohos.application.formInfo                 | FormDimension             | Dimension_2_1                                                                                                                                                                                                                                                                                                                  | 新增 |
| ohos.application.formInfo                 | FormDimension             | Dimension_4_4                                                                                                                                                                                                                                                                                                                  | 新增 |
| ohos.application.formInfo                 | FormDimension             | Dimension_2_4                                                                                                                                                                                                                                                                                                                  | 新增 |
| ohos.application.formInfo                 | FormDimension             | Dimension_2_2                                                                                                                                                                                                                                                                                                                  | 新增 |
| ohos.application.formInfo                 | FormDimension             | Dimension_1_2 = 1                                                                                                                                                                                                                                                                                                              | 新增 |
| ohos.application.formInfo                 | FormParam                 | DEVICE_ID_KEY = "ohos.extra.param.key.device_id"                                                                                                                                                                                                                                                                               | 新增 |
| ohos.application.formInfo                 | FormParam                 | ABILITY_NAME_KEY = "ohos.extra.param.key.ability_name"                                                                                                                                                                                                                                                                         | 新增 |
| ohos.application.formInfo                 | FormParam                 | BUNDLE_NAME_KEY = "ohos.extra.param.key.bundle_name"                                                                                                                                                                                                                                                                           | 新增 |
| ohos.application.quickFixManager          | quickFixManager           | function getApplicationQuickFixInfo(bundleName: string, callback: AsyncCallback\<ApplicationQuickFixInfo>): void;<br>function getApplicationQuickFixInfo(bundleName: string): Promise\<ApplicationQuickFixInfo>;                                                                                                              | 新增 |
| ohos.application.quickFixManager          | quickFixManager           | function applyQuickFix(hapModuleQuickFixFiles: Array\<string>, callback: AsyncCallback\<void>): void;<br>function applyQuickFix(hapModuleQuickFixFiles: Array\<string>): Promise\<void>;                                                                                                                                      | 新增 |
| ohos.application.quickFixManager          | ApplicationQuickFixInfo   | readonly hapModuleQuickFixInfo: Array\<HapModuleQuickFixInfo>;                                                                                                                                                                                                                                                                 | 新增 |
| ohos.application.quickFixManager          | ApplicationQuickFixInfo   | readonly quickFixVersionName: string;                                                                                                                                                                                                                                                                                          | 新增 |
| ohos.application.quickFixManager          | ApplicationQuickFixInfo   | readonly quickFixVersionCode: number;                                                                                                                                                                                                                                                                                          | 新增 |
| ohos.application.quickFixManager          | ApplicationQuickFixInfo   | readonly bundleVersionName: string;                                                                                                                                                                                                                                                                                            | 新增 |
| ohos.application.quickFixManager          | ApplicationQuickFixInfo   | readonly bundleVersionCode: number;                                                                                                                                                                                                                                                                                            | 新增 |
| ohos.application.quickFixManager          | ApplicationQuickFixInfo   | readonly bundleName: string;                                                                                                                                                                                                                                                                                                   | 新增 |
| ohos.application.quickFixManager          | HapModuleQuickFixInfo     | readonly quickFixFilePath: string;                                                                                                                                                                                                                                                                                             | 新增 |
| ohos.application.quickFixManager          | HapModuleQuickFixInfo     | readonly originHapHash: string;                                                                                                                                                                                                                                                                                                | 新增 |
| ohos.application.quickFixManager          | HapModuleQuickFixInfo     | readonly moduleName: string;                                                                                                                                                                                                                                                                                                   | 新增 |
| ProcessData                               | ProcessData               | isKeepAlive: boolean;                                                                                                                                                                                                                                                                                                          | 新增 |
| ProcessData                               | ProcessData               | isContinuousTask: boolean;                                                                                                                                                                                                                                                                                                     | 新增 |
| ProcessData                               | ProcessData               | state: number;                                                                                                                                                                                                                                                                                                                 | 新增 |
| ServiceExtensionContext                   | ServiceExtensionContext   | startAbilityByCall(want: Want): Promise\<Caller>;                                                                                                                                                                                                                                                                              | 新增 |
| ohos.ability.wantConstant                  | Action                    | ACTION_MARKER_DOWNLOAD = "ohos.want.action.marketDownload"                                        | 删除 |
| ohos.application.AbilityLifecycleCallback  | AbilityLifecycleCallback  | onAbilityWindowStageDestroy(ability: Ability): void;                                              | 删除 |
| ohos.application.AbilityLifecycleCallback  | AbilityLifecycleCallback  | onAbilityWindowStageCreate(ability: Ability): void;                                               | 删除 |
| ohos.application.DataShareExtensionAbility | DataShareExtensionAbility | getType?(uri: string, callback: AsyncCallback\<string>): void;                                    | 删除 |
| ohos.application.DataShareExtensionAbility | DataShareExtensionAbility | openFile?(uri: string, mode: string, callback: AsyncCallback\<number>): void;                     | 删除 |
| ohos.application.DataShareExtensionAbility | DataShareExtensionAbility | getFileTypes?(uri: string, mimeTypeFilter: string, callback: AsyncCallback\<Array\<string>>): void; | 删除 |
| applicationInfo | ApplicationInfo | readonly iconId: string;           | 废弃 |
| applicationInfo | ApplicationInfo | readonly labelId: string;          | 废弃 |
| want            | Want            | entities?: Array\<string>;         | 废弃 |
| want            | Want            | parameters?: {[key: string]: any}; | 废弃 |
| want            | Want            | action?: string;                   | 废弃 |
| want            | Want            | flags?: number;                    | 废弃 |
| want            | Want            | type?: string;                     | 废弃 |
| want            | Want            | uri?: string;                      | 废弃 |
| want            | Want            | abilityName?: string;              | 废弃 |
| want            | Want            | bundleName?: string;               | 废弃 |
| want            | Want            | deviceId?: string;                 | 废弃 |