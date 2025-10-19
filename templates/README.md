## Các mẫu Markdown phổ biến

### Mẫu README.md cho dự án

```markdown
# Tên Dự Án

Mô tả ngắn gọn về dự án của bạn.

## Tính năng

- Tính năng 1
- Tính năng 2
- Tính năng 3

## Cài đặt

\`\`\`bash
npm install ten-du-an
\`\`\`

## Sử dụng

\`\`\`javascript
const project = require('ten-du-an');
project.run();
\`\`\`

## Đóng góp

Mọi đóng góp đều được hoan nghênh! Vui lòng tạo pull request.

## Giấy phép

MIT License
```

### Mẫu tài liệu API

```markdown
# API Documentation

## Endpoint: GET /api/users

Lấy danh sách người dùng

### Parameters

| Tên | Kiểu | Bắt buộc | Mô tả |
|-----|------|----------|-------|
| page | integer | Không | Số trang (mặc định: 1) |
| limit | integer | Không | Số kết quả mỗi trang (mặc định: 10) |

### Response

\`\`\`json
{
  "data": [
    {
      "id": 1,
      "name": "Nguyễn Văn A",
      "email": "a@example.com"
    }
  ],
  "total": 100,
  "page": 1
}
\`\`\`

### Error Codes

| Code | Mô tả |
|------|-------|
| 400 | Yêu cầu không hợp lệ |
| 404 | Không tìm thấy |
| 500 | Lỗi máy chủ |
```

### Mẫu Changelog

```markdown
# Changelog

Tất cả các thay đổi quan trọng của dự án này sẽ được ghi lại trong file này.

## [1.0.1] - 2024-01-15

### Added
- Thêm tính năng mới X
- Thêm hỗ trợ cho Y

### Changed
- Cải thiện hiệu suất của Z
- Cập nhật dependencies

### Fixed
- Sửa lỗi A
- Sửa lỗi B

### Removed
- Xóa feature cũ C

## [1.0.0] - 2024-01-01

### Added
- Phiên bản đầu tiên
```

### Mẫu Contributing Guide

```markdown
# Hướng dẫn đóng góp

Cảm ơn bạn đã quan tâm đến việc đóng góp cho dự án!

## Quy trình đóng góp

1. Fork repository
2. Tạo branch mới (\`git checkout -b feature/TinhNangMoi\`)
3. Commit thay đổi (\`git commit -m 'Thêm tính năng mới'\`)
4. Push lên branch (\`git push origin feature/TinhNangMoi\`)
5. Tạo Pull Request

## Quy tắc coding

- Sử dụng 2 spaces cho indentation
- Viết comments rõ ràng
- Tuân thủ style guide của dự án

## Báo lỗi

Khi báo lỗi, vui lòng cung cấp:
- Mô tả chi tiết lỗi
- Các bước tái hiện
- Môi trường (OS, version, v.v.)
- Screenshots nếu có
```

### Mẫu Issue Template

```markdown
## Mô tả vấn đề

Mô tả rõ ràng và ngắn gọn về vấn đề.

## Các bước tái hiện

1. Truy cập '...'
2. Click vào '....'
3. Scroll xuống '....'
4. Thấy lỗi

## Kết quả mong đợi

Mô tả bạn mong đợi điều gì xảy ra.

## Kết quả thực tế

Mô tả điều gì thực sự xảy ra.

## Screenshots

Nếu có thể, thêm screenshots để minh họa vấn đề.

## Môi trường

- OS: [e.g. Windows 10, macOS 13.0]
- Browser: [e.g. Chrome 120, Firefox 121]
- Version: [e.g. 1.0.0]

## Thông tin bổ sung

Thêm bất kỳ thông tin nào khác về vấn đề.
```

## Công cụ hữu ích

- [Markdown Guide](https://www.markdownguide.org/) - Hướng dẫn Markdown đầy đủ
- [Dillinger](https://dillinger.io/) - Trình soạn thảo Markdown trực tuyến
- [StackEdit](https://stackedit.io/) - Trình soạn thảo Markdown trong trình duyệt
- [Markdown Table Generator](https://www.tablesgenerator.com/markdown_tables) - Tạo bảng Markdown

## GitHub Flavored Markdown (GFM)

GitHub có một số extension cho Markdown:

### Syntax Highlighting

````markdown
```python
def hello_world():
    print("Hello, World!")
```
````

### Mentions

```markdown
@username - Nhắc đến user
#123 - Tham chiếu đến issue/PR
```

### Emoji

```markdown
:smile: :heart: :rocket:
```

## Mẹo và thủ thuật

1. **Xuống dòng**: Thêm 2 khoảng trắng ở cuối dòng hoặc sử dụng thẻ \`<br>\`
2. **Escape ký tự đặc biệt**: Sử dụng backslash \`\\*\` để hiển thị ký tự thay vì format
3. **HTML trong Markdown**: Bạn có thể sử dụng HTML trực tiếp trong Markdown
4. **Anchor links**: Tạo link đến heading: \`[Link](#tiêu-đề)\`

## Đóng góp

Nếu bạn muốn đóng góp thêm mẫu hoặc hướng dẫn, vui lòng tạo pull request!

## Giấy phép

MIT License - Tự do sử dụng và chỉnh sửa
