# Shell01

这个 **Shell 01 Piscine 项目** 是 **Shell 00** 的进阶训练，旨在通过更复杂的 Shell 脚本任务，深化你的 **系统管理能力** 和 **脚本编程逻辑**，同时培养对 **数据转换** 和 **自动化流程** 的掌控力。以下是核心学习目标解析：

---

### **技术能力跃迁**
1. **高级文本处理**
- 多级管道操作（如 `cat /etc/passwd` → 过滤注释 → 反转用户名 → 按规则排序，练习07 `r_dwssap.sh`）
- 正则表达式高级应用（如匹配 `.sh` 文件并去除扩展名，练习02 `find_sh.sh`）
- 结构化输出格式化（逗号分隔、行尾符号控制，练习01 `print_groups.sh`）

2. **系统信息提取与处理**
- 用户组信息解析（`id` 命令结合环境变量 `FT_USER`，练习01）
- MAC 地址捕获（`ifconfig` 输出处理，练习04 `MAC.sh`）
- 文件系统深度统计（递归计数文件/目录，练习03 `count_files.sh`）

3. **数据转换与计算**
- 自定义进制转换（将 `'\"?!` 和 `mrdoc` 编码的数字转换为 `gtaio luSnemf` 进制，练习08 `add_chelou.sh`）
- 跨进制运算（如将符号组合转换为数值进行加法，再编码输出）

4. **极端场景操作**
- 创建特殊符号命名的文件（练习05：`\?$*'MaRViN'*$?\"`）
- 输出行间隔控制（`ls -l` 隔行显示，练习06 `skip.sh`）

---

### **思维模式升级**
1. **逻辑链拆解**
- 复杂需求的步骤分解（如练习07需按顺序执行：过滤 → 隔行 → 反转 → 排序 → 截取 → 格式化）
- 逆向工程思维（如练习08需从示例反推进制映射规则）

2. **精确性到原子级**
- 输出格式的严格匹配（如练习01要求逗号分隔无空格）
- 环境变量动态处理（依赖 `FT_USER`、`FT_LINE1` 等外部输入）
- 边缘情况预判（如处理含空格或特殊符号的文件名）

3. **数学抽象能力**
- 自定义进制设计（练习08中符号与数值的映射关系）
- 跨进制运算的实现（需先转十进制计算，再转目标进制）

---

### **工程实战训练**
1. **防御式编程**
- 处理不可控输入（如 `FT_NBR1` 含特殊符号）
- 防止命令注入（谨慎处理变量展开）

2. **系统工具深度整合**
- `id`、`ifconfig`、`find` 等命令的进阶参数使用
- 结合 `awk`、`sed`、`cut` 进行文本手术

3. **版本控制纪律**
- 复杂脚本的 Git 提交规范（确保脚本可复现）
- 适应自动化评估工具（Moulinette 对输出格式的机械式检查）

---

### **隐藏文化密码**
1. **压力管理隐喻**
- 文档中插入的 **水獭百科**（Lutra lutra）暗喻开发者需要像水獭一样：  
	**灵活**（适应不同进制/格式）
	**细致**（如梳理毛发般处理文本）
	**领地意识**（严格守护脚本的精确性）

2. **幽默抗压训练**
- 练习08的示例输出包含 `Segmentation fault`（段错误），暗示即使任务看似荒诞（如用符号做进制计算），仍需保持冷静。

3. **协作与独立平衡**
- 反复强调“问左边/右边的同伴”，但最终依赖自身对 `man` 和文档的理解（“RTFM”精神）。

---

### **通关策略**
1. **分步验证法**
- 对复杂任务（如练习07-08），用 `echo` 逐步打印中间结果，确保每步输出符合预期。

2. **进制转换工具化**
- 为练习08设计进制转换表：

```bash
	# ' \"?! → 0-4
	# mrdoc → 0-4
	# gtaio luSnemf → 0-12
```

3. **特殊符号转义特训**
- 用 `printf` 或 `echo -e` 处理包含引号、反斜杠的文件名（练习05）。

4. **环境变量沙盒测试**
- 使用 `export FT_USER=test` 模拟不同场景，避免依赖宿主机配置。

---

这个项目将把你从“Shell 基础操作者”进化为“系统级脚本巫师”。当你能让 `add_chelou.sh` 优雅地输出 `Salut` 而非 `SSegmentation fault` 时，说明已掌握 Shell 的混沌与秩序共舞之道！
