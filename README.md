import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

# 创建 x 和 y 数据
x = np.linspace(-5, 5, 100)
y = np.linspace(-5, 5, 100)
x, y = np.meshgrid(x, y)

# 计算 z 数据
z = x**2 + y**2

# 创建一个三维图形对象
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

# 绘制曲面图
ax.plot_surface(x, y, z, cmap='viridis')

# 添加标题和轴标签
ax.set_title('Surface plot of z = x^2 + y^2')
ax.set_xlabel('X')
ax.set_ylabel('Y')
ax.set_zlabel('Z')

# 显示图形
plt.show()
