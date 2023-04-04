## Setup & coding
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

Chạy tạo lib
```
npm run rollup
```

## Document Library
### Rollup
    Mặc dù cả hai công cụ đều có thể hoàn thành cùng một mục tiêu tùy thuộc vào cấu hình, nhưng thông thường, 
    - webpack được sử dụng để đóng gói các ứng dụng
    - Rollup phù hợp với các thư viện đóng gói

    Cũng tương tự như webpack, rollup sử dụng hệ sinh thái plugin
    Theo thiết kế, bản tổng hợp không biết cách thực hiện mọi thứ, nó dựa vào các plugin được cài đặt riêng lẻ để thêm chức năng mà bạn cần.

    Rollup được tạo ra vì một lý do khác: làm phẳng các thư viện hiệu quả nhất, nó cho phép bạn code ứng dụng sử dụng các module ES2015, sau đó nó sẽ kết hợp tất cả các module thành một file nhằm giảm số lượng request http và cải thiện thời gian tải trang web. Mục đích của Rollup là trở nên nhanh và tạo các đoạn code rõ ràng và hiệu quả hơn bất kỳ công cụ đóng gói khác.
