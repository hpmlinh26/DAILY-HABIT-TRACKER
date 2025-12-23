# Daily Habit Tracker — Game Mode (Streamlit)

Ứng dụng **Daily Habit Tracker & Gamify** viết bằng **Python + Streamlit** (ưu tiên Pandas/Numpy/Matplotlib), giúp người dùng theo dõi thói quen theo ngày theo kiểu “nhiệm vụ trong game”: hoàn thành quest, nhận thưởng, lên level và có bảng xếp hạng.

---

## 1) Tính năng chính

### ✅ Fixed Quests (Nhiệm vụ cố định)
Mỗi user được gán sẵn bộ quest:
- Steps >= 8000  
- Water >= 2000 ml  
- Study >= 1 hour  
- Sleep >= 7 hours  
- Wake up <= 07:00  

Bạn có thể **bật/tắt quest** và **chỉnh điểm** ở trang **Manage → Quests**.

### ✅ Check-in hằng ngày (Today)
- Chọn ngày, tick **Done/Missed** cho từng quest
- Ghi chú (note) theo từng quest

### 🎁 Daily Chest (Rương hằng ngày)
Nếu bạn **hoàn thành tất cả Daily quests trong ngày**, bạn được mở **Daily Chest** để nhận:
- điểm thưởng cố định + loot ngẫu nhiên (Coin/Gem/Badge…)

### 🐉 Weekly Boss + Boss Chest
- Mỗi lần hoàn thành daily quest sẽ gây “damage”
- Đủ damage trong tuần sẽ được mở **Boss Chest** (phần thưởng lớn hơn)

### 🔥 Streak Bonus
Tự tính thưởng theo mốc streak: **3/7/14/22/30 ngày** (dựa trên Completed liên tiếp).

### 🗓️ Lịch 30 ngày (Calendar)
Lịch 30 ngày hiển thị mức độ hoàn thành daily quest theo màu (emoji):
- ⬜ 0%
- 🟥 thấp
- 🟧 trung bình
- 🟨 gần đủ
- 🟩 100%

### 🏆 Leaderboard (tuỳ chọn)
Bảng xếp hạng toàn hệ thống theo tổng điểm.
Người dùng chỉ thấy khi tick “Hiện Leaderboard”.

---

## 2) Công nghệ sử dụng
- **Streamlit**: tạo web UI nhanh
- **Pandas**: quản lý dữ liệu dạng bảng (users/habits/logs/rewards)
- **NumPy**: random loot, xử lý mảng
- **Matplotlib**: vẽ biểu đồ điểm theo ngày

---

## 3) Cấu trúc dữ liệu (CSV)
Dữ liệu được lưu trong thư mục `data/`:
- `users.csv`: danh sách người dùng
- `habits.csv`: danh sách quest/habit theo user
- `logs.csv`: lịch sử check-in theo ngày
- `rewards.csv`: lịch sử mở rương (daily/boss)

> Lưu bằng CSV giúp dễ đọc, dễ debug, dễ nộp bài/đính kèm báo cáo.

---
 
