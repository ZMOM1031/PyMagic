.. _configure:

==========
配置
==========


当第一次使用 PyMagic 时，只要一根 Macro USB 数据线链接到电脑就够了。
当连接了 Macro USB 线后，在 Windows 中会自动安装移动磁盘驱动和虚拟串口驱动。

移动磁盘的驱动系统自带了，可以自动识别出来，而虚拟串口的驱动可以在这个移动磁盘中找到。
在 Linux 和 Mac 下，无需另外安装驱动。

移动磁盘中默认会有4个文件，它们分别是
::

   main.py	// 开机自动运行文件，可以将自己的代码放在里面
   boot.py	// 开机引到文件，由它加载main.py
   pybcdc.inf	// Windows下的虚拟串口驱动文件
   README.txt	// 简要说明


Windows
==========

1、使用 USB 连接到 PyMagic

.. image:: images/configure-01.png
    :alt: PYB v1.0 pinout

2、打开设备管理器，安装驱动

.. image:: images/configure-02.png
    :alt: PYB v1.0 pinout
    :width: 700px

.. image:: images/configure-03.png
    :alt: PYB v1.0 pinout
    :width: 700px

.. image:: images/configure-04.png
    :alt: PYB v1.0 pinout
    :width: 700px

.. image:: images/configure-05.png
    :alt: PYB v1.0 pinout
    :width: 700px

.. image:: images/configure-06.png
    :alt: PYB v1.0 pinout
    :width: 700px

.. image:: images/configure-07.png
    :alt: PYB v1.0 pinout
    :width: 700px

3、打开 `PuTTY <http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html>`_ 模拟终端，连接设备


.. image:: images/configure-08.png
    :alt: PYB v1.0 pinout
    :width: 700px

4、打开后默认看到的是 ``main.py`` 里的代码，按 `Ctrl + C` 可终止执行。

.. image:: images/configure-09.png
    :alt: PYB v1.0 pinout
    :width: 700px

5、在 ``Python Shell`` 里输入 ``help()`` 查看帮助信息。

.. image:: images/configure-10.png
    :alt: PYB v1.0 pinout
    :width: 700px

Linux
==========

1、使用 USB 连接到 PyMagic

2、打开终端并运行
::

   sudo screen /dev/ttyACM0

或者
::

   sudo picocom /dev/ttyACM0

或者
::

   sudo minicom -D /dev/ttyACM0

（注视具体情况而定，可能为 ``/dev/ttyACM*``）

Mac
==========

打开命令行输入以下命令
::

   screen /dev/tty.usbmodem*

