package org.automationexam;

import java.io.File;
import java.io.IOException;

import org.openqa.selenium.By;
import org.openqa.selenium.OutputType;
import org.openqa.selenium.TakesScreenshot;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;


import com.google.common.io.Files;

public class ChromeSafaryFirefox {

	public static void main(String[] args) throws IOException {
	//chrome driver launch	
     
		WebDriver driver=new ChromeDriver();
      
       
		
		
      driver.manage().window().maximize();
      driver.get("https://www.getcalley.com/page-sitemap.xml");
      
      File f=((TakesScreenshot)driver).getScreenshotAs(OutputType.FILE);
     
      driver.findElement(By.xpath("//*[@id=\"sitemap\"]/tbody/tr[1]/td[1]/a")).click();
      Files.copy(f, new File("C:\\Users\\lenovo\\Desktop\\AutomationScreenshot\\screenshot1.jpg"));
      driver.navigate().back();
      
      driver.findElement(By.xpath("//*[@id=\"sitemap\"]/tbody/tr[2]/td[1]/a")).click();
      Files.copy(f, new File("C:\\Users\\lenovo\\Desktop\\AutomationScreenshot\\screenshot2.jpg"));
      driver.navigate().back();
      
      driver.findElement(By.xpath("//*[@id=\"sitemap\"]/tbody/tr[3]/td[1]/a")).click();
      Files.copy(f, new File("C:\\Users\\lenovo\\Desktop\\AutomationScreenshot\\screenshot3.jpg"));
      driver.navigate().back();
      
      
      driver.findElement(By.xpath("//*[@id=\"sitemap\"]/tbody/tr[4]/td[1]/a")).click();
      Files.copy(f, new File("C:\\Users\\lenovo\\Desktop\\AutomationScreenshot\\screenshot4.jpg"));
      driver.navigate().back();
      
      driver.findElement(By.xpath("//*[@id=\"sitemap\"]/tbody/tr[5]/td[1]/a")).click();
      Files.copy(f, new File("C:\\Users\\lenovo\\Desktop\\AutomationScreenshot\\screenshot5.jpg"));
      driver.navigate().back();
      
     

      
	}

}

