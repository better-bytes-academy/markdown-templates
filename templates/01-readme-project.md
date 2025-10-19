# [Tên Project] - Automation Testing Framework

## 📋 Mô tả
Mô tả ngắn gọn về project automation testing này, ứng dụng/hệ thống được test, và mục đích của framework.

## 🛠️ Công nghệ sử dụng
- **Ngôn ngữ**: Java 11
- **Test Framework**: TestNG / JUnit / Pytest
- **Automation Tool**: Selenium WebDriver / Playwright / Cypress
- **Build Tool**: Maven / Gradle
- **Reporting**: Allure / ExtentReports
- **CI/CD**: Jenkins / GitHub Actions

## 📁 Cấu trúc thư mục
```
project-root/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── pages/          # Page Object Models
│   │   │   ├── utils/          # Utilities & Helpers
│   │   │   └── config/         # Configuration files
│   └── test/
│       ├── java/
│       │   ├── tests/          # Test classes
│       │   └── data/           # Test data
│       └── resources/
│           └── testng.xml      # TestNG suite files
├── reports/                     # Test reports
├── screenshots/                 # Screenshots on failure
└── pom.xml                     # Maven dependencies
```

## ⚙️ Cài đặt & Cấu hình

### Yêu cầu hệ thống
- JDK 11 trở lên
- Maven 3.6+
- Chrome/Firefox browser

### Các bước cài đặt
1. Clone repository:
```bash
   git clone [repository-url]
   cd [project-name]
```

2. Cài đặt dependencies:
```bash
   mvn clean install
```

3. Cấu hình file `config.properties`:
```properties
   base.url=https://example.com
   browser=chrome
   implicit.wait=10
```

## 🚀 Chạy Tests

### Chạy tất cả tests
```bash
mvn clean test
```

### Chạy test suite cụ thể
```bash
mvn clean test -DsuiteXmlFile=testng.xml
```

### Chạy tests với browser khác
```bash
mvn clean test -Dbrowser=firefox
```

### Chạy parallel tests
```bash
mvn clean test -Dthreadcount=4
```

## 📊 Test Reports
- Reports được tạo trong thư mục: `target/allure-results/`
- Xem report:
```bash
  allure serve target/allure-results
```

## 📝 Quy tắc viết test
- Sử dụng Page Object Model pattern
- Tên test method phải mô tả rõ ràng: `test_<action>_<expected_result>`
- Mỗi test phải độc lập, không phụ thuộc lẫn nhau
- Sử dụng data provider cho test data-driven
- Luôn cleanup sau mỗi test

## 🐛 Troubleshooting

### Lỗi thường gặp

**Lỗi: WebDriver not found**
- Giải pháp: Đảm bảo WebDriverManager được cấu hình đúng

**Lỗi: Element not found**
- Giải pháp: Kiểm tra locator và thêm explicit wait

## 👥 Contributors
- [Tên bạn] - Test Automation Engineer

## 📄 License
MIT License

---
**Last Updated**: [Ngày tháng năm]