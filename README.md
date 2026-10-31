# BIOS Master Tool Kit

**Bộ công cụ chuyên nghiệp cho kỹ thuật viên: đọc, phân tích và xử lý firmware BIOS/UEFI của laptop và máy bộ trên Windows.**

Giao diện chia theo hãng (Dell, HP, Apple, Lenovo, AMI, Chromebook) kèm bộ công cụ dùng chung. Mọi thao tác trong một cửa sổ, tiếng Việt và tiếng Anh, chế độ sáng và tối.

| | |
|---|---|
| **Tải bản mới nhất** | [BiosMaster.exe](https://github.com/Hotrovanthinh/biosmaster-releases/releases/latest/download/BiosMaster.exe) · [Ghi chú các phiên bản](https://github.com/Hotrovanthinh/biosmaster-releases/releases) |
| **Hệ điều hành** | Windows 10 / 11 (64-bit) |
| **Giấy phép** | Mua một lần, dùng vĩnh viễn · 1 mã = 1 máy · cập nhật miễn phí 1 năm · gia hạn cập nhật theo năm |

---

## Tính năng

| Mục | Nội dung chính |
|---|---|
| **DELL** | Đọc thông tin DMI, mở khóa và vá các dạng BIOS Dell, giải nén gói PFS, tải BIOS mới nhất |
| **HP** | Đọc DMI, xử lý gói SoftPaq / SFX, vá BIOS HP (G8, G9), dọn dẹp VSS |
| **APPLE** | Đọc thông tin và vá firmware Apple |
| **LENOVO** | Đọc DMI và xử lý BIOS Lenovo |
| **AMI BIOS** | Đọc thông tin, vá BIOS AMI, dọn SPD và VSS |
| **CHROMEBOOK** | Vá BIOS Chromebook |
| **CÔNG CỤ** | Phân tích Intel ME (MEA), RCUnlocker, trích và thay logo BIOS, trích VBT, kiểm tra Secure Boot, **GIẢI NÉN** 16 loại gói firmware (Dell PFS, AMI, Award, Insyde, Phoenix, Fujitsu, Panasonic, Toshiba, Apple EFI, VAIO...) |

**Tiện ích đi kèm**

- Tự nhận diện hãng BIOS khi nạp tệp; nhầm hãng thì hỏi chuyển tab hoặc tiếp tục.
- Kéo-thả tệp thẳng vào cửa sổ, kể cả khi chạy quyền quản trị.
- Nhật ký thao tác ngay trong app và file nhật ký đầy đủ để gửi hỗ trợ.
- **Không cần cài Python hay thư viện nào.** Công cụ ngoài (7-Zip, MEA, BIOSUtilities, UEFIExtract, ComExtract) chỉ được tải khi bạn dùng đến chức năng cần chúng: app hỏi trước, lấy thẳng từ nơi của tác giả và kiểm tra SHA-256 trước khi dùng.
- Tự báo khi có phiên bản mới trong thời hạn cập nhật của bạn.

## Yêu cầu hệ thống

- Windows 10 hoặc 11, 64-bit.
- Kết nối Internet khi **kích hoạt** (một lần), khi tải công cụ ngoài lần đầu, và để xác nhận giấy phép (tự động, xem mục *Giấy phép*).
- Quyền Administrator: app tự xin nâng quyền (UAC) khi mở. Từ chối thì app vẫn chạy, chỉ các tính năng cần quyền quản trị bị hạn chế.
- Dung lượng: khoảng 20 MB cho app, cộng khoảng 30 MB nếu tải đủ công cụ ngoài.

## Bắt đầu nhanh

1. Tải [BiosMaster.exe](https://github.com/Hotrovanthinh/biosmaster-releases/releases/latest/download/BiosMaster.exe) và chạy (Windows hỏi quyền quản trị thì chọn **Yes**).
2. Hộp **"Kích hoạt bản quyền"** hiện ra: dán mã kích hoạt `BMTK-XXXX-XXXX-XXXX-XXXX` bạn nhận khi mua, bấm **KÍCH HOẠT**.
3. Dùng ngay. Từ lần sau app mở thẳng, không hỏi lại mã.

Kiểm tra file tải về nguyên vẹn (mã SHA-256 được ghi ở trang từng phiên bản):

```powershell
Get-FileHash .\BiosMaster.exe -Algorithm SHA256
```

## Giấy phép

| | |
|---|---|
| **Mua một lần, dùng vĩnh viễn** | Không có hạn sử dụng. Mua xong dùng mãi bản đã nhận. |
| **1 mã = 1 máy** | Cần dùng nhiều máy thì mỗi máy một mã. |
| **Cập nhật miễn phí 1 năm** | Mọi bản phát hành trong 1 năm kể từ ngày mua đều được nhận miễn phí. |
| **Gia hạn cập nhật theo năm** | Hết thời hạn cập nhật bạn **vẫn dùng mãi bản đã có**. Muốn nâng cấp lên bản mới hơn thì mua gia hạn theo năm (xem bên dưới). |
| **Dùng khi mất mạng** | Sau khi kích hoạt, app tự xác nhận giấy phép ngầm mỗi khi mở và mỗi vài giờ. Mất mạng tối đa 14 ngày vẫn dùng bình thường; quá hạn đó chỉ cần nối mạng một lần. |

### Cập nhật và gia hạn

- **Trong thời hạn cập nhật:** app tự báo khi có bản mới; bấm số phiên bản ở góc trên bên trái thanh bên để kiểm tra (khi đang dùng bản mới nhất, hộp thoại ghi kèm **ngày hết hạn cập nhật** của bạn). Có bản mới thì bấm *Tải về*: app tự đóng, thay file rồi mở lại.
- **Hết thời hạn cập nhật:** bản đã có chạy bình thường, không mất gì. Khi có bản mới hơn, app báo bản đó nằm ngoài thời hạn của bạn và **không mời tải**.
- **Muốn nâng cấp sau khi hết hạn:** liên hệ người bán để **gia hạn thêm theo năm**. Mỗi lần gia hạn cộng thêm 1 năm (tính từ ngày hết hạn nếu còn hạn, hoặc từ ngày gia hạn nếu đã hết). Bạn **giữ nguyên mã kích hoạt**, không cần mua lại hay cài lại; sau khi người bán gia hạn, mở app, bấm số phiên bản để nhận bản mới.

### Đổi máy, cài lại Windows

| Tình huống | Cách làm |
|---|---|
| **Cài lại Windows, đổi ổ đĩa, thay CPU** | App tự nhận ra đúng máy đó. Nếu hỏi lại mã, nhập là xong; **không tốn lượt chuyển máy**. |
| **Chuyển sang máy khác** (đổi máy, đổi bo mạch chủ) | Mở app trên máy mới, nhập mã, bấm **CHUYỂN SANG MÁY NÀY**. Tối đa **3 lần mỗi năm**; máy cũ ngừng dùng được. Hết lượt thì liên hệ người bán. |
| **Quên hoặc mất mã** | Liên hệ người bán để được gửi lại. |

> **Mã kích hoạt là bí mật của bạn.** Không đăng công khai hay gửi người khác: ai có mã đều kích hoạt được. Giấy phép bị chia sẻ trái phép có thể bị thu hồi.

## Quyền riêng tư

Khi kích hoạt và xác nhận giấy phép, phần mềm gửi tới máy chủ bản quyền: mã kích hoạt, **mã băm một chiều** của một vài đặc điểm máy (không đảo ngược được, không gồm số serial hay tên máy), phiên bản phần mềm, và máy chủ ghi nhận địa chỉ IP. **Không gửi** file BIOS, file của bạn hay kết quả phân tích. Công cụ ngoài được tải trực tiếp từ nguồn của tác giả, không qua máy chủ của chúng tôi.

## Xử lý sự cố

| Hiện tượng | Cách xử lý |
|---|---|
| Windows SmartScreen hoặc phần mềm diệt virus cảnh báo | File chưa có chữ ký số của nhà phát hành. So SHA-256 như hướng dẫn trên; khớp thì có thể chọn *More info → Run anyway*. Nếu bị chặn nhầm, liên hệ người bán. |
| "Mã không đúng hoặc không có trong hệ thống" | Mã không phân biệt hoa thường. Kiểm tra từng ký tự (O/0, I/L/1 được tự sửa). Nhập sai nhiều lần liên tiếp sẽ bị chặn tạm vài phút. |
| "Mã này đang dùng trên một máy khác" | Bấm **CHUYỂN SANG MÁY NÀY** nếu bạn là chủ mã và đổi máy. |
| "Không kết nối được máy chủ bản quyền" | Kiểm tra mạng, tường lửa hoặc proxy rồi thử lại. |
| "Bản này phát hành sau thời hạn cập nhật" | Bạn đang mở bản mới hơn thời hạn cập nhật của mình. Dùng bản cũ hơn, hoặc gia hạn cập nhật. |
| Một chức năng báo thiếu công cụ | Chọn *Tải về* khi app hỏi; cần có mạng lần đầu. |

Khi cần hỗ trợ, gửi kèm file nhật ký: `%LOCALAPPDATA%\BiosMaster\biosmaster.log`.

## Lưu ý quan trọng

Các thao tác vá và sửa firmware có thể khiến máy **không khởi động được**. Luôn sao lưu file BIOS gốc trước khi ghi, chỉ thao tác trên máy bạn có quyền xử lý và hiểu rủi ro. Phần mềm được cung cấp để phục vụ kỹ thuật viên; người dùng tự chịu trách nhiệm về cách sử dụng.

## Mua hàng và hỗ trợ

Mua mã kích hoạt, gia hạn cập nhật theo năm, đổi máy quá lượt hoặc cần hỗ trợ: liên hệ người bán qua kênh bạn đã dùng để mua phần mềm.

---

© BIOS Master. Mọi quyền được bảo lưu. Đây là phần mềm thương mại; kho này dùng để phân phối các bản phát hành.
