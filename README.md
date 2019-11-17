一、实验目的
掌握字符串String及其方法的使用
掌握异常处理结构
二、实验内容
利用已学的字符串处理知识编程完成《长恨歌》古诗的整理对齐工作，写出功能函数，并运行。达到如下功能：
1.每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”
2.允许提供输入参数，统计古诗中某个字或词出现的次数
考虑操作中可能出现的异常，在程序中设计异常处理程序
三、实验步骤
1.将所要输出的文字输入，进行所需格式的输出；
2.接着统计该文字中某文字出现的次数；
3.异常处理
四、流程图
![image](https://github.com/2018310783/-/upload/master)
五、核心代码
1.将该段文字分割成数组 
		String line = new String(args[0]);	
		c  = line.length();
		char[] chs=line.toCharArray();
		System.out.println(Arrays.toString(chs));
		char[] newchs;
2.用for循环每7个字添加一个逗号，每14字添加一个句号和换行符 
		for(a=0,b=7;a<c;a+=14,b+=14)
		{	
			newchs = Arrays.copyOfRange(chs, a, b);
			for(char s:newchs)				
			    System.out.print(s);
			    System.out.print(",");
			newchs = Arrays.copyOfRange(chs, a+7, b+7);
			for(char s:newchs)
				System.out.print(s);
				System.out.print("。");
				System.out.print("\n");  
		}
3．对比字符是否相等，输出相同字符数目
		int count=0;
		String str1= s;
		while(str.indexOf(str1)!=-1)//返回指定字符在字符串中第一次出现处的索引，如果此字符串中没有这样的字符，则返回 -1。
		{			
			int d=str.indexOf(str1);
	        str=str.substring(d+str1.length());
	        count++;
	    }
		System.out.println(s+"出现的次数为"+count);
六、实验结果 
![image](https://github.com/2018310783/-/upload/master)
七、实验感想
在写代码的时候经常会出现小细节的错误，这提醒了我在以后的学习中要更加认真仔细，对每一行代码都要认真的阅读，进行检查和完善。养成这个好习惯将对我以后的学习有更多的好处。
