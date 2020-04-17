1,ListAppActivity.java    //本机的App展示
2,InstallerActivity.java   //安装app到虚拟机
3,NewHomeActivity extends NexusLauncherActivity  //主要的界面，Android系统的launcher改装的
            其中 startVirtualActivity() 方法是拉起安装在虚拟机应用的方法
4,LoadingActivity.java //拉起虚拟机应用后进入的activity
5,VActivityManager.java //负责各种接口，远程调用
6,VActivityManagerService //远程接口实现 ，接口是IActivityManager

7,所有方法经过此处MethodInvocationStub  launcher3 Launcher activity

                if ("getPhoneId".equals(method.getName())) {
                    Log.d("xsp", method.getName() + " value=" + String.valueOf(res));
                    res = -19309;
                }
8, VirtualCore是主要入口