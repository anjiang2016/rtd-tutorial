使用办法
===========

.. _installation:

安装
----

To use ziku, first install it using pip:

.. code-block:: console

    (.venv) pip install ziku

使用
----

使用函数 :py:func: ``ziku.write`` 来将 ``"汉字"`` 写入img中.

.. code-block:: console

    import ziku
    import cv2
    ziku.size(0.4)
    img=cv2.imread("src/ziku/earthmap.png")
    img=ziku.write(img,"太阳当空照...",x=100,y=100)

    ziku.size(0.6)
    img=ziku.write(img,"花儿对我笑",x=100,y=200)
    cv2.imwrite("ziku.png",img)

    ziku.size(0.8)
    img=ziku.write(img,"小鸟说 早早早",x=100,y=300)
    cv2.imwrite("ziku.png",img)

    ziku.size(1)
    img=ziku.write(img,"你为什么背上大书包",x=100,y=400)
    cv2.imwrite("ziku.png",img)

使用函数 :py:func:``ziku.ZIKU.test`` 来将运行 ``测试`` 代码.测试代码的内容为：

.. code-block:: console

    def test(self):
        """ 测试用的函数，运行后，把一些汉字写入例子图片上，然后保存到当前目录下的Ziku.png中"""
        current_dir=os.path.dirname(__file__)#当前文件所在目录
        print(current_dir)
        self.size=0.5
        img = np.zeros((300,300,3))
        img = cv2.imread(os.path.join(current_dir,"earthmap.png"))
        
        #img[0:hzi,0:wzi][select_index]=zi.copy()[select_index]
        self.write2Img(img,'老师明明可以靠颜值-汉字字库',pos=np.array([50,50]))
        self.write2Img(img,'字库的使用办法:',pos=np.array([110,50]))
        self.write2Img(img,'import-ZIKU',pos=np.array([170,50]))
        self.write2Img(img,'ziku=ZIKU("./ZIKU")',pos=np.array([230,50]))
        self.write2Img(img,'ziku.write2Image(img,"你要写的字")',pos=np.array([300,50]))
        self.write2Img(img,'试着打印一组符号:  @@@@`-=[]\;\',./`\\',pos=np.array([370,50]))
        cv2.imwrite("ZiKu.png",img)
        print("save to ./ZiKu.png")

