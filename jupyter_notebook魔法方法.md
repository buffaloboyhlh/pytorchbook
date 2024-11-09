在 Jupyter Notebook 中，“魔法方法”（Magic Methods）是一些特定的命令，可以在单元格中执行，通常以 `%` 或 `%%` 开头。这些魔法方法提供了丰富的功能，帮助用户更高效地使用 Jupyter Notebook。魔法方法并不是 Python 本身的一部分，而是 Jupyter Notebook 提供的扩展功能。

### 一、行魔法命令（Line Magics）

行魔法方法以单个百分号 (`%`) 开头，作用于当前行的代码。

1. **`%run`**
   - 用于运行一个 Python 脚本。
   ```python
   %run script.py
   ```

2. **`%time`**
   - 用于测量一行代码的执行时间。
   ```python
   %time some_function()
   ```

3. **`%timeit`**
   - 自动多次运行一行代码，并提供平均执行时间，适合用于性能优化。
   ```python
   %timeit some_function()
   ```

4. **`%ls`**
   - 列出当前目录的文件和文件夹。
   ```python
   %ls
   ```

5. **`%cd`**
   - 切换当前工作目录。
   ```python
   %cd /path/to/directory
   ```

6. **`%pwd`**
   - 显示当前工作目录的路径。
   ```python
   %pwd
   ```

7. **`%matplotlib inline`**
   - 用于在 Jupyter Notebook 中嵌入 Matplotlib 图形（这使得绘图结果直接显示在 Notebook 中，而不弹出窗口）。
   ```python
   %matplotlib inline
   ```

8. **`%load`**
   - 加载一个外部 Python 文件并显示其内容。
   ```python
   %load script.py
   ```

9. **`%who`**
   - 显示当前命名空间中定义的所有变量。
   ```python
   %who
   ```

10. **`%history`**
    - 显示代码历史，可以指定查看最近的代码或某个范围内的代码。
    ```python
    %history
    ```

### 二、cell 魔法命令（Cell Magics）

单元格魔法命令以 `%%` 开头，作用于整个单元格。

1. **`%%time`**
   - 测量整个单元格的执行时间。
   ```python
   %%time
   # 执行多行代码
   some_function()
   another_function()
   ```

2. **`%%timeit`**
   - 测量整个单元格代码的执行时间，自动进行多次测试。
   ```python
   %%timeit
   some_function()
   another_function()
   ```

3. **`%%writefile`**
   - 将单元格中的内容写入文件。
   ```python
   %%writefile my_script.py
   # 这段代码会被写入 my_script.py 文件
   def my_function():
       pass
   ```

4. **`%%capture`**
   - 捕获代码单元中的输出（标准输出和标准错误），防止它显示在 Notebook 中。
   ```python
   %%capture captured_output
   print("Hello, World!")
   ```

5. **`%%bash`**
   - 在单元格中运行 Bash 命令。
   ```python
   %%bash
   echo "Hello from Bash"
   ```

6. **`%%perl` / `%%ruby` / `%%javascript`**
   - 允许在单元格中执行 Perl、Ruby 或 JavaScript 代码。
   ```python
   %%perl
   print "Hello, Perl!"
   ```

7. **`%%file`**
   - 在指定文件中写入代码，可以指定文件的路径和名称。
   ```python
   %%file my_script.py
   # Python code goes here
   def my_function():
       pass
   ```

### 三、其他常用魔法命令

1. **`%env`**
   - 查看和设置环境变量。
   ```python
   %env
   %env MY_VAR=value
   ```

2. **`%load_ext`**
   - 加载 Jupyter Notebook 扩展。
   ```python
   %load_ext autoreload
   ```

3. **`%unload_ext`**
   - 卸载一个扩展。
   ```python
   %unload_ext autoreload
   ```

4. **`%store`**
   - 在 Notebook 会话之间存储变量。
   ```python
   %store my_variable
   ```

5. **`%bookmark`**
   - 设置或查看书签。
   ```python
   %bookmark my_bookmark /path/to/directory
   ```

6. **`%debug`**
   - 启动调试器，通常用来在错误发生时进行交互式调试。
   ```python
   %debug
   ```

### 四、扩展魔法方法

Jupyter 支持第三方扩展，用户可以使用一些额外的魔法方法来扩展功能，例如通过安装 `ipython-sql` 扩展，可以使用 `%sql` 来执行 SQL 查询，或者通过 `line_profiler` 和 `memory_profiler` 等扩展来进行性能和内存分析。

### 五、如何查看所有魔法命令

你可以使用 `%lsmagic` 来列出当前支持的所有魔法命令：

```python
%lsmagic
```

### 六、结论

Jupyter Notebook 提供了丰富的魔法方法来增强开发体验，简化代码执行和调试过程。你可以通过这些命令快速执行系统任务、调试代码、性能分析等。