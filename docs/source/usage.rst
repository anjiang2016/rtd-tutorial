使用办法
=======

.. _installation:

安装
----

To use ziku, first install it using pip:

.. code-block:: console

    (.venv) pip install ziku

使用
----

使用函数``ziku.write(img,"汉字",x=100,y=100)``来将``"汉字"``写入img中   


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

