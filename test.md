import matplotlib.pyplot as plt
import numpy as np 

x = np.linspace(0, 3 * np.pi, 100)# linspace 第一个参数序列起始值, 第二个参数序列结束值,第三个参数为样本数默认50
y = np.sin(x)#正弦图像

plt.rcParams['font.sans-serif']=['SimHei'] #加上这一句就能在图表中显示中文
plt.rcParams['axes.unicode_minus']=False #用来正常显示负号
plt.subplot(1,2,1)#显示在第一行第一列
plt.title(r'$f(x)=sin(x)$') #图像的标题为"f(x)=sin(x)"
plt.plot(x, y)#生成以x为横坐标 y为纵坐标的图像
#plt.show()

x1 = [t*0.375*np.pi for t in x]#设定x的取值范围
y1 = np.sin(x1)#以x1为自变量的正弦函数
plt.subplot(1,2,2)#显示在第一行第二列
# plt.title(u"测试2") #注意：在前面加一个u
plt.title(r'$f(x)=sin(\omega x), \omega = \frac{3}{8} \pi$') #图像的标题为"f(x)=sin(wx) w=3/8pi 其中 \omega 表示w "
plt.plot(x, y1)#生成以x1为横坐标 y1为纵坐标的图像
plt.show()#输出图像