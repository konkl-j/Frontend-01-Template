# 每周总结可以写在这里

# 每周总结可以写在这里

### 语言分类
* 形式语言
    - 中文/英文
* 形式语言（乔姆斯基谱系）
    - 0型 无限制文法
    - 1型 上下文相关文法  
    - 2型 上下文无关文法  
    - 3型 正则文法  
### 产生式(BNF)
* 用尖括号括起来的名称来表示语法结构名
* 语法结构分成基础结构和需要用其他语法结构定义的符合结构
    - 基础结构称终结符
    - 符合结构称非终结符
* 引号和中间的字符表示终结符
* 可以有括号
* \* 表示重复多次
* | 表示或
* \+ 表示至少一次
```
"a"
"b"
<program>:= ("a" + |  "b" + )+
<program>:= <program> "a" + | <program> "b"+

<Number> = "0" | "1" | "2" | .... | "9"
<DecimalNumber> = "0" | (( "1" | "2".... | "9") <Number>*)
<AdditiveExpression> = <DecimalNumber> |
 <AdditiveExpression>  "+" <DecimalNumber>


<MutiplicativeExpression> = <DecimalNumber> | <MutiplicativeExpression>  "+" <DecimalNumber>
<logicExpression> = <AdditiveExpression> | 
<logicExpression>  "||" <AdditiveExpression> |
<logicExpression>  "&&" <AdditiveExpression>
1 + 2 * 3 

```
### 图灵完备性
- 命令式 图灵机
    * goto
    * if 和 while
- 申明式 lambda
    * 递归

### 动态于静态

- 动态：
    * 在用户的设备/在线服务器上
    * 产品实际运行时
    * Runtime
- 静态
    * 在程序员的设备上
    * 产品开发时
    * CompileTime

### 类型系统
- 动态类型系统与静态类型系统
- 强类型与弱类型（有无隐式转换）
    * string + number
    * string == Boolean
- 复合类型
    * 结构体
    * 函数签名
- 子类型
    * 逆变/协变    

### 一般的命令式编程语言
```
Atom
Expression 
statement
structure
program
```


### unicode
ASCII 
使用 “\u” 转义

### 词法分析
- InputElement
    - whitespace // 空格
        - tab
        - vt
        - ff
        - sp
        - nbsp // no-break space
        - zwnbsp // zero width no-break space \ufeff 零宽空格 bit order mask
    - lineTerminator  // 换行
        - lf // line feed \n
        - cr // carriage return 回车 \r
        - ls // line separator   
        - ps // paragraph separator
    - comment         // 注释
    - token           // 一切有效的东西
        - punctuator // 符合        
        - identifierName // 标识符
            - keywords // 关键字
            - identifier // 不能以数字开头
            - future reserved keywords enum
        - literal // 直接量
            - Number
                - IEEE 754 
                    - Sign (1)
                    - Exponent (11)
                    - Fraction ()
                - 12.3e10 (科学计数法，e后为位数)
                - 写一个正则 匹配所有的number直接量    
                - 安全整数范围 1fffffffff(16) 
                - Math.abs(0.1 + 0.2 - 0.3) <= Number.EPSILON
            - String
                - character
                    - ASCII
                    - Unicode
                    - UCS
                    - GB
                        - GB2312
                        - GBK
                        - GB18030
                    - ISO-8859
                    - BIG5    
              - Encoding
                - UTF
                    - UTF-8  8
                    - UTF-16 
                    - 写一个utf-8 encoding 
              - Grammar
                - "abc"
                - 'abc'
                - \`abc\` 模板字符串
                         
            - Boolean
            

