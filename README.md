# 操作步骤



首先创建一个新终端：

- 先看一下有没有终端存在：

  - ```bash
    screen -ls
    ```

    应该是下面这样的（现在是没有终端的，mc那个是我的服务器，请不要动233）：

    ```bash
    root@instance-of05m7kn:~# screen -ls
    There are screens on:
            2594.mc (11/09/2018 05:21:24 PM)        (Detached)
    1 Sockets in /var/run/screen/S-root.
    ```


- 接下来新建终端：

  - ```bash
    screen -S server
    ```

    此时会跳进一个新的终端界面，所有的操作就在这里进行；

- **当操作完毕后，按`ctrl + A + D`退出此终端。**

- 此时再使用`screen -ls`查看一下终端列表：


  - ```bash
    root@instance-of05m7kn:~# screen -ls
    There are screens on:
            21361.server    (11/10/2018 03:25:44 PM)        (Detached)
            2594.mc (11/09/2018 05:21:24 PM)        (Detached)
    2 Sockets in /var/run/screen/S-root.
    ```

    可以看到现在有一个叫server的终端存在。理论上现在你打开的时候就是这样的，终端我创好了。

- 此时想要进入已经存在的server终端，应输入如下指令：


  - ```bash
    screen -r server
    ```

以上就是终端的操作，应该你是只需要用到`screen -r server`就可以了