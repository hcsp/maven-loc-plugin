# Maven综合练习：编写一个统计代码行数的Maven插件

请编写一个能统计代码行数的Maven插件。要求如下：

- 能够统计由下列`<configuration>`所指定的文件中的代码总行数。提示，该模式称为[`Ant-style path pattern`](https://ant.apache.org/manual/dirtasks.html) 
- 在绑定到特定阶段后，该插件能够输出：

```
被统计的代码行数为X
```

你的插件需要支持的配置格式：

```
<plugin>
    <groupId>MY_PLUGIN_GROUP_ID</groupId>
    <artifactId>MY_PLUGIN_GROUP_ID</artifactId>
    <version>MY_PLUGIN_VERSION</version>
    <configuration>
        <includes>
            <include>src/**/Sample.java</include>
        </includes>
    </configuration>
    <executions>
        <execution>
            <id>loc</id>
            <goals>
                <goal>loc</goal>
            </goals>
        </execution>
    </executions>
</plugin>

```

在`pom.xml`中将该插件替换为你自己所开发的插件的groupId/artifactId/version，然后提交Pull Request。

-----
注意！我们只允许你修改以下文件，对其他文件的修改会被拒绝：

-----

- pom.xml
