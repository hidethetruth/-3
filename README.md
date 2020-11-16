# shiyan3
接口及异常处理

### 实验目的

1.掌握Java中抽象类和抽象方法的定义； 
2.掌握Java中接口的定义，熟练掌握接口的定义形式以及接口的实现方法
3.了解异常的使用方法，并在程序中根据输入情况做异常处理

### 实验内容

1.某学校为了给学生提供勤工俭学机会，也减轻授课教师的部分压力，准许博士研究生参与课程的助教工作。此时，该博士研究生有双重身份：学生和助教教师。
2.设计两个管理接口：学生管理接口和教师管理接口。学生接口必须包括缴纳学费、查学费的方法；教师接口包括发放薪水和查询薪水的方法。
3.设计博士研究生类，实现上述的两个接口，该博士研究生应具有姓名、性别、年龄、每学期学费、每月薪水等属性。（其他属性及方法，可自行发挥）
4.编写测试类，并实例化至少两名博士研究生，统计他们的年收入和学费。根据两者之差，算出每名博士研究生的年应纳税金额（国家最新工资纳税标准，请自行检索）。

### 实验要求
1.在博士研究生类中实现各个接口定义的抽象方法;
2.对年学费和年收入进行统计，用收入减去学费，求得纳税额；
3.国家最新纳税标准（系数），属于某一时期的特定固定值，与实例化对象没有关系，考虑如何用static  final修饰定义。
4.实例化研究生类时，可采用运行时通过main方法的参数args一次性赋值，也可采用Scanner类实现运行时交互式输入。
5.根据输入情况，要在程序中做异常处理。

### 实验过程:
1 首先

### 核心代码
```
    public static void main(String[] args) {
        try {
            System.out.println("博士研究生：");
            Doctor xm = new Doctor();
            xm.setName("胡凯莉");
            xm.setAge(20);
            xm.setNumber(2019310000);
            xm.setSex("男");
            xm.setTuition(5500);
            xm.setSalary(1800);
            System.out.println("学生姓名:" + xm.getName());
            System.out.println("学生年龄:" + xm.getAge());
            System.out.println("学生编号:" + xm.getNumber());
            System.out.println("学生性别:" + xm.getSex());
            xm.find_tuition();
            xm.find_salary();
            xm.taxation();
            System.out.println("博士研究生2：");
            Doctor xf = new Doctor();
            xf.setName("周淑怡");
            xf.setAge(22);
            xf.setNumber(2017310001);
            xf.setSex("女");
            xf.setTuition(5500);
            xf.setSalary(2000);
            System.out.println("学生姓名:" + xf.getName());
            System.out.println("学生年龄:" + xf.getAge());
            System.out.println("学生编号:" + xf.getNumber());
            System.out.println("学生性别:" + xf.getSex());
            xf.find_tuition();
            xf.find_salary();
            xf.taxation();
        } catch (Exception e) {
            System.out.println("数据异常");
        }

    }
```
### 实验结果


### 实验感想
