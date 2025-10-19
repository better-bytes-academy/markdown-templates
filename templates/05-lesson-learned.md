# 📚 Lessons Learned - Automation Testing

> Ghi chú các bài học, kinh nghiệm, tips & tricks trong quá trình làm automation testing

---

## 🗓️ Tháng 10/2024

### ✅ Lesson #1: Sử dụng WebDriverWait thay vì Thread.sleep()

**Ngày học**: 15/10/2024  
**Tình huống**: Tests thường fail do elements load chậm  
**Vấn đề gặp phải**:
```java
// ❌ Cách làm sai
Thread.sleep(5000); // Hard wait
driver.findElement(By.id("submitBtn")).click();
```

**Giải pháp**:
```java
// ✅ Cách làm đúng
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
WebElement submitBtn = wait.until(
    ExpectedConditions.elementToBeClickable(By.id("submitBtn"))
);
submitBtn.click();
```

**Bài học rút ra**:
- Thread.sleep làm tests chạy chậm không cần thiết
- Explicit wait chỉ đợi đến khi điều kiện thỏa mãn
- Tests chạy nhanh hơn và ổn định hơn

**Tags**: `#selenium` `#wait` `#best-practice`

**Tham khảo**: [Selenium Waits Documentation](https://www.selenium.dev/documentation/webdriver/waits/)

---

### ✅ Lesson #2: Page Object Model giúp code dễ maintain

**Ngày học**: 18/10/2024  
**Tình huống**: Khi UI thay đổi phải update nhiều test files  
**Vấn đề gặp phải**:
- Locators bị duplicate ở nhiều nơi
- Khi button thay đổi ID phải sửa 20+ files

**Giải pháp**: Implement Page Object Model
```java
// LoginPage.java
public class LoginPage {
    private WebDriver driver;
    
    @FindBy(id = "username")
    private WebElement usernameField;
    
    @FindBy(id = "password")
    private WebElement passwordField;
    
    @FindBy(css = ".login-btn")
    private WebElement loginButton;
    
    public void login(String username, String password) {
        usernameField.sendKeys(username);
        passwordField.sendKeys(password);
        loginButton.click();
    }
}
```

**Bài học rút ra**:
- Tách UI logic ra Page Objects
- Mỗi page là một class
- Khi UI thay đổi chỉ cần sửa 1 chỗ
- Tests code ngắn gọn, dễ đọc hơn

**Tags**: `#design-pattern` `#pom` `#maintainability`

---

### ✅ Lesson #3: Data-driven testing với TestNG DataProvider

**Ngày học**: 22/10/2024  
**Tình huống**: Cần test login với nhiều user accounts khác nhau  
**Giải pháp**:
```java
@DataProvider(name = "loginData")
public Object[][] getLoginData() {
    return new Object[][] {
        {"user1@test.com", "pass123", true},
        {"user2@test.com", "pass456", true},
        {"invalid@test.com", "wrong", false}
    };
}

@Test(dataProvider = "loginData")
public void testLogin(String username, String password, boolean shouldPass) {
    loginPage.login(username, password);
    if (shouldPass) {
        Assert.assertTrue(dashboardPage.isDisplayed());
    } else {
        Assert.assertTrue(loginPage.hasError());
    }
}
```

**Bài học rút ra**:
- 1 test method có thể chạy với nhiều bộ data
- Dễ dàng thêm test cases mới
- Code gọn gàng, không duplicate logic

**Tags**: `#testng` `#data-driven` `#parameterization`

---

## 🗓️ Tháng 9/2024

### ✅ Lesson #4: Chụp screenshot khi test fail

**Ngày học**: 05/09/2024  
**Vấn đề**: Khó debug khi test fail trên CI/CD  
**Giải pháp**:
```java
@AfterMethod
public void tearDown(ITestResult result) {
    if (result.getStatus() == ITestResult.FAILURE) {
        String screenshotPath = captureScreenshot(result.getName());
        // Attach to Allure report
        Allure.addAttachment("Failed Screenshot", 
            new ByteArrayInputStream(((TakesScreenshot) driver)
            .getScreenshotAs(OutputType.BYTES)));
    }
    driver.quit();
}
```

**Bài học rút ra**:
- Luôn capture screenshot/video khi fail
- Attach vào test report để dễ debug
- Giúp reproduce bug nhanh hơn

**Tags**: `#debugging` `#screenshot` `#reporting`

---

### ✅ Lesson #5: Tránh hard-code test data trong code

**Ngày học**: 12/09/2024  
**Vấn đề**: Test data thay đổi thường xuyên  
**Giải pháp**:
```java
// config.properties
test.url=https://staging.example.com
test.username=testuser@example.com
test.password=Test@123

// TestBase.java
Properties config = new Properties();
config.load(new FileInputStream("config.properties"));
String url = config.getProperty("test.url");
```

**Bài học rút ra**:
- Tách config ra file riêng (properties/yaml/json)
- Dễ thay đổi cho các environments khác nhau
- Không cần rebuild code khi đổi config

**Tags**: `#configuration` `#test-data` `#environment`

---

## 📊 Thống kê

**Tổng số bài học**: 5  
**Tháng 10/2024**: 3 lessons  
**Tháng 9/2024**: 2 lessons  

## 📑 Phân loại theo Tags

### Design Pattern
- Lesson #2: Page Object Model

### Selenium Best Practices
- Lesson #1: WebDriverWait
- Lesson #4: Screenshot on failure

### Test Framework
- Lesson #3: Data-driven testing
- Lesson #5: Configuration management

---

## 🎯 Action Items

- [ ] Refactor tất cả tests sang POM pattern
- [ ] Setup screenshot capture cho CI/CD pipeline
- [ ] Tạo centralized config management
- [ ] Document thêm về parallel testing

---

## 💡 Quick Tips

> **Tip 1**: Luôn review lại lessons learned hàng tuần để cải thiện  
> **Tip 2**: Share với team để mọi người cùng học hỏi  
> **Tip 3**: Update lessons này thường xuyên khi gặp vấn đề mới

---

**Last Updated**: 22/10/2025
**Maintained by**: [Tên bạn]