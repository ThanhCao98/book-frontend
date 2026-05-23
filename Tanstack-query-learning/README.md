# Tanstack Query Learning

### Tại sao nên sử dụng Tanstack Query

**useEffect** là công cụ để kéo dữ liệu về chứ hoàn toàn không có khả năng  quản lý dữ liệu đó ⇒  Thiếu bộ não xử lý trung tâm. <br>

**Có 3 trường hợp khi không sử dụng Tanstack Query:**

* &#x20;Không biết khi nào data đã cũ để tự động gọi lại.
* Không biết các component khác cũng cần dữ liệu đó để dùng chung.
* Không biết dữ liệu trên serve đã thay đổi để tự động cập nhật.

&#x20;⇒ Thiếu một hệ thống quản lý tập trung để điều phối tất cả.

<figure><img src=".gitbook/assets/Screenshot 2026-05-23 at 13.49.50.png" alt=""><figcaption></figcaption></figure>

```
Fetch hay Axios giúp kết nối server. 
Tanstack Query giúp bạn đồng bộ dữ liệu đó với UI
một cách thông minh
```

