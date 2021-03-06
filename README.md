## 码匠社区

## 资料

[Spring Guides](http://spring.io/guides)

[Spring Web](https://spring.io/guides/gs/serving-web-content/)

[elasticsearch社区](https://elasticsearch.cn/explore)

[GitHub开发者平台](https://developer.github.com/v3/guides/managing-deploy-keys/#deploy-keys)

[BootStrap](https://v3.bootcss.com/getting-started/)

[GitHub OAuth](https://developer.github.com/apps/building-oauth-apps/creating-an-oauth-app/)

[Spring文档](https://sping.io/docs)

[Mybatis generator](http://mybatis.github.io/generator/)

## 工具

[git](https://git-scm.com/download)

[Visual Paradigm画图工具](https://www.visual-paradigm.com)

[Flyway](https://flyway.org/getstarted)

[PageHelper](https://pagehelper.github.io/docs/)

## 脚本

```sql
CREATE TABLE `user` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `ACCOUNT_ID` varchar(100) DEFAULT NULL,
  `NAME` varchar(50) DEFAULT NULL,
  `TOKEN` char(36) DEFAULT NULL,
  `GMT_CREATE` bigint(20) DEFAULT NULL,
  `GMT_MODIFIED` bigint(20) DEFAULT NULL,
  `bio` varchar(256) DEFAULT NULL,
  `avatar_url` varchar(100) DEFAULT NULL,
  PRIMARY KEY (`ID`)
) ENGINE=InnoDb DEFAULT CHARSET=utf8
```

```sql
CREATE TABLE `question` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `title` varchar(50) DEFAULT NULL,
  `description` text,
  `GMT_CREATE` bigint(20) DEFAULT NULL,
  `GMT_MODIFIED` bigint(20) DEFAULT NULL,
  `creator` int(11) DEFAULT NULL,
  `comment_count` int(11) DEFAULT '0',
  `view_count` int(11) DEFAULT '0',
  `like_count` int(11) DEFAULT '0',
  `tag` varchar(256) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8
```

```
    mvn flyway:migrate
    mvn -Dmybatis.generator.overwrite=true mybatis-generator:generate
```