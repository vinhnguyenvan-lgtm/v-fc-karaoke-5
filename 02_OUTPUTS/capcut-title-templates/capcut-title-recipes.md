# Công thức Title CapCut — 5 phong cách

**Mặc định:** khung 9:16 (1080×1920), 30 fps, làm trên CapCut desktop. Mobile làm được y hệt, chỉ khác vị trí nút.
**Khung 16:9:** giảm cỡ chữ khoảng 30%. Vị trí Y trong bảng là tính từ tâm khung (âm = lên trên, dương = xuống dưới).
**Tên effect/animation** có thể đổi theo phiên bản và khu vực. Không thấy đúng tên thì gõ từ khoá trong ngoặc vào ô tìm kiếm.
**Font:** toàn bộ font dưới đây là font Google miễn phí, có hỗ trợ dấu tiếng Việt. Bạn tải về máy rồi cài vào CapCut (Text → Font → Import/Upload font, hoặc cài thẳng vào hệ điều hành).

**Lưu preset:** dựng xong thì chọn lớp chữ → nút **Save preset** (hoặc ngôi sao/bookmark trong tab Text). Animation và keyframe không lưu vào preset chữ được. Muốn giữ cả chuyển động, hãy lưu project mẫu riêng (vd `TITLE-LIBRARY`), khi cần thì copy lớp chữ sang project khác.

---

## 1. TỐI GIẢN (Minimal)

### 1A — Tiêu đề chính "Fade + giãn chữ"
| Thông số | Giá trị |
|---|---|
| Font | Be Vietnam Pro — Light (300) |
| Cỡ / màu | 9 · #FFFFFF |
| Character spacing | 8 |
| Case | IN HOA |
| Stroke / Shadow | Tắt hết |
| Vị trí | Giữa khung, Y = 0 |
| Thời lượng | 3s |

**Keyframe:**
- 0s: Opacity 0% · Scale 96% · Character spacing 2
- 0.6s: Opacity 100% · Scale 100% · Character spacing 8
- 2.4s: giữ nguyên
- 3.0s: Opacity 0%

Easing: chọn **Ease out** cho đoạn vào, **Ease in** cho đoạn ra (bấm chuột phải vào keyframe → curve).
Nếu bản của bạn không keyframe được Character spacing: bỏ dòng đó, dùng Animation In → **Fade in** (từ khoá *fade*), độ dài 0.6s.

