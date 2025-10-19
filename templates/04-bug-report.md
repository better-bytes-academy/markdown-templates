# Bug Report - [Tên ngắn gọn của bug]

## Bug Information
- **Bug ID**: BUG-001
- **Reported by**: [Tên bạn]
- **Date**: [DD/MM/YYYY]
- **Environment**: Staging
- **Build Version**: v2.3.0

## Severity & Priority
- **Severity**: 🔴 Critical / 🟠 Major / 🟡 Minor / 🟢 Trivial
- **Priority**: High / Medium / Low

## Bug Description
Mô tả ngắn gọn về bug, hiện tượng xảy ra và ảnh hưởng.

## Steps to Reproduce
1. Navigate to https://staging.example.com/checkout
2. Add 3 items to cart
3. Proceed to checkout
4. Enter shipping information
5. Click "Place Order" button
6. Observe the error

## Expected Result
- Order should be placed successfully
- Confirmation page should display
- Email confirmation should be sent

## Actual Result
- Error message appears: "Payment gateway timeout"
- Order is not created in database
- User is stuck on checkout page

## Test Data Used
```json
{
  "user": "testuser@example.com",
  "items": ["ITEM001", "ITEM002", "ITEM003"],
  "payment_method": "credit_card"
}
```

## Attachments
- Screenshot: ![Error Screenshot](./screenshots/bug-001.png)
- Video recording: [Link to video]
- Log file: `error-log-2024-01-15.txt`

## Console Errors
```
Error: Payment gateway request timeout after 30s
at PaymentService.processPayment (PaymentService.java:45)
at CheckoutController.placeOrder (CheckoutController.java:120)
```

## Browser/Device Information
- **Browser**: Chrome 120.0.6099.129
- **OS**: Windows 11
- **Screen Resolution**: 1920x1080

## Frequency
- ⚫ Always (100%)
- ⚪ Sometimes (50%)
- ⚪ Rarely (<10%)

## Workaround
Có thể retry sau 5 phút hoặc sử dụng PayPal thay vì credit card.

## Additional Notes
Bug này chỉ xảy ra với orders có giá trị > $500. Orders nhỏ hơn hoạt động bình thường.

## Status History
| Date | Status | Updated By | Comment |
|------|--------|------------|---------|
| 15/01/2024 | Open | QA Team | Bug reported |
| 16/01/2024 | In Progress | Dev Team | Investigating |
| 17/01/2024 | Fixed | Dev Team | Increased timeout to 60s |
| 18/01/2024 | Retest | QA Team | Verification needed |