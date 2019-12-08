实验目的
分析学生选课系统
使用GUI窗体及其组件设计窗体界面
完成学生选课过程业务逻辑编程
基于文件保存并读取数据
处理异常
实验要求
一、系统角色分析及类设计
例如：学校有“人员”，分为“教师”和“学生”，教师教授“课程”，学生选择课程。
定义每种角色人员的属性，及其操作方法。
属性示例： 人员（编号、姓名、性别……）
教师（编号、姓名、性别、所授课程、……）
   学生（编号、姓名、性别、所选课程、……）
   课程（编号、课程名称、上课地点、时间、授课教师、……）
以上属性仅为示例，同学们可以自行扩展。

二、要求:
1、 设计GUI窗体，支持学生注册、课程新加、学生选课、学生退课、打印学生选课列表等操作。
2、 基于事件模型对业务逻辑编程，实现在界面上支持上述操作。
3、 针对操作过程中可能会出现的各种异常，做异常处理
4、 基于输入/输出编程，支持学生、课程、教师等数据的读写操作。
5、 基于Github.com提交实验，包括实验SRC源文件夹程序、README.MD实验报告文档。。


核心代码
mainJFrame=new JFrame("用户注册");
	con=mainJFrame.getContentPane();
	con.setLayout(new FlowLayout());
	
	labTitle=new JLabel("<html><body><h1>用户注册     </h1> </body>  </html> ");
	con.add(labTitle);
	con.add(Box.createHorizontalStrut(20000));
	
	labName=new JLabel("用户名:");
	txtName=new JTextField();
	txtName.setColumns(20);
	con.add(labName);
	con.add(txtName);
	con.add(Box.createHorizontalStrut(20000));
上述代码表示的是用户注册时用到的文本窗口方法，其他的窗口和用户名窗口同理，
	labSex=new JLabel("性别:");
	mRadio=new JRadioButton("男",true);
	mRadio.addActionListener(this);
	fRadio=new JRadioButton("女",false);
上述代码表示的是用户注册时用到的单选窗口方法，
labClass=new JLabel("所属班级:");
	Jcombobox1=new JComboBox<Object>(msg1);
	con.add(labClass);
	con.add(Jcombobox1);
	con.add(Box.createHorizontalStrut(30000));
上述代码表示的是用户注册时用到的下拉窗口方法
regBtn=new JButton("注册");
	regBtn.addActionListener(this); 
	con.add(regBtn);
上述代码是按钮的方法。
     super("课程信息管理系统");
      学号=new JTextField(10);//创建文本信息的的对象
      姓名=new JTextField(10);
      电话号码=new JTextField(15);
      年龄=new JTextField(5);
      所选课程=new JTextField(15);
      身份证号码=new JTextField(18);
      加课=new JButton("增加课程信息");
      删课=new JButton("删除课程信息");
      选课=new JButton("学生选课");
      退课=new JButton("学生退课");
      查询=new JButton("全部课程");
上述是主界面用到的按钮及内容，
//修改课程信息
	public void update(Teacher_information tea) {
		int flag=find(tea.getteaID());    
		arry.set(flag, tea);
上述是修改课程的方法
public boolean delete(String s)
	{  
		int pos=find(s);
		if (pos==-1)
			return false;
		
		arry.remove(pos);    
		return true;
	}上述是退课方法。
编程感想
学会了GUI的使用方法，复习了对窗口的使用，先学会了基于事件模型对业务逻辑编程，复习了异常处理的使用，学会了有一定思路的连续编程。
