# SSMApplication
基于SSM框架的简单的图书管理项目

通过狂神学习，模仿其代码，手打SSM框架应用，可作为SSM框架开发模板使用

## 数据库环境
创建一个存放书籍数据的数据库表

<code>
CREATE DATABASE `ssmbuild`;
  
USE `ssmbuild`;
  
DROP TABLE IF EXISTS `books`;
  
CREATE TABLE `books` (
`bookID` INT(10) NOT NULL AUTO_INCREMENT COMMENT '书id',
`bookName` VARCHAR(100) NOT NULL COMMENT '书名',
`bookCounts` INT(11) NOT NULL COMMENT '数量',
`detail` VARCHAR(200) NOT NULL COMMENT '描述',
KEY `bookID` (`bookID`)
) ENGINE=INNODB DEFAULT CHARSET=utf8;
  
INSERT  INTO `books`(`bookID`,`bookName`,`bookCounts`,`detail`)VALUES 
(1,'Java',1,'从入门到放弃'),
(2,'MySQL',10,'从删库到跑路'),
(3,'Linux',5,'从进门到进牢');
</code>

1. 数据库配置文件；database.properties
2. Mybati配置文件；mybatis-config.xml
3. Spring整合Mybatis的相关的配置文件；spring-dao.xml
4. Spring整合service层; spring-service.xml
5. SpringMVC层；spring-mvc.xml
