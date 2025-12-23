# Daily Habit Tracker — Gamified (Streamlit + Pandas)

Ứng dụng web theo dõi thói quen hằng ngày theo hướng **game hóa** (streak, level, rương thưởng, boss tuần). Dự án ưu tiên **xử lý dữ liệu và trực quan hóa** bằng **Pandas / NumPy / Matplotlib**, đồng thời dùng **Streamlit** để tạo giao diện web tương tác nhanh, dễ triển khai.

---

## Tổng quan
Ứng dụng biến việc duy trì thói quen thành các **nhiệm vụ (quests)**. Mỗi người dùng khi tạo mới sẽ được gán một bộ **thói quen cố định** (có thể cấu hình trong code), sau đó thực hiện check-in mỗi ngày. Hệ thống tự động tính điểm, thưởng theo streak và phát thưởng thông qua rương hằng ngày/tuần. Toàn bộ dữ liệu được lưu dạng **CSV** để đơn giản, dễ kiểm tra và thuận tiện cho báo cáo học thuật.

---

## Tính năng chính
- **Nhiệm vụ cố định (Fixed Quests/Habits)**
  - User mới tự động có bộ nhiệm vụ được định nghĩa sẵn.
  - Có thể **bật/tắt** nhiệm vụ (active) để phù hợp lịch cá nhân (tuỳ chọn: chỉnh điểm).

- **Check-in hằng ngày**
  - Đánh dấu từng nhiệm vụ theo ngày: **Completed / Missed**
  - Có thể ghi chú đi kèm.

- **Streak (chuỗi ngày liên tiếp)**
  - Tính streak cho các nhiệm vụ Daily.
  - Thưởng **milestone bonus** theo các mốc streak cấu hình (3/7/14/22/30…).

- **Daily Chest 🎁**
  - Hoàn thành **tất cả nhiệm vụ Daily đang active** trong ngày → mở rương.
  - Rương phát **loot ngẫu nhiên** theo trọng số (rarity) + điểm thưởng.

- **Weekly Boss 🐉**
  - Mỗi lần hoàn thành Daily sẽ cộng “damage” trong tuần.
  - Đạt ngưỡng mục tiêu → hạ boss và mở **Boss Chest** (loot “xịn” hơn).
  - Boss chest chỉ mở **1 lần/tuần**.

- **Kho đồ (Inventory)**
  - Tổng hợp vật phẩm đã nhận theo loại và độ hiếm.

- **Biểu đồ thống kê**
  - Vẽ biểu đồ **điểm theo ngày** trong 30 ngày gần nhất (bao gồm điểm loot) bằng Matplotlib.

- **Leaderboard (toàn hệ thống)**
  - Bảng xếp hạng nhiều user theo tổng điểm.
  - Ẩn mặc định, chỉ hiện khi bật trong sidebar.

---

## Công nghệ sử dụng
- **Python**
- **Streamlit** — giao diện web tương tác
- **Pandas / NumPy** — mô hình dữ liệu, xử lý log, tính điểm/streak/quest
- **Matplotlib** — biểu đồ và trực quan hóa

---

## Lưu trữ dữ liệu (CSV)
Trạng thái ứng dụng được lưu trong thư mục `./data/`:
- `users.csv` — thông tin người dùng
- `habits.csv` — danh sách nhiệm vụ cố định theo user (kèm active/points)
- `logs.csv` — lịch sử check-in theo ngày
- `rewards.csv` — lịch sử mở rương (daily/boss), loot và điểm thưởng

> Lưu CSV giúp hệ thống **dễ đọc – dễ debug – dễ trình bày** khi làm báo cáo.

---

## Hướng dẫn chạy

### 1) Chạy local (máy cá nhân)
Cài thư viện:
```bash
pip install streamlit pandas numpy matplotlib
