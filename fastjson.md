# FastJSON实现详解

## 1、序列化

* 所谓序列化，就是将java的各种对象转化为json串。

* 所涉及到的类：

  ```
   JSONStreamAware、JSONAware、JSON、JSONSerializer、SerializerConfig、SerializerWriter、SerializerFeature（enum）、ObjectSerializer、SerializerFilter
  ```

* 图片
  ![](/assets/542381f7453e1.jpg.png)

  ### 序列化的入口

  1、通常都是用 JSON.toJSONString\(\) 这个静态方法来实现序列化。JSON是一个抽象类，实现了JSONAware（转为json串）和JSONStreamAware\(将json串写入Appendable\)

