# RTAssignment

package com.pack;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;

public class RTCamp {

	/**
	 * @param args
	 */
	public static void main(String[] args) {
		   //Create a new instance of Firefox Browser
		
	       WebDriver driver = new FirefoxDriver();
           String url="http://demo.rtcamp.com/rtmedia/";
	       //Open the URL in firefox browser
	       driver.get(url);
	       //Maximize the Browser window
	       driver.manage().window().maximize();

	       // Enter a valid username in the email textbox
	       
	       	WebElement username = driver.findElement(By.id("bp-login-widget-user-login"));
	       	username.clear();
	       	CharSequence [] user={"demo"};
	       	username.sendKeys(user);
	       	
	       	WebElement password = driver.findElement(By.id("bp-login-widget-user-pass"));
	       	password.clear();
	     	CharSequence [] pass={"demo"};
	     	password.sendKeys(pass);
	       	
	       	// click on the Sign in button
	        WebElement SignInButton = driver.findElement(By.id("bp-login-widget-submit"));
	  
	        SignInButton.click();
	       // close the web browser
	
	       //driver.close();
	    
	       System.out.println("Test script executed successfully.");
	      
	     
	       		// terminate the program
	      
	       //System.exit(0);
	       	
	}

} 

