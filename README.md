# HttpUtil
Http-post-get表单请求,在这里边我在项目里边使用的是post提交表单,
传递的方式是使用JSON字符串,引入了阿里的fastjson.jar
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>fastjson</artifactId>
    <version>1.2.15</version>
</dependency>
这里是的简单的示例:
public static void main(String[] args) {
		Map<String,String> map = new HashMap<String,String>();
		map.put("agentNum", "A2078072");
		map.put("mccCode", "BZ0000001");
		map.put("settleWay", "d0");
		map.put("cardType", "0");
		String respCode = HttpClientUtil.doPost("http://localhost:8077/test/test",JSON.toJSON(map));
		System.out.println("--响应状态码:--" +respCode);
	}
  里边还有很多方法,跟据项目里边需要用到的方式来进行传递,我这里需要的是JSON
