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

  1、通常都是用 JSON.toJSONString\(\) 这个静态方法来实现序列化。JSON是一个抽象类，实现了JSONAware（转为json串）和JSONStreamAware\(将json串写入Appendable\)的接口，同时又是JSONArray（内部实现是list）和JSONMap（内部是map）的父类。该入口的内部实现基本相同，只是内部的某些特定配置和对外暴露的接口不同。该方法的内部实现实际上是托付给了JSONSerializer



