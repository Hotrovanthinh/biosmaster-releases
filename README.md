# BIOS Master Tool Kit - bản phát hành

Kho này **chỉ chứa file phát hành** của BIOS Master Tool Kit (`BiosMaster.exe`). Phần mềm yêu cầu **mã kích hoạt** mua từ người bán; không có mã thì không dùng được.

## Tải về

- Trang các bản phát hành: <https://github.com/Hotrovanthinh/biosmaster-releases/releases/latest>
- Link tải trực tiếp bản mới nhất: <https://github.com/Hotrovanthinh/biosmaster-releases/releases/latest/download/BiosMaster.exe>

Mỗi bản phát hành ghi **mã SHA-256** của file. Kiểm tra bằng PowerShell:

```powershell
Get-FileHash .\BiosMaster.exe -Algorithm SHA256
```

## Kích hoạt

1. Mở `BiosMaster.exe` (Windows hỏi quyền quản trị thì chọn Yes).
2. Hộp **"Kích hoạt bản quyền"** hiện ra: dán mã `BMTK-XXXX-XXXX-XXXX-XXXX` rồi bấm **KÍCH HOẠT** (cần có mạng lúc này).
3. Mỗi mã dùng cho **1 máy**, dùng vĩnh viễn, **cập nhật miễn phí 1 năm** kể từ ngày mua (hết hạn vẫn dùng mãi bản đã có).
4. Đổi máy: mở phần mềm trên máy mới, nhập mã, bấm **CHUYỂN SANG MÁY NÀY** (tối đa 3 lần mỗi năm).

## Lưu ý

- Windows SmartScreen hoặc phần mềm diệt virus có thể cảnh báo vì file chưa có chữ ký số của nhà phát hành. So SHA-256 như trên để chắc chắn file nguyên vẹn.
- Phần mềm tự tải các công cụ ngoài (7-Zip, MEA...) trực tiếp từ nơi của tác giả khi bạn dùng đến chức năng cần chúng, và hỏi bạn trước.
- Cần hỗ trợ hoặc quên mã kích hoạt: liên hệ người bán.
