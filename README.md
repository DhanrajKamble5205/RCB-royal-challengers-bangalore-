

1. Write a test that validates that the team has only 4 foreign players


Public Static void main(String[] args) {

RestAssured.baseURI="";
String res_body = given().when().get().then().extract().response().asString();

JsonPath player = new JsonPath(res_body);
int count = player.getList("player.country").size();

for(int i=0;i<player;i++)
{
	String res = player.getString("player["+i+"].roal");
	
	if(player != "India")
	{
		int count = +1;
		System.out.println(count);

		Assert.assertEquals(role,"South Africa");
		Assert.assertEquals(role,"Australia");
		Assert.assertEquals(role,"Srilanka");
		Assert.assertEquals(role,"Australia");
		System.out.println(res);
	}
}
}




2. Write a test that validates that there is at least one wicket keeper


Public Static void main(String[] args) {

RestAssured.baseURI="";
String res_body = given().when().get().then().extract().response().asString();

JsonPath player = new JsonPath(res_body);
int count = player.getList("player.role").size();

for(int i=0;i<player;i++)
{
	String res = player.getString("player["+i+"].roal");
	
	Assert.assertEquals(player,"Wicket-keeper")
	System.out.println(res);
}
}
