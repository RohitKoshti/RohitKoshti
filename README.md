import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class LoginTest {
    public static void main(String[] args) {
        // Set the system property for the ChromeDriver executable
        System.setProperty("webdriver.chrome.driver", "path/to/chromedriver");

        // Create an instance of the ChromeDriver
        WebDriver driver = new ChromeDriver();

        // Navigate to the login page
        driver.get("https://gor-pathology.web.app/");

        // Find the username and password fields and enter the credentials
        WebElement usernameField = driver.findElement(By.id("username"));
        WebElement passwordField = driver.findElement(By.id("password"));

        usernameField.sendKeys("test@kennect.io");
        passwordField.sendKeys("Qwerty@1234");

        // Find the login button and click it
        WebElement loginButton = driver.findElement(By.id("login-button"));
        loginButton.click();

        // Wait for the home page to load and perform further actions or assertions
        // ...

        // Close the browser
        driver.quit();
    }
}
