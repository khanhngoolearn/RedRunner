# Lab 01 - Khám phá dự án RedRunner

## Thông tin sinh viên
- **Họ tên**: Nguyễn Đình Khánh
- **MSSV**: 2212552
- **Lớp**: CTK46B

## Mô tả
Bài thực hành Lab 01 môn **Game 2D Development with Unity**.  
Khám phá và phân tích dự án game RedRunner - một Platformer 2D mã nguồn mở được phát triển bởi Bayat Games.

## Các thay đổi đã thực hiện
1. **Thay đổi tốc độ chạy**: 9 → 15
2. **Thay đổi lực nhảy**: 12 → 24 
3. **Thay đổi trọng lực**: 1.5 → 0.5 
4. **Thêm Coin vào scene**: Đặt tại vị trí gần điểm xuất phát, coin hoạt động tốt (phát ra âm thanh, hiệu ứng biến mất và tăng điểm).

## Screenshots
Dưới đây là các ảnh chụp màn hình minh chứng cho quá trình thực hành (đính kèm trong thư mục `screenshots/` hoặc nhúng trực tiếp):

1. **Unity Editor tổng quan** – thể hiện rõ các cửa sổ Scene, Game, Hierarchy, Inspector.
2. **Game đang chạy – Màn hình Menu**.
3. **Game đang chạy – Gameplay** (nhân vật đang chạy/nhảy).
4. **Game đang chạy – Game Over**.
5. **Inspector của nhân vật RedRunner** – hiển thị đầy đủ các Component.
6. **Code trong Visual Studio** – một phần của `GameManager.cs` hoặc `RedCharacter.cs`.

## Kiến thức đã học được
1. **Cấu trúc dự án Unity**: hiểu rõ vai trò của các thư mục như `Assets/Scenes`, `Assets/Scripts`, `Assets/Prefabs`, v.v.
2. **Prefab**: khái niệm và lợi ích của việc sử dụng Prefab (tái sử dụng, cập nhật đồng loạt, sinh đối tượng động).
3. **Component cơ bản**: Transform, Rigidbody2D, Collider2D, Animator, AudioSource – cách chúng phối hợp để tạo chuyển động và va chạm.
4. **Tổ chức Scene**: các đối tượng gốc trong Hierarchy và chức năng của từng Canvas (In-Game, Pause, End, Start,...).
5. **Singleton Pattern**: áp dụng trong `GameManager` để quản lý trạng thái game toàn cục.
6. **Xử lý di chuyển và nhảy**: sử dụng `Rigidbody2D.velocity` kết hợp với kiểm tra mặt đất (`GroundCheck`).
7. **Hệ thống Enemy**: thiết kế đa dạng (Spike, Water, Saw, Eye,...) sử dụng abstract class `Enemy` và override phương thức `Kill()`.
8. **Collision vs Trigger**: phân biệt qua ví dụ Spike (dùng `OnCollisionStay2D`, chỉ chết khi chạm đúng mặt nhọn) và Water (dùng `OnTriggerEnter2D`, chết ngay khi vào vùng).
9. **Event/Delegate**: `GameManager` dùng event để thông báo thay đổi điểm, âm thanh, reset game mà không cần tham chiếu trực tiếp.
10. **Lưu dữ liệu**: sử dụng thư viện `SaveGameFree` để lưu điểm cao, số xu và điểm cuối cùng khi thoát game.
