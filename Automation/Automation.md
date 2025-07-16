x## Backend Technology => Java, .Net, Python, Nodejs, PHP, Ruby, Go
## Frontend => Reactjs, Angular, Vuejs
setup eclipse:
1. click =file = java projects===project name ( demo test ) also set JRE (current version )==>finish
2.  DEMOTest ==> write click on project property  (demotest)==>click on java bulid path ==> after that click on library


## Write First Test Case ##

package MyPackage;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class FirstTestCase {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		 //lunch chrome browser
		
		 System.setProperty("webdriver.chrome.driver","E:\\automation\\chromedriver-win64\\chromedriver-win64\\chromedriver.exe");

		WebDriver driver = new ChromeDriver();
		
		driver.navigate().to("https://www.google.com//");
		
		// capturee url of the web page
		
		String title =  driver.getTitle();
		
		System.out.println(" Page Title :" : + title);
		
		//Capture url of the  webpage 

		System.out.println("URL: "+ driver.getCurrentUrl());
		
	}
 }
	
## Locators ##

1 .Identify web elements 

##locators 2 types##

1. Basci locating streategies
2. Customized locating strategies

## Basci locating streategies ##
1. BY Id
2. BY Name
3. By Link text
4. By partial link text


## Customized locating Streategies##
1. By CSS
2. Xpath
















