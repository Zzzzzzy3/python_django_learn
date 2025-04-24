### 1. **使用 `inspectdb` 生成模型**

Django 提供了 **`inspectdb`** 命令，能自动扫描数据库结构并生成对应的模型代码。

python manage.py inspectdb [table_name] > your_app/models.py

python manage.py inspectdb --database databasename tablename1 tablename2 > 路径/models.py


---

- 替换 `[table_name]` 为你的表名（可选），如果不指定表名，会扫描所有表。
    
- 将生成的代码追加到 `your_app/models.py` 中，或新建一个模型文件。