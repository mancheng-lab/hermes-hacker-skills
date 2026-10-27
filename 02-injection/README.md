# 注入类（`02-injection`）

_SQLi / XSS / 命令注入 / SSTI / XXE / NoSQL / 原型链污染 / EL / JNDI / CRLF_

## sqli-sql-injection  `P0`

SQL 注入。当输入进入 SQL 查询、认证逻辑、排序、过滤、报表，或存在数据库特有的布尔/时间盲注与带外执行路径时使用。

## xss-cross-site-scripting  `P0`

跨站脚本 XSS。当用户可控内容进入 HTML、属性、JavaScript、DOM 汇聚点、上传文件或多上下文渲染路径时使用。

## cmdi-command-injection  `P0`

命令注入。当用户输入可能进入 shell 命令、进程执行、格式转换器、导入流水线或盲式带外命令汇聚点时使用。

## ssti-server-side-template-injection  `P0`

服务端模板注入 SSTI。当模板表达式、服务端渲染、预览功能或模板引擎可能执行攻击者可控内容时使用。

## xxe-xml-external-entity  `P0`

XXE XML 外部实体注入。当 XML、SVG、OOXML、SOAP 或解析器驱动的导入流程可能解析外部实体、文件或内网资源时使用。

## nosql-injection  `P0`

NoSQL 注入。当存在 MongoDB 风格操作符、JSON 查询对象、灵活搜索过滤器或后端查询 DSL 时，可能造成数据或逻辑滥用时使用。

## expression-language-injection  `P1`

表达式语言注入（Java EL、SpEL、OGNL、MVEL）。当 Spring、Struts2、Confluence 等框架可能求值攻击者可控表达式时使用。

## jndi-injection  `P1`

JNDI 注入。当 Java 应用使用攻击者可控的名字执行 JNDI 查找时——尤其是经由 Log4j2、Spring 或任何可达 InitialContext.lookup() 的代码路径。

## prototype-pollution  `P0`

JavaScript 原型链污染（基础 + 进阶 RCE 合订本）。当用户输入被合并进对象（query 解析器、JSON body、deep assign）、用不可信键配置库、或需要在 Node/浏览器中挖掘 RCE gadget 时使用。进阶部分覆盖服务端 RCE、客户端 gadget、过滤器绕过与检测手法。

## crlf-injection  `P1`

CRLF 注入。当用户输入进入 HTTP 响应头、Location 跳转、Set-Cookie 值或日志文件，可用回车换行切分或注入内容时使用。
