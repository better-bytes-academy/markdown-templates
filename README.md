# Markdown Templates

## Giới thiệu

Repository này chứa hướng dẫn cách viết Markdown và các mẫu Markdown thông dụng để sử dụng trong các dự án của bạn.

## Markdown là gì?

Markdown là một ngôn ngữ đánh dấu văn bản nhẹ (lightweight markup language) được tạo ra bởi John Gruber vào năm 2004. Markdown cho phép bạn viết văn bản có định dạng sử dụng cú pháp văn bản thuần túy dễ đọc và dễ viết.

## Cú pháp Markdown cơ bản

### 1. Tiêu đề (Headers)

```markdown
# Tiêu đề cấp 1
## Tiêu đề cấp 2
### Tiêu đề cấp 3
#### Tiêu đề cấp 4
##### Tiêu đề cấp 5
###### Tiêu đề cấp 6
```

### 2. Nhấn mạnh văn bản (Text Emphasis)

```markdown
*Chữ nghiêng* hoặc _Chữ nghiêng_
**Chữ đậm** hoặc __Chữ đậm__
***Chữ đậm và nghiêng*** hoặc ___Chữ đậm và nghiêng___
~~Gạch ngang~~
```

### 3. Danh sách (Lists)

**Danh sách không thứ tự:**
```markdown
- Mục 1
- Mục 2
  - Mục con 2.1
  - Mục con 2.2
- Mục 3
```

**Danh sách có thứ tự:**
```markdown
1. Mục đầu tiên
2. Mục thứ hai
3. Mục thứ ba
   1. Mục con 3.1
   2. Mục con 3.2
```

### 4. Liên kết (Links)

```markdown
[Văn bản hiển thị](https://example.com)
[Văn bản có tooltip](https://example.com "Đây là tooltip")
```

### 5. Hình ảnh (Images)

```markdown
![Văn bản thay thế](đường-dẫn-hình-ảnh.jpg)
![Văn bản thay thế](đường-dẫn-hình-ảnh.jpg "Tiêu đề hình ảnh")
```

### 6. Trích dẫn (Blockquotes)

```markdown
> Đây là một trích dẫn
> Có thể nhiều dòng
>
> > Trích dẫn lồng nhau
```

### 7. Code

**Code inline:**
```markdown
Sử dụng `code` trong câu
```

**Code block:**
````markdown
```javascript
function hello() {
  console.log("Hello World!");
}
```
````

### 8. Đường kẻ ngang (Horizontal Rules)

```markdown
---
hoặc
***
hoặc
___
```

### 9. Bảng (Tables)

```markdown
| Cột 1 | Cột 2 | Cột 3 |
|-------|-------|-------|
| Dữ liệu 1 | Dữ liệu 2 | Dữ liệu 3 |
| Dữ liệu 4 | Dữ liệu 5 | Dữ liệu 6 |

Căn chỉnh:
| Trái | Giữa | Phải |
|:-----|:----:|-----:|
| Text | Text | Text |
```

### 10. Checkbox (Task Lists)

```markdown
- [x] Nhiệm vụ đã hoàn thành
- [ ] Nhiệm vụ chưa hoàn thành
- [ ] Nhiệm vụ khác
```

## Một số Markdown templates tham khảo
1. [README project](./templates/01-readme-project.md)
2. [Test plan](./templates/02-test-plan.md)
3. [Test case](./templates/03-test-case.md)
4. [Bug report](./templates/04-bug-report.md)
5. [Các kiến thức được học](./templates/05-lesson-learned.md)

## Cộng đồng Better Bytes Academy

Better Bytes Academy xây dựng và phát triển các cộng đồng chất lượng cho QA/Tester:

### 🎭 Playwright Việt Nam

**Playwright Việt Nam** là cộng đồng lớn nhất về Playwright tại Việt Nam, nơi kết nối các QA Engineer, Test Automation Engineer và những người yêu thích automation testing.

**Tham gia cộng đồng:**
- Facebook Group: https://www.facebook.com/groups/playwright.automation.test
- Telegram: https://go.betterbytesvn.com/Automation-Testing-Forum
- Website: https://academy.betterbytesvn.com/

**Hoạt động của cộng đồng:**
- Chia sẻ kiến thức, kinh nghiệm về Playwright
- Tổ chức các workshop, webinar
- Hỗ trợ giải đáp thắc mắc
- Tổ chức các contest và thử thách

## Liên hệ

Nếu có bất cứ vấn đề gì liên quan đến nội dung hoặc bản quyền, vui lòng liên hệ trực tiếp tới **Better Bytes Academy** để được hỗ trợ và xử lý.

- **Email:** [betterbytes.academy@gmail.com](mailto:betterbytes.academy@gmail.com) 
- **Facebook:** [Fanpage Playwright Việt Nam](https://www.facebook.com/playwrightvietnam/)
- **Website:** https://academy.betterbytesvn.com/

<details>
<summary><strong>📮 Donate cho chúng mình</strong></summary>

#### Thông tin chuyển khoản

- **Ngân hàng:** Vietcombank  
- **Số tài khoản:** 9962275964  
- **Chủ tài khoản:** DO MINH PHONG
- **QR code**:
![QR donate](https://academy.betterbytesvn.com/wp-content/uploads/2025/09/image.png)

**Xin chân thành cảm ơn!** ❤️

</details>