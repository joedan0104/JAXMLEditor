# JAXMLEditor
AndroidManifest ARSC 二进制文件原始修改器。
参考项目：
https://github.com/fourbrother/AXMLEditor
在修改的过程中本人能力有限，大家可以在此基础上再修改

1>插入属性
java -jar JAXMLEditor.jar -attr -i [标签名] [标签唯一标识] [属性名] [属性值] [输入xml] [输出xml]

案例：java -jar JAXMLEditor.jar -attr -i application package debuggable true AndroidManifest.xml AndroidManifest_out.xml

application的标签中插入android:debuggable="true"属性，让程序处于可调式状态

2>删除属性
java -jar JAXMLEditor.jar -attr -r [标签名] [标签唯一标识] [属性名] [输入xml] [输出xml]

案例：java -jar JAXMLEditor.jar -attr -r application allowBackup AndroidManifest.xml AndroidManifest_out.xml

application标签中删除allowBackup属性，这样此app就可以进行沙盒数据备份

3>更改属性
java -jar JAXMLEditor.jar -attr -m [标签名] [标签唯一标识] [属性名] [属性值] [输入xml] [输出xml]

案例：java -jar JAXMLEditor.jar -attr -m application package debuggable true AndroidManifest.xml AndroidManifest_out.xml

application的标签中修改android:debuggable="true"属性，让程序处于可调式状态

4>插入标签
java -jar JAXMLEditor.jar -tag -i [需要插入标签内容的xml文件] [输入xml] [输出xml]

案例：java -jar JAXMLEditor.jar -tag -i [insert.xml] AndroidManifest.xml AndroidManifest_out.xml

因为插入标签时一个标签内容比较多，所以命令方式不方便，而是输入一个需要插入标签内容的xml文件即可。

5>删除标签
java -jar AXMLEditor.jar -tag -r [标签名] [标签唯一标识] [输入xml] [输出xml]

案例：java -jar JAXMLEditor.jar -tag -r activity cn.wjdiankong.demo.MainActivity AndroidManifest.xml AndroidManifest_out.xml

删除android:name="cn.wjdiankong.demo.MainActivity"的标签内容

6>修改标签
java -jar JAXMLEditor.jar -tag -m [标签名] [标签唯一标识] [属性名] [属性值] AndroidManifest.xml AndroidManifest_out.xml
 例如：修改渠道号
java -jar JAXMLEditor.jar -tag -m meta-data UMENG_CHANNEL value baidu AndroidManifest.xml AndroidManifest_out.xml


