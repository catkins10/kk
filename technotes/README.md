JSON��һ���ı���ʽչʾ�ṹ�����ݵķ�ʽ���Ӳ�����ʱ��ʼ��������򵥺��á���ƽ̨���ر��ʺ�HTTP�����ݵĴ��䣨�������ں����е�REST�������㷺ʹ�á�

## 1��JSON��ʲô
JSON��Դ��1999���[JS���Թ淶ECMA262��һ���Ӽ�](http://javascript.crockford.com/)����15.12�½������˸�ʽ�������������2003����Ϊһ�����ݸ�ʽ[ECMA404](http://www.ecma-international.org/publications/files/ECMA-ST/ECMA-404.pdf)���܇������в��У���������
2006�꣬��Ϊ[rfc4627](http://www.ietf.org/rfc/rfc4627.txt)��������ʱ�淶���ӵ�18ҳ��ȥ��û�õĲ��֣�ʮҳ������

JSON��Ӧ�úܹ㷺�������г���100�������µ�JSON�⣺[json.org](http://www.json.org/)��

����Ŀ��Բο����[����json��һ��](https://github.com/burningtree/awesome-json)��


## 2����ȱ�㡢��׼��schema
### �ṹ������
���������򵥱�׼�淶֮һ��
- ֻ�����ֽṹ�������ڵļ�ֵ�Լ��Ͻṹ�����飬������{}��ʾ���ڲ���"key":"value"��������[]��ʾ����ֵͬ�ö��ŷֿ�
- ������ֵ��7���� false / null / true / object / array / number / string
- �ټ��Ͻṹ����Ƕ�ף���������������︴�ӵ�����
- һ����ʵ����

```javascript
   {
      "Image": {
          "Width":  800,
          "Height": 600,
          "Title":  "View from 15th Floor",
          "Thumbnail": {
              "Url":    "http://www.example.com/image/481989943",
              "Height": 125,
              "Width":  "100"
          },
          "IDs": [116, 943, 234, 38793]
        }
   }
``` 

### �ŵ�
- ���ڴ��ı������Զ��������Ķ��Ǻ��Ѻõġ�
- �淶�򵥣��������״������伴�ã��ر���JS���ECMA�ű������ڽ�֧�ֵģ�����ֱ����Ϊ����ʹ�á�
- ƽ̨�޹��ԣ���Ϊ���ͺͽṹ����ƽ̨�޹صģ����Һô�������ʵ�ֲ�ͬ���ԵĴ�����⣬������Ϊ�����ͬ�칹ϵͳ֮������ݴ����ʽЭ�飬�ر�����HTTP/REST�µ����ݸ�ʽ��

### ȱ��
ȱ��Ҳ�����ԣ�
- ����һ�㣬�ı���ʾ������һ����˵�ȶ����ƴ�ö࣬�����ݴ����Ϻͽ��������϶�Ҫ��Ӱ�����ܡ�
- ȱ��schema����ͬ���ı����ݸ�ʽ��XML�ȣ������͵��ϸ��Ժͷḻ����Ҫ��ܶࡣXML���Խ���XSD��DTD�����帴�ӵĸ�ʽ�����ɴ�����֤XML�ĵ��Ƿ���ϸ�ʽҪ��������һ���ģ����Ի���XSD�����ɾ������ԵĲ������룬����apache xmlbeans��������Щ������ϵ�һ���γ�һ���Ӵ����̬���������XML����ʵ��SOAP��WSDL��һϵ�е�ws-*�淶����������Ҳ���Կ���JSON��ȱ���淶������£�ʵ�����и���һЩ������ԣ��ر��ǽ�����REST�Ŀ��ٷ�չ���Ѿ���һЩschema��صķ�չ(����[���JSON Schema](https://spacetelescope.github.io/understanding-json-schema/index.html)��[ʹ��JSON Schema](http://usingjsonschema.com/downloads/)�� [����schema����](http://azimi.me/json-schema-view/demo/demo.html))��Ҳ��������WSDL��[WADL](https://www.w3.org/Submission/wadl/)���֡�

## ���ü����빤��
### ��ؼ����Լ���XML�Ĺ�ϵ
- ʹ��JSONʵ��RPC������XML-RPC����[JSON-RPC](http://www.jsonrpc.org/)
- ʹ��JSONʵ��path��ѯ����������XML-PATH����[JsonPATH](https://github.com/json-path/JsonPath)
- ���߲�ѯ���ߣ�[JsonPATH](http://jsonpath.com/)
 
���������ʾ��json���ñ��ʽ$.Image.IDs[:1]��ѯ���õ�116��
![image](https://raw.githubusercontent.com/kimmking/kk/master/images/json/jsonpath.png)


���ǿ���JSON��XML�����֮��ʵ������������ʽ���Կ���һ����ѧԺ�ţ�һ����ƽ���ɡ�һ�������POJOת����XML��JSON�Ĺ��̣�������һ�µģ����󲿷ֹ������Ը��ã��Ժ��л�������ϸ��������̣���10��ǰ���Լ�Ҳ����һ������XML��RPC��[http://code.google.com/p/rpcfx/](http://code.google.com/p/rpcfx/)��ò���Ѿ���ǽ��������ʵ����java��dotnet��JS��XML���л��뷴���л���ͬʱ��Ϊһ������Ʒ��ʵ����JSON���л���

����thoughtsworks��˾��Ʒ��XStream����ͬʱ����XML��JSON�����л���������Jackson�����֯������fasterxml�����Ǵ���xml�ġ���Ȼ������Ƕ�������Fastjson�⣬��΢�ĸ�Ҳ��һ�������ܵ�XML���л��⡣
ֻ��XML���Ÿ��ϸ�Ľṹ�����ḻ�Ĺ�����̬���ò�ѯ�������˵��XML����XQuery��XLST�ȹ��ߡ�����ʽ��Ҳ��DOM��ʽ��SAX��ģʽ����������Ȼ��ͬ�ļ�����

�������������ǣ�XML������[VTD-XML](http://vtd-xml.sourceforge.net/)���ֽ����DOM����̫���ڴ���SAXֻ�ܵ���ÿ���ڵ��һ�β����������ȱ��ĸ����ܴ���ʽ��

### Java���
- [Fastjson](https://github.com/alibaba/fastjson)
- [Jackson](http://wiki.fasterxml.com/JacksonHome)
- [Gson](https://github.com/google/gson)
- [Xstream](http://x-stream.github.io/)

### ����
- ��ʽ�����ߣ�[jsbeautifier](http://jsbeautifier.org/)
- chrome�����[5��Json View���](http://www.cnplugins.com/zhuanti/five-chrome-json-plugins.html)
- ����Mock: [����mock](https://www.easy-mock.com/)
- ����Mock��[SoapUI](https://www.soapui.org/rest-testing-mocking/rest-service-mocking.html)����֧�֣�SwaggerUIҲ���ԣ�[RestMock](https://github.com/andrzejchm/RESTMock)Ҳ���ԡ�

![image](https://github.com/kimmking/kk/blob/master/images/json/json01.png?raw=true)
![image](https://github.com/kimmking/kk/blob/master/images/json/json02.png?raw=true)

## Google JSON���ָ��
��ѭ�õ���������������ǰ���80%������:
- Ӣ�İ�[Google JSON Style Guide](https://google.github.io/styleguide/jsoncstyleguide.xml)��https://google.github.io/styleguide/jsoncstyleguide.xml
- ���İ�[Google JSON���ָ��](https://github.com/darcyliu/google-styleguide/blob/master/JSONStyleGuide.md)��https://github.com/darcyliu/google-styleguide/blob/master/JSONStyleGuide.md

��ժ¼���£�
- ��������ֵ������˫���ţ���Ҫ��ע��д���������棬��������Ҫ���
- ��Ҫ����ṹ����������Ƽ����ñ�ƽ����ʽ����β�Ҫ̫����
- ������ʽҪ�����壬���絥������ʾ
- �շ�ʽ��������ѭBean�淶
- ʹ�ð汾�����Ʊ����ͻ
- ����һЩ�ؼ��֣���Ҫ������key
- ���һ�������ǿ�ѡ�Ļ��߰�����ֵ��nullֵ�����Ǵ�JSON��ȥ�������ԣ��������Ĵ����к�ǿ������ԭ��
- ���л�ö������ʱ��ʹ��name������value
- ����Ҫ�ñ�׼��ʽ����
- ��ƺ�ͨ�õķ�ҳ����
- ��ƺ��쳣����

## ʹ��JSONʵ��API
[JSON API](http://jsonapi.org.cn/format/)��Google JSON���ָ���кܶ�����໥����֮����

[JSON API](http://jsonapi.org.cn/format/)�����ݽ����淶�����Զ���ͻ�����λ�ȡ���޸���Դ���Լ������������Ӧ��Ӧ����

JSON API���������С��������������Լ��ͻ�����������䴫������������ڸ�Чʵ�ֵ�ͬʱ�����������ɶ��ԡ�����ԺͿɷ����ԡ�

## REST
 todo list
 - dubbox
 - resteasy
 - restlet
 - jersey
 
![image](https://github.com/kimmking/kk/blob/master/images/json/rest.jpg?raw=true)

## SwaggerUIʵ��API�ĵ����������߲���
 todo list
 
![image](https://github.com/kimmking/kk/blob/master/images/json/json03.png?raw=true)

## ��������
JSON��ʹ�ã����ݲ�ͬ��;���м������͵ĳ�����
1. �ڲ���̨ϵͳ֮������ݴ��䣬��������»���HTTP��JSON��ʽ��ʵû�����ơ�
2. ǰ��̨֮���API���ã����͵���ǰ����ΪReact/VUE/AngularJS/ExtJS�ȿ�����ģ�ǰ���ʹ��JSON������
- ��ʱ����ʹ������Dubbox֮��Ŀ�ܣ�����ԭʼһЩSpringMVC��Controller��ֱ��@ResponseBody��@RestControllerҲ���ԡ�
- ǿ�ҽ�����Dubbox֮���rest֮���ټ�һ��Nginxת��������һЩ���ԵĿ��ƣ�����ͬԴ�Ŀ��ơ��򵥵Ļ�����ԡ���ȫ���Եȶ����Էŵ�Nginx��������Ҳ���ڶ������ʱ�ĸ��ؾ��⡣
- ����ʹ��swaggerUI���Զ�ʵ��API�ĵ������߲��ԡ����ܺ�ǿ�󣬲����򵥣����ҿ���mock�ӿڣ��ں�̨û������֮ǰ��ǰ̨�Ϳ����ȿ����ˡ�
- ����ʹ��RestUnit��SoapUI��ʵ���Զ���������ѹ�����ԡ�

3. �ṩ���������Ŀ����ӿ�API
����ͬ�ϣ����Բο�Google JSON���ָ����JSON API�½ڡ�

## json��һЩ����
�����æ����һ��Fastjson��bug���⣬�����������ʵ�Ǵ��ʹ�õĲ��淶�ԣ������������ֿӵĿ����Ծͺܴ󡣸�����ƽʱʹ�õľ��飬�Լ��ܽ��ҳ��������⣬�������£�

### 1.��ѭJava Beans�淶��JSON�淶
ʵ���������ǣ���ѭbeans�淶��JSON�淶�ķ�ʽ���ܼ��ٴ󲿷ֵ����⣬������ȷʵ��setter��getter���ñ����ͼ�annotation��ע��������͵�ƥ��ת����������fastjson��issue������ͼ��"{"a":{}}"�е�aת����List�ġ�

### 2.ʹ��������key
������Ҫʹ�����ֵ��ַ���ͷ��key������ʹ�÷���Java��class��property�����淶��key����������ٲ���Ҫ�ĳ�ͻ����jsonpath��js�a.1���ܻᱻ���ͳ�a[1]��a["1"]����Щ�����������Ҫ���鷳��

### 3.�������ڴ���
��һ��ǰ���Google JSON���ָ����Ҳ�ᵽ�ˣ�����ʹ�ñ�׼�����ڸ�ʽ���������л��ͷ����л��ﶼ����ͬ����datePattern��ʽ��

### 4.�����Զ������л��뷴���л�
����������˵���Զ������л���һ�����ĸ�Դ��

������Ҫʹ���Զ������л��������򲻵��ѣ����ȿ���ʹ��ע����ˣ������ȷ�ʽ�����������½�һ��VO������װʵ����Ҫ�����ԡ�ʹ���Զ������л�ʱһ��ҪС�ģ���Ϊ�����ᵼ���������⣺
- �ı���pojo <-> jsonstring ����Ȼ��Ӧ��ϵ���Ӷ��������Ķ�������Ų����⣬��ı�Ĺ�ϵ�޷��򵥵Ĵ�bean��json�Ͽ������ˣ�
- �����л����ܳ�����Ϊ��Ӧ����ԭ���������ˡ�

���ֻ�����л�����ȥ����Ӧ������JSON���ݡ������������󣩵����ݸ�ʽ��JSON�޹ػ����Ǳ�׼�ģ���ʱ�Զ������л�������ν�ˣ�������Ҫ���շ�������

### 5.JsonObject��ʹ��
JsonObject��JSON�ַ�����pojo����ת�������е��м������ͣ��м���󣬲�Ҫ���ã�������Ҫ��

### 6.Hibernate�������
�������뼶�������ܵ��³������⣬����hibernate�������װһ��VO���������л���ʹ��VO�໹��һ���ô������ǿ���ȥ��һЩû�õ����ԣ�������������ͬʱ���Լ��϶�������ԡ�

### 7.���Ƕ���뷺������
������Ҫ��ʹ�ù���Ĳ��Ƕ�׵�ͬʱʹ�÷��ͣ�List��Map�ȣ������ܵ������Ͷ�ʧ����������Ƚ��Ѳ顣

### 8.��������������������
������Ҫ��ͬһ��Bean�Ĳ�νṹ��ʹ�ö�������Ͷ��󣬿��ܵ������Ͷ�ʧ����������Ƚ��Ѳ顣��Ȼ���ǿ���ͨ��������ʾ�Ĵ��ݸ�����ȷ�����ͣ����������������˸���Ĳ�ȷ���ԡ����õ�����Ӧ����һ��ʼ���ʱ�ͱ��������Щ���⡣

### 9.����ѭ������
��������ѭ�����ã������Ȼ����ͨ�����л����Խ�������������ܱ�������⡣

## fastjson�����ʵ��
### 1.���л�һ�������JSON�ַ���

### 2.�����л�һ��JSON�ַ�����Java����

### 3.���ڴ���

### 4.�Զ������л��뷴���л�

### 5.�������л����Ե�ʹ��

### 6.Annotationע���ʹ��

### 7.��Spring MVC�����ʹ��

### 8.��Spring Boot�ļ���ʹ��

## fastjson�����˵��
todo list

