# Design and Evaluation of a Gamified Behavior Change Support System for Daily Habit Formation

Ứng dụng **Daily Habit Tracker & Gamify**, là một hệ thống hỗ trợ người dùng xây dựng và duy trì thói quen hằng ngày thông qua các cơ chế trò chơi hóa (Gamification).
Hệ thống giúp biến các thói quen khô khan thành trải nghiệm trực quan, có động lực và mang tính cạnh tranh lành mạnh.
---

## 1) Tính năng chính

**Mục tiêu của đề tài**

- Hỗ trợ người dùng hình thành thói quen tích cực
- Tăng mức độ duy trì thói quen thông qua Gamification
- Trực quan hóa dữ liệu tiến trình cá nhân
- Tạo môi trường cạnh tranh và tương tác cộng đồng
  
## 2) Các chức năng chính

**2.1. Hệ thống tính điểm (Point System)**

- Hệ thống tính điểm (Point System)
- Điểm nhiệm vụ (Task Point)
- Điểm chuỗi ngày liên tiếp (Streak)
- Điểm thưởng từ rương quà (Reward Chest)
- Tổng điểm dùng để xác định cấp độ (Level)

**2.2. Gamification**

- Hệ thống Level dựa trên tổng điểm tích lũy
- Cơ chế Boss:
 + Biến thói quen thành các “trận chiến”
 + Tăng tính giải trí và động lực cho người dùng

**2.3. Trực quan hóa dữ liệu**

- Biểu đồ đường theo dõi biến động điểm số trong 30 ngày (Matplotlib)
- Calendar Heatmap: Đánh giá mức độ kỷ luật thông qua màu sắc theo ngày

**2.4. Tính năng cộng đồng**

- Leaderboard thời gian thực
- So sánh thành tích giữa các người dùng trong hệ thống

## 3. Công nghệ sử dụng

- Ngôn ngữ: Python
- Framework: Streamlit
- Thư viện trực quan: Matplotlib
- Lưu trữ dữ liệu: CSV
- Triển khai thử nghiệm: Google Colab + Cloudflared

