[TOC]

# SQL

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

-- 更新表
ALTER TABLE tablename
ADD phone VARCHAR(20);
-- 以下语句并非对所有DBMS都有效
ALTER TABLE tablename
DROP COLUMN phone;

-- 删除表
DROP TABLE tablename;

-- 重命名表（MySQL、Oracle使用RENAME语句）
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
