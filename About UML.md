# UML

## UML 类图

UML 类图是软件工程以及设计模式中常用的类表示语言。

### 基本语法

#### 类和对象

+ 类：大驼峰黑体表示，并注明是一个类，如`Bank Account Class`表示一个`BankAccount`类
+ 单一特指对象：小写对象名并注明其类型，如`bank account: Bank Account Class`表示`BankAccount`类的一个对象
+ 泛指所有对象：在类名前加一个冒号表示指代该类所有对象，如`: Bank Account Class`表示`BankAccount`类的所有实例

#### 访问控制

+ 加号开头：公有成员
+ 减号开头：私有成员
+ 井号开头：保护成员
+ 波浪号开头：包内成员，即程序集内成员
+ 斜体装饰：抽象成员
+ 下划线装饰：静态成员

#### 成员类型

+ 第一行：类或对象名
+ 第二行：成员，或称属性/字段
+ 第三行：成员函数，或称方法

![Bank Account](.\img\uml class\bank-account.png)

### 关系

#### 泛化

表示类、接口之间的继承与实现的关系称为**泛化（Generalization）**，即 is-a 。

##### 继承

继承关系使用空心三角线表示，派生类指向基类。

![Derive](.\img\uml class\derive.png)

##### 实现

实现关系使用空心三角虚线表示。如果实现对象是一个接口，在接口的名称上方还应标注`<<interface>>`。

![Implement](.\img\uml class\implement.png)

#### 依赖

如果一个类要构造另一个类，或需要使用另一个类，则为**依赖（Dependency）**关系。使用虚线非闭合箭头表示，依赖方指向依赖。

![Dependency](.\img\uml class\dependency.png)

#### 关联

如果一个类和另一个类有关联，则为**关联（Association）**关系，如一个类知道另一个类（另一个类不一定知道这个类）。使用实线非闭合箭头表示，由类指向被关联的类。如下，人需要钱，但钱不需要人，两者是一对多关系，注释中的数字用来表示数量关系，`0..*`表示有 0 ~ n 个。

![Association](.\img\uml class\association.png)

#### 聚合

如果一个类与另一个类为 has-a 关系，即一个类包含另一个类，则为**聚合（Aggregate）**关系。空心菱形连线表示，包含者为菱形，指向被包含者。

![Aggregate](.\img\uml class\aggregate.png)

#### 组合

如果一个类和另一个类有着“强”整体关联性，并且两个类没有派生和实现关系，且不互相包含，则为**组合（Composition）**关系，两者的生命周期为一个整体，其中一个结束另一个也结束。实心菱形连线表示，由整体指向部分。

![Composition](.\img\uml class\composition.png)

## UML 对象图

UML 对象图常用于表示对象。

### 基本语法

+ 名称：上一部分所说的`bank account: Bank Account Class`称为一个具名实例，`: Bank Account Class`称为匿名实例
+ 状态：类中的属性在实例对象上称作状态，状态的值用等号连接，如`-balance:Dollars=1000`。方法是属于类的，对象只有状态
+ 链接：一个链接用于连接两个相关的对象，用直线表示

### 演示

下方演示了一个公司对象、多个部门对象、一个员工对象与匿名信息对象在 UML 中的关系表示。

![Object](.\img\uml object\object.png)

