# Appendable

Appendable接口的实现类的对象能够被添加char序列和值。如果某个类的实例打算接受取自java.util.Formatter的格式化输出，那么该类必须实现Appendable接口。

要添加的字符应该是有效的 Unicode 字符。

Appendable 对于多线程访问而言没必要是安全的。线程安全由扩展和实现此接口的类负责。

**所有已知实现类：**

BufferedWriter, CharArrayWriter, CharBuffer, FileWriter, FilterWriter, LogStream, OutputStreamWriter, PipedWriter, PrintStream, PrintWriter, StringBuffer, StringBuilder, StringWriter, Writer



