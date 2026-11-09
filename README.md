# Bộ skill SEO tiếng Việt cơ bản cho Claude

Ba skill cho Claude: **nghiên cứu từ khoá → lên dàn ý → viết bài SEO**, viết cho thị trường
Việt Nam. **Không cần tài khoản công cụ SEO trả phí** — Claude tự tìm Google bằng công cụ tìm
web có sẵn trong gói Claude.

| Skill | Làm gì | Ra gì |
|---|---|---|
| [`tu-khoa-co-ban`](tu-khoa-co-ban/SKILL.md) | Mở rộng từ khoá, phân loại ý định tìm kiếm, gom nhóm, lập silo, xếp ưu tiên | Bảng từ khoá + bảng nhóm + sơ đồ silo + thẻ từ khoá |
| [`dan-y-co-ban`](dan-y-co-ban/SKILL.md) | Đọc top Google, rút heading đối thủ, tìm khoảng trống, chọn khung bài | Dàn ý H1/H2/H3 có ghi chú viết + Meta + FAQ + brief |
| [`viet-bai-co-ban`](viet-bai-co-ban/SKILL.md) | Viết bài theo dàn ý, có nguồn cho mọi con số, lọc văn máy, chặn từ tuyệt đối | Bài sạch để đăng + ghi chú làm việc + schema JSON-LD |

Ba skill nối tiếp nhau: thẻ từ khoá → dàn ý → bài viết. Dùng riêng từng cái cũng được.

## Chuẩn bài viết

- Trả lời ngay trong 40–60 từ đầu bài và đầu mỗi mục (dễ được Google / AI trích dẫn).
- Mỗi đoạn đọc tách riêng vẫn hiểu.
- **Có nguồn đã đọc thật mới viết con số** — không bịa giá, thống kê, chuyên gia.
- Chặn từ tuyệt đối "nhất, số 1, hàng đầu…" khi không có chứng cứ (Luật Quảng cáo Việt Nam).
- E-E-A-T theo mức rủi ro ngành (sức khoẻ, tài chính, pháp lý cần tác giả, người duyệt, nguồn chính thống).
- Lọc 14 dấu hiệu văn máy tiếng Việt.
- Tự chấm 8 tiêu chí trước khi giao.

## Cài đặt

**claude.ai / app Claude (Pro, Max, Team, Enterprise):**
1. Tải 3 file zip ở mục [Releases](../../releases/latest).
2. Settings → Capabilities: bật *Code execution and file creation*.
3. Mục Skills → *Upload skill* → chọn lần lượt 3 file zip.
4. Khi chat, bật **Web search**.

**Claude Code:** chép 3 thư mục vào `~/.claude/skills/`:
```bash
git clone https://github.com/ibangtam/skill-seo-co-ban.git
cp -R skill-seo-co-ban/*-co-ban ~/.claude/skills/
```

## Dùng thế nào

| Việc | Gõ ví dụ |
|---|---|
| Nghiên cứu từ khoá | "Nghiên cứu từ khoá cho: máy lọc nước, lõi lọc nước. Bán toàn quốc, mục tiêu ra đơn." |
| Lên dàn ý | "Lên dàn ý cho từ khoá: cách chọn máy lọc nước cho gia đình" |
| Viết bài | "Viết bài theo dàn ý trên" — hoặc "Viết bài SEO cho từ khoá: …" |

Mẹo: điền một lần [hồ sơ thương hiệu](viet-bai-co-ban/references/ho-so-thuong-hieu.md) rồi dán vào
đầu cuộc trò chuyện hoặc vào Project — bài sẽ đúng giọng hơn.

## Giới hạn (nói thật)

- **Không có số lượt tìm kiếm thật** — chỉ ước lượng Cao / Vừa / Thấp. Muốn có số: dán file xuất
  Google Keyword Planner (miễn phí khi có tài khoản Google Ads), Search Console của chính website,
  hoặc Ahrefs / Semrush nếu có.
- Công cụ tìm web của Claude thường không hiện "Mọi người cũng hỏi", quảng cáo, và thứ tự kết quả
  không chắc là thứ hạng Google Việt Nam → các phép đếm "top 10" là gần đúng.
- Bài viết ra là **bản nháp tốt**, vẫn cần người đọc lại trước khi đăng, nhất là ngành sức khoẻ,
  tài chính, pháp lý. Chỗ ghi `[CẦN …]` là thông tin bạn tự điền.

## Ghi nguồn

Bộ lọc văn máy (`viet-bai-co-ban/references/loc-dau-van-may.md`) Việt hoá và rút gọn theo tinh
thần hướng dẫn *Signs of AI writing* của WikiProject AI Cleanup (Wikipedia) và dự án
[blader/humanizer](https://github.com/blader/humanizer) (MIT).

## Đóng góp

Thấy skill làm sai, mơ hồ, hoặc có cách hay hơn — mở Issue hoặc Pull Request. Ví dụ đầu ra thật
(đã ẩn thông tin khách) rất được hoan nghênh.

## Giấy phép

[MIT](LICENSE) — dùng, sửa, chia sẻ tự do, kể cả cho mục đích thương mại.

Do **SEO Băng Tâm** xây dựng và chia sẻ cho cộng đồng SEO Việt Nam.

---

### English (short)

Three Claude skills for **Vietnamese SEO**: keyword research → content outline → article writing.
No paid SEO tools required — they use Claude's built-in web search, plus any data you paste
(Keyword Planner, Search Console, Ahrefs exports). Install the zips from Releases on claude.ai,
or copy the folders into `~/.claude/skills/` for Claude Code. MIT licensed.
