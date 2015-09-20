# LightweightUITableView
![]()
LightweightUITalbeView项目是一个简化UITableView开发的轻量级类库，使用它你可以不用再编写繁杂的数据源和代理方法，可以不用再手动维护可变高度的Cell行高。
## 目录
LightweightUITalbeView      包含整个轻量级UITableview所需要的内容，可以直接copy到项目中使用；
LightweightUITalbeViewDemo  用于演示LightweightUITalbeView库的使用；
##说明
* KCTableViewArrayDataSource和KCTableViewDelegate用于给UIViewController中的UITableView的dataSource和delegate瘦身，也是LightweightUITalbeView的核心，二者将数据源和代理方法从控制器中解放出来，并提供了一些便捷方法用于快速配置数据；
* UITableView+KC 用于实现自动行高扩展处理，理论上来说和KCTableViewArrayDataSource、KCTableViewDelegate可以分开使用，但是为了设置更加方便建议配合使用；
* KCTableViewArrayDataSourceWithCommitEditingStyle用于处理可编辑Cell，KCTableViewArrayDataSource会根据属性设置动态调用，外界无需直接调用；
* UITableViewCell+KC是对于UITableViewCell的扩展，仅用于辅助操作；
* KCTableViewCell是对UITableViewCell的简单封装，方便配置Cell背景和设置间距，一般用于frame控制行高的情况，和当前库没有直接联系，仅用于辅助；
* KCTableViewController是对于KCTableViewArrayDataSource、KCTableViewDelegate、UITableView+KC使用的简单控制器封装，用于辅助开发者快速创建使用LightweightUITalbeView的表格控制器；
* UIView+KC是对UIView属性的简单扩展，和当前库没有直接联系，仅用于辅助；

总之，KCTableViewArrayDataSource、KCTableViewDelegate、UITableView+KC三个类是给UITableView瘦身的核心，理论上其他辅助类如果不需要均可以去掉（需要开发者简单修改使用的辅助方法，但是可行）。
##示例
##效果