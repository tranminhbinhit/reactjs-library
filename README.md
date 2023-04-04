# Source
https://dev.to/alexeagleson/how-to-create-and-publish-a-react-component-library-2oe
# Setup & coding
Tạo packaget.js
```
npm init
```
Tạo các file trong /src

Tạo tsconfig.json & chỉnh config phù hợp
```
npx tsc --init
```
Thêm thư viện rollup
```
npm install rollup @rollup/plugin-node-resolve @rollup/plugin-typescript @rollup/plugin-commonjs rollup-plugin-dts --save-dev
```
Tạo file config rollup rollup.config.js

Chạy tạo lib trong thư mục dist
```
npm run rollup
```

# Public github package
Tạo file .npmrc với nội dung
C:\Users\{YOUR_WINDOWS_USERNAME}\.npmrc
```
registry=https://registry.npmjs.org/
@YOUR_GITHUB_USERNAME:registry=https://npm.pkg.github.com/
//npm.pkg.github.com/:_authToken=YOUR_AUTH_TOKEN
```
Public library lên github response
```
1. Chỉnh version phù hợp
npm publish

```
Kết quả
https://github.com/tranminhbinhit?tab=packages

# Document Library
## Rollup
    Mặc dù cả hai công cụ đều có thể hoàn thành cùng một mục tiêu tùy thuộc vào cấu hình, nhưng thông thường, 
    - webpack được sử dụng để đóng gói các ứng dụng
    - Rollup phù hợp với các thư viện đóng gói

    Cũng tương tự như webpack, rollup sử dụng hệ sinh thái plugin
    Theo thiết kế, bản tổng hợp không biết cách thực hiện mọi thứ, nó dựa vào các plugin được cài đặt riêng lẻ để thêm chức năng mà bạn cần.

    Rollup được tạo ra vì một lý do khác: làm phẳng các thư viện hiệu quả nhất, nó cho phép bạn code ứng dụng sử dụng các module ES2015, sau đó nó sẽ kết hợp tất cả các module thành một file nhằm giảm số lượng request http và cải thiện thời gian tải trang web. Mục đích của Rollup là trở nên nhanh và tạo các đoạn code rõ ràng và hiệu quả hơn bất kỳ công cụ đóng gói khác.
