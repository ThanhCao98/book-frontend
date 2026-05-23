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

### Điểm mạnh của Tanstack Query

| Tính năng chính                                                      | Ví dụ - Trang Blog                                                                                                                                                                                                                                      |
| -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Deduplication - Chống trùng lặp request**                          | Có 2 component trên cùng 1 trang và cả 2 cùng dùng chung 1 bộ dữ liệu thì API chỉ gọi 1 lần duy nhất                                                                                                                                                    |
| **Background Refetch - Tự động cập nhật dữ liệu ở nền**              | Khi chuyển từ tab chính sang tab khác rồi quay lại tab chính thì Tanstack Query sẽ âm thầm gọi lại API để kiểm tra dữ liệu mới (Toàn bộ quá trình diễn ra ở background, dữ liệu trên màn hình sẽ tự động thay đổi mà không cần người dùng phải nhấn F5) |
| **Automatic Revalidation - Tự động đồng bộ sau khi tạo dữ liệu mới** | Khi ấn nút "Đăng bài", bài viết mới xuất hiện ngay trong danh sách bên dưới mà form và danh sách không cần biết đến sự tồn tại của nhau                                                                                                                 |
| **Prefetching - Tải trước dữ liệu**                                  | Khi di chuyển giữa các trang hệ thống đã tải trước dữ liệu và catch lại tạo cảm giác trang load ngày lập tức                                                                                                                                            |
| **Optimistic UI**                                                    | Bấm vào nút "Thích" nó phản hồi ngay lập tức, không có 1 phần loading nào mà nó không hề chạy lên server update rồi mới chạy về client cập nhật UI                                                                                                      |

⇒ Tất cả đều xoay quanh 1 khái niệm cốt lõi là **Serve State Management**

