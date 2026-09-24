# Ubuntu20.04 + ROS Noetic 安装报告
仓库作者：ouyang-ros-lab
## 环境信息
系统：Ubuntu 20.04 LTS
ROS版本：ROS Noetic Ninjemys

## 安装步骤
1. 使用VMware新建虚拟机，安装Ubuntu 20.04，关闭系统自动更新弹窗。
2. 更换国内软件源，安装ROS Noetic，配置环境变量，每次新开终端执行 `source /opt/ros/noetic/setup.bash`。
3. ROS小海龟测试：
   - 终端1：`roscore`
   - 终端2：`rosrun turtlesim turtlesim_node` 启动海龟仿真窗口
   - 终端3：`rosrun turtlesim turtle_teleop_key` 开启键盘控制
4. 点击终端3窗口，使用方向键 ↑ ↓ ← → 控制海龟移动，录制演示视频。

## 遇到的问题与解决办法
1. 新开终端执行ROS命令报错：每次打开终端需要手动加载ROS环境变量 `source /opt/ros/noetic/setup.bash`。
2. 方向键无法控制海龟：必须点击运行 `turtle_teleop_key` 的终端窗口，让终端获取键盘焦点。
3. 输入rostopic命令提示消息类型错误：放弃话题自动发布，改用任务要求的键盘控制海龟。
4. 虚拟机窗口过小，界面按钮被遮挡：调整虚拟机窗口大小，用快捷键辅助操作。

## 仓库文件说明
- version.png：Ubuntu + ROS版本信息截图
- turtle_demo.mp4：键盘控制小海龟移动录屏（画面包含GitHub用户名 ouyang-ros-lab）
