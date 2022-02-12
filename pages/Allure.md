- ### 常用命令
	- pytest.main(["-svx", "--alluredir", "./allure-results", "TestCases/"]), pytest-allure包生成allure-results文件夹，包含测试的结果数据
	  id:: 62062e04-21cc-4461-874e-b8e54e94bbf8
	- allure generate  allure-results -o allure-report --clean， 根据allure-results生成allure-report
	- allure open allure-report 默认浏览器打开报告
	  id:: 62062de3-3475-484a-9c47-bf601b5727de
	- allure serve allure-results, 也是打开报告，区别与open是不需要generate这一步，直接根据results打开
- ### ps
	- report文件的打开默认是启用一个静态文件服务，所以如果需要团队之间查看的话，需要运行一个服务(nginx，anywhere等)
- pytest.main(["-svx", "--alluredir", "./allure-results", "TestCases/"])
  os.system(r"allure generate  allure-results -o allure-report --clean")
  os.system(r"allure open allure-report")
-
- ### pytest-allure定制报告
	- Epic
	- Description
	- Title
	- Feature: 标注主要功能模块
	  collapsed:: false
	- Story: 标注Features功能模块下的分支功能
		- Allure中对严重级别的定义：
			- 1、 Blocker级别：中断缺陷（客户端程序无响应，无法执行下一步操作）
			- 2、 Critical级别：临界缺陷（ 功能点缺失）
			- 3、 Normal级别：普通缺陷（数值计算错误）
			- 4、 Minor级别：次要缺陷（界面错误与UI需求不符）
			- 5、 Trivial级别：轻微缺陷（必输项无提示，或者提示不规范）
	- Severity: 标注测试用例的重要级别
	- Step: 标注测试用例的重要步骤
	- Issue和TestCase: 标注Issue、Case，可加入URL
	- Attach
-