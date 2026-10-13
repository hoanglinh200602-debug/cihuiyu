# 词汇雨 — Pixel Vocabulary Rain ☔🌰

Game luyện từ vựng HSK1 theo 15 bài do người dùng cung cấp. Nhân vật quả sồi pixel di chuyển để đón các giọt mưa từ vựng.

## Chạy trên máy

Cài Node.js 18+ rồi chạy:

```bash
npm install
npm run dev
```

Mở địa chỉ localhost hiện trong terminal.

## Deploy Vercel

1. Tạo GitHub repository, tải toàn bộ các file trong thư mục này lên (giữ nguyên thư mục `src`).
2. Vercel → Add New Project → Import Git Repository.
3. Framework Preset: **Vite** (hoặc Other). Build Command: `npm run build`; Output Directory: `dist`.
4. Deploy. Những lần push code tiếp theo sẽ được Vercel cập nhật tự động.

## Các chức năng

- 15 bài, 335 mục từ (bao gồm từ trùng giữa các bài và một số danh từ riêng)
- 越译汉 / 汉译越 / 混合挑战
- 3 mức độ 小雨 / 中雨 / 暴雨
- Nhập Pinyin có số thanh điệu, `ü` → `v`, chấp nhận khoảng trắng
- Đáp án nghĩa Việt nhiều lựa chọn do giáo viên sửa được
- Hướng dẫn song ngữ trước khi chơi; tùy chọn ẩn hướng dẫn
- Nhân vật pixel vẽ bằng Canvas, hiệu ứng che ô / trúng mưa
- Điểm, tim, sao, từ sai, lưu tiến độ bằng localStorage
- Sửa ngân hàng từ, bật/tắt từ, nhập/xuất bản sao lưu JSON
- Nút điều khiển cảm ứng trên điện thoại

## Lưu ý về học liệu

Danh sách từ được nhập từ nội dung người dùng cung cấp, **chưa đối chiếu với bản in chính thức của giáo trình**. Một số mục ngữ pháp như `的`, `们`, `了` không phù hợp với kiểu dịch một-một; giáo viên nên tắt hoặc điều chỉnh đáp án trước khi dùng. Phiên âm thanh nhẹ, biến điệu và cách viết `-r` có thể có nhiều quy ước; hãy rà soát trong `src/vocab.json` hoặc phần giáo viên.

## Giới hạn V1

- Không có tài khoản/cloud sync. localStorage chỉ lưu trên cùng trình duyệt và thiết bị.
- Không có máy chủ, bảng xếp hạng chung hay nhập CSV/Excel (đang dùng JSON).
- Chế độ mưa nhiều giọt: trả lời theo thứ tự chạm; khi trả lời thì dừng các giọt còn lại.
- Nhân vật pixel được vẽ bằng mã nguồn, lấy cảm hứng từ ảnh tham khảo chứ không sao chép sprite pixel-for-pixel.
