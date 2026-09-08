# 机械臂系统四层架构

## 四层关系

感知(Perception) ──→ 规划(Planning) ──→ 控制(Control) ──→ 执行
↑ ↑ ↑
相机/传感器 MoveIt/OMPL PID/阻抗/MPC

## 层说明

| 层 | 输入 | 输出 | 开源库 | 计划落地 |
|----|------|------|--------|----------|
| **感知** | RGBD图像 | 物体6D位姿 | OpenCV/PyTorch | Day 20+ |
| **规划** | 目标位姿 | 关节轨迹 | MoveIt2/OMPL | Day 10+ |
| **控制** | 轨迹点 | 关节力矩 | ros2_control | Day 15+ |
| **学习** | 演示数据 | 策略网络 | LeRobot/ACT | Day 30+ |

## 仿真机器人

- UR5e（轻量仿真）
- Franka Emika Panda（复杂抓取）
- SO-101（真机，Day 36+）
EOF