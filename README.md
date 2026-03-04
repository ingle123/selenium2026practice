# selenium2026practice
selenium2026practice
package testnguse;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.annotations.AfterMethod;
import org.testng.annotations.BeforeMethod;
import org.testng.annotations.BeforeSuite;
import org.testng.annotations.Test;

// This is actual test ng use case
public class ActualTestNgUse {
	
		public static WebDriver driver = new ChromeDriver();
		@BeforeMethod
		public void beforeclass() {
			WebDriver driver = new ChromeDriver();
			driver.get("https://www.facebook.com");
			driver.manage().window().maximize();
			
		}
		@Test(priority=2)
		public void test() throws InterruptedException {
			driver.findElement(By.name("email")).sendKeys("Nilesh");
			driver.findElement(By.name("pass")).sendKeys("123456");

					
			
			
		}
		@Test(groups= {"Sanity"})
		public void test2() throws InterruptedException {
			driver.findElement(By.name("email")).sendKeys("Nilesh");
			driver.findElement(By.name("pass")).sendKeys("654321");
			
		}
	   @AfterMethod
	   public void close() {
		   driver.close();
	   }
	   @BeforeSuite
	   public void suite() {
		   System.out.println("My suite code");
		   
	   }

	}
	
	

