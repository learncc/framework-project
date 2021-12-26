[TOC]

# SQL

## 插入数据

1. INSERT INTO table(column...) VALUES (...)
2. INSERT INTO table(column...) SELECT语句

## 更新数据

UPDATE table SET column=xxx... WHERE语句

## 删除数据

DELETE FROM table WHERE语句

## 表

```sql
-- 创建表
-- NULL值（当不指定NOT NULL，多数DBMS认为指定的是NULL）
-- DEFAULT
CREATE TABLE tablename
(
    id VARCHAR(10) NOT NULL,
    description VARCHAR(12) NULL,
    prod_desc VARCHAR(12),
    price DECIMAL(10) DEFAULT 1
);

-- MySQL版本
CREATE TABLE tablename
(
    id INT NOT NULL AUTO_INCREMENT,
    prod_id CHAR(10) NULL,
    prod_desc CHAR(12),
    prod_price DECIMAL(10) DEFAULT 1,
    -- 支持组合主键
    PRIMARY KEY (id)
) ENGINE = InnoDB;

-- 更新表
ALTER TABLE tablename
ADD phone VARCHAR(20);
-- 以下语句并非对所有DBMS都有效
ALTER TABLE tablename
DROP COLUMN phone;

-- 删除表
DROP TABLE tablename;

-- 重命名表（MySQL、Oracle使用RENAME语句）
RENAME TABLE tablename TO tablename2;
```

## 视图

```sql
-- 创建视图
CREATE VIEW viewname AS SELECT语句;

-- 删除视图
DROP VIEW viewname;
```

## 存储过程

## 事务处理

## 游标

## 约束

1. 主键约束
2. 外键约束
3. 唯一约束
4. 检查约束

## 索引

```sql
CREATE INDEX indexname
ON tablename (cloumnname)
```

## 触发器

## 安全

1. GRANT语句
2. REVOKE语句