### 1B — Lower third "gạch chân"
- Dòng 1 (tên): Be Vietnam Pro SemiBold, cỡ 6, trắng
- Dòng 2 (chức danh): Be Vietnam Pro Regular, cỡ 4, #FFFFFF opacity 70%
- Gạch: tạo lớp Text chỉ chứa ký tự `—` hoặc `_____`, màu nhấn (vd #E8FF59), đặt giữa 2 dòng
- Vị trí: góc dưới trái, X = -280 · Y = 620 (9:16)
- Animation In: dòng 1 **Slide right** (*slide*) 0.4s · dòng 2 cùng hiệu ứng, lùi 0.15s · gạch **Wipe** (*wipe*) 0.5s
- Animation Out: **Fade out** 0.3s cho cả 3 lớp

---

## 2. GLITCH

### 2A — Tiêu đề "RGB tách lớp"
Dựng 3 lớp chữ giống hệt nhau, chồng lên nhau:

| Lớp | Màu | Blend mode | Offset |
|---|---|---|---|
| Trên cùng | #FFFFFF | Normal | X 0 |
| Giữa | #FF0040 | Screen | X -6 |
| Dưới | #00F0FF | Screen | X +6 |

- Font: Anton, cỡ 12, IN HOA, spacing 2
- Thời lượng 2.5s

**Keyframe giật** (chỉ trên lớp đỏ và xanh, đặt keyframe cách nhau 2 frame):
- 0.00s: offset ±6
- 0.07s: offset ±18
- 0.13s: offset ±2
- 0.20s: offset ±12
- 0.27s: offset ±6, giữ đến hết
- Lặp lại cụm giật này ở 1.6s

Easing: **Linear** (glitch cần chuyển động gắt, không mượt).

**Thêm:** Effects → Video effects → *glitch* (vd Glitch, Shake, Signal), kéo phủ đúng 0.3s đầu và 0.3s ở mốc 1.6s.
**Nhanh hơn:** Animation In → *glitch* trên lớp trắng, độ dài 0.4s, bỏ phần keyframe.

### 2B — Chữ "nhiễu tín hiệu" cho lyric/tên bài
- Font: VT323, cỡ 9, #39FF14 (xanh terminal)
- Animation In: **Typewriter** (*typewriter / type*) 0.8s
- Loop animation: **Flicker** (*flicker / blink*)
- Phủ thêm effect *VHS* hoặc *scanline*, opacity khoảng 40%

---

## 3. KINETIC TYPOGRAPHY

### 3A — Từng chữ "đập" theo nhịp
Quy tắc: **mỗi từ là một lớp Text riêng**, đặt điểm bắt đầu đúng beat. Bật waveform của track nhạc để dóng beat; nếu BPM 120 thì mỗi beat dài 0.5s.

| Thông số | Giá trị |
|---|---|
| Font | Montserrat Black (900) |
| Cỡ | Từ khoá chính 16 · từ phụ 8 |
| Màu | Trắng; từ khoá chính tô màu nhấn #FFD400 |
| Vị trí | So le: từ lẻ Y = -150, từ chẵn Y = +150 |

**Keyframe cho mỗi từ:**
- Frame 0: Scale 140% · Opacity 0%
- Frame 4 (≈0.13s): Scale 95% · Opacity 100%
- Frame 7 (≈0.23s): Scale 100%
- Giữ đến khi từ tiếp theo xuất hiện, rồi cắt cứng (không fade)

Easing đoạn 0→4: **Ease out**.
Làm xong từ đầu tiên thì copy/paste ra các từ sau, chỉ sửa nội dung và vị trí.

### 3B — Câu "trượt khối" (dùng cho câu quote, hook đầu video)
- Font: Oswald Bold, cỡ 10, IN HOA, line spacing 0.8
- Tách câu thành 3 dòng, mỗi dòng một lớp
- Dòng 1 vào từ trái, dòng 2 từ phải, dòng 3 từ dưới, lệch nhau 0.1s
- Keyframe Position: điểm đầu nằm ngoài khung → 0.3s vào vị trí, easing **Ease out**
- Ra: cả 3 lớp Scale 100 → 0% trong 0.2s, easing **Ease in**
- Muốn dòng hiện ra như bị "cắt" ở mép: thêm Mask → **Linear** lên từng lớp

---

## 4. RETRO

### 4A — Tiêu đề "Synthwave 80s"
- Font: Bungee, cỡ 11
- Màu chữ: #FF2E97
- Stroke: #FFE45E, độ dày 15
- Shadow: #2B1055 · opacity 100% · blur 0 · distance 12 · angle 135° (bóng đặc, không nhoè)
- Glow (nếu bản của bạn có): #FF2E97, cường độ thấp
- Animation In: **Zoom in** hoặc **Bounce** (*bounce*) 0.5s
- Loop: **Wave** hoặc **Swing** (*wave*), nhẹ
- Nền: chọn Filter tông tím–hồng, thêm effect *grain* hoặc *VHS* opacity 30%

### 4B — Tiêu đề "Băng VHS 90s"
- Font: VT323, cỡ 8, trắng
- Đặt góc trên trái kiểu ngày giờ máy quay: `PLAY ▶  10.29.1996`
- Lớp phụ góc dưới: `SP 0:00:12`, cỡ 5
- Effects: *VHS* + *grain*, phủ cả clip
- Animation In: không dùng. Chữ xuất hiện cứng, đúng chất màn hình máy quay

### 4C — Tiêu đề "Poster cổ điển"
- Font: Pacifico (dòng chính) + Oswald (dòng phụ IN HOA, spacing 10)
- Màu: #F3E3C3 (giấy cũ) trên nền nâu đậm
- Shadow: #000000 · opacity 50% · blur 2 · distance 4
- Animation In: **Fade in** 0.8s; dòng phụ trễ 0.3s
- Filter: tông film ấm + grain

---

## 5. CINEMATIC

### 5A — Tiêu đề phim "Lộ ra từ bóng tối"
| Thông số | Giá trị |
|---|---|
| Font | Cormorant Garamond — Medium |
| Cỡ / màu | 10 · #EDE6D6 (trắng ngà) |
| Character spacing | 15 |
| Case | IN HOA |
| Thời lượng | 5s |

**Keyframe:**
- 0s: Opacity 0% · Scale 104%
- 2.0s: Opacity 100% · Scale 100%
- 4.0s: Opacity 100%
- 5.0s: Opacity 0%

Easing: **Ease in-out**, chuyển động phải chậm mới ra chất điện ảnh.
Mờ nét khi vào: Animation In → **Blur** (*blur*) 1.5s, dùng thay cho keyframe opacity ở đoạn đầu.

**Khung letterbox (thanh đen điện ảnh):**
- Cách 1: tìm effect *bars / cinema / letterbox*
- Cách 2: thêm lớp màu đen (Media → Library → *black*, hoặc ảnh PNG đen), Mask → **Mirror**, đảo mask (Invert), chỉnh để chừa dải giữa theo tỉ lệ 2.39:1

### 5B — Credit "tên + vai trò" kiểu trailer
- Dòng nhỏ phía trên: Be Vietnam Pro Regular, cỡ 3.5, spacing 20, opacity 70% → `A FILM BY`
- Dòng chính: Cormorant Garamond SemiBold, cỡ 8 → tên người
- Hai dòng xuất hiện cùng lúc, Fade in 1s, giữ 2s, Fade out 1s
- Chèn nhiều credit liên tiếp, giữa các credit để trống 0.5s màn đen

### 5C — Text "mở bằng ánh sáng"
- Font: Playfair Display Bold, cỡ 11, trắng
- Mask **Linear** trên lớp chữ, feather khoảng 30
- Keyframe vị trí mask: từ mép trái chạy sang mép phải trong 1.5s → chữ lộ dần như có vệt sáng quét qua
- Phủ effect *light leak* hoặc *flare* ở chế độ Screen, đặt đúng đoạn 1.5s này

---

## Bảng tra nhanh

| Phong cách | Font chính | Tốc độ vào | Easing | Nhận diện |
|---|---|---|---|---|
| Tối giản | Be Vietnam Pro Light | 0.5–0.8s | Ease out | Nhiều khoảng trống, spacing rộng |
| Glitch | Anton / VT323 | 0.2–0.4s | Linear | Tách màu RGB, giật |
| Kinetic | Montserrat Black / Oswald | 0.1–0.3s | Ease out | Khớp beat, scale mạnh |
| Retro | Bungee / Pacifico / VT323 | 0.4–0.6s | Bounce | Stroke dày, bóng đặc, grain |
| Cinematic | Cormorant / Playfair | 1.5–2s | Ease in-out | Chậm, spacing rộng, letterbox |
