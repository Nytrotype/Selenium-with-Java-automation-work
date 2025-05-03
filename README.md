## **Project Overview**
This project focuses on automating web applications using **Selenium WebDriver** with **Java**. The goal is to create reliable, reusable test scripts for browser automation on **Microsoft Edge**.

## **Features**
✅ **Automated Browser Navigation** – Open and interact with web pages  
✅ **Google Search Test** – Execute basic automation on Google.com  
✅ **Cross-Browser Compatibility** – Primarily using Microsoft Edge  
✅ **JUnit Integration** – Structured test cases using JUnit framework  
✅ **Data-Driven Testing** – Ability to parameterize tests with external data  

## **Prerequisites**
Before running this project, ensure you have the following installed:
- **Java JDK** (Latest version)
- **Eclipse IDE** (or IntelliJ IDEA)
- **Selenium WebDriver** (`selenium-java` dependency)
- **Microsoft Edge WebDriver** ([Download here](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/))
- **Maven** (for dependency management)

## **Installation**
### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/Nytrotype/Selenium-with-Java-automation-work.git
cd Selenium-with-Java-automation-work
```

### **2️⃣ Open in Eclipse**
1. **Open Eclipse** → Click **File** → **Open Projects from File System**  
2. Select the **cloned project folder** → Click **Finish**  

### **3️⃣ Install Dependencies**
If using **Maven**, update dependencies by running:
```sh
mvn clean install
```
📌 This downloads required libraries (Selenium, JUnit, WebDriver).

## **Usage**
### **Run Basic Google Search Test**
Execute the following test case in Eclipse:
```java
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.edge.EdgeDriver;

public class GoogleSearchTest {
    public static void main(String[] args) {
        System.setProperty("webdriver.edge.driver", "C:\\WebDriver\\msedgedriver.exe");
        WebDriver driver = new EdgeDriver();
        
        driver.get("https://www.google.com");

        WebElement searchBox = driver.findElement(By.name("q"));
        searchBox.sendKeys("Microsoft Copilot");
        searchBox.submit();
        
        try { Thread.sleep(3000); } catch (InterruptedException e) { e.printStackTrace(); }
        driver.quit();
    }
}
```

## **Contributing**
🔹 **Fork this repository**  
🔹 Submit **pull requests** for new test cases  
🔹 Improve efficiency with **better locators & assertions**  

## **License**
📜 This project is licensed under the **MIT License**. See the `LICENSE` file for more details.

## **Contact**
📩 Maintainer: Nytrotype  
💬 Open issues for support  
