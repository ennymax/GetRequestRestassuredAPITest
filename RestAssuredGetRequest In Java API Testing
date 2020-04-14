package EnnymaxQA.EnnymaxQA;

import org.testng.annotations.Test;

import io.restassured.RestAssured;
import io.restassured.http.Method;
import io.restassured.response.Response;
import io.restassured.specification.RequestSpecification;
import junit.framework.Assert;

public class GetRequestRestassuredAPI 
{
@Test
void GetDatafromAPI()
{
//Specify API URL
RestAssured.baseURI = "http://restapi.demoqa.com/utilities/weather/city";

//Send Request to URL
RequestSpecification httprequest = RestAssured.given();

//Response From URL
Response response = httprequest.request(Method.GET, "/ondo state");

//Store Response in String
String responsebody= response.getBody().asString();
System.out.println("\n The response body is  \n\n"+responsebody+"\n\n");

//Statusline Validation
int statuscode = response.getStatusCode();
System.out.println("The Status code is  "+statuscode+"\n\n");
Assert.assertEquals(statuscode, 200);

//StatusLine validation
String statusline = response.getStatusLine();
System.out.println("The Status line is  "+statusline+"\n\n");
Assert.assertEquals(statusline, "HTTP/1.1 200 OK");

//Statusid validation
String statusid = response.getSessionId();
System.out.println("The Status ID is  "+statusid+"\n\n");

}

}
