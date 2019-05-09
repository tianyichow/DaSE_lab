## 实验一：统计字符串中单词出现次数

大数据版的“Hello World”程序就是字符统计啦。我们任务很简单，给定一个字符串列表，我们需要统计字符串列表中每种字符串出现次数。
![pic3](https://github.com/tianyichow/DaSE_lab/raw/master/setup/pic/pic3.png)

### [参考代码]

```
def wordCount(data):
    re = {}
    for i in data:
        re[i] = re.get(i, 0 ) + 1
    return re
​
if __name__ == "__main__":
    data = ["ab","cd","ab","d","d"]
    print ("The result is %s" % wordCount(data))

```

### [执行结果]

```The result is {'d': 2, 'ab': 2, 'cd': 1}```

### [疑点解释]

* get()函数：
该函数的方法语法为 dict.get(key,defult=None)，其中key是字典中要查找的键，defult为如果如果指定键的值不存在时，返回该默认值值。

* ```if __name__ == '__main__' ```又是什么呢？
当.py文件被直接运行时，```if __name__ == '__main__'```之下的代码块将被运行；当.py文件以模块形式被导入时，```if __name__ == '__main__'```之下的代码块不被运行。

