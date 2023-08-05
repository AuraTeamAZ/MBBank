# MBBank

EN: An unofficial API wrapper for Vietnam Military Commercial Joint Stock Bank (MBBank, MB). [Read full English version docs](./README.md)

VN: API wrapper không chính thức dành cho Ngân hàng Quân Đội (MB)

**Lưu ý**: Việc sử dụng thư viện này có thể trái với quy định của MB và có thể dẫn tới việc bị vô hiệu hóa tài khoản hoặc tương tự. Chúng tôi không chịu trách nhiệm nếu việc trên xảy ra.

## Giới thiệu

Mục đích của thư viện này là để giúp bạn dễ tương tác hơn với API của MB và có thể tự tạo được một cổng thanh toán riêng cho bản thân.

## Yêu cầu

Thư viện này sử dụng Tesseract để giải captcha của MB. Hãy đảm bảo rằng Tesseract đã được cài đặt: [tesseract-ocr](https://github.com/tesseract-ocr/tesseract)

## Dành cho Python

Thư viện này một phần được dựa trên dự án [MBBank](https://pypi.org/project/mbbank-lib/) của The DT.

## Ví dụ

### Lấy số dư tài khoản

```ts
(async () => {
    const { MB } = require("mbbank");
    
    const mb = new MB({ username: "0123456789", password: "foobar" });

    await mb.getBalance();
})
```

### Lấy lịch sử giao dịch

```ts
(async () => {
    const { MB } = require("mbbank");
    
    const mb = new MB({ username: "0123456789", password: "foobar" });

    await mb.getTransactionHistory();
})
```

## Giấy phép

Giấy phép MIT