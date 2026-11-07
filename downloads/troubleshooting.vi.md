# Xử lý sự cố

## Menu không có iPhone, hoặc mục quét bị xám

1. Kiểm tra cùng Apple Account, bật Wi-Fi và Bluetooth, iPhone ở gần Mac. Giữ phím Option khi bấm nút để xem đủ menu.
2. Trong app, nhấn **Không thấy iPhone trong menu?**. Finder mở thư mục `Nhận từ iPhone`.
3. Trong thư mục đó, bấm chuột phải vào vùng trống → **Insert from iPhone** → **Scan Documents**.
4. Nhấn Lưu trên iPhone. File về thư mục này sẽ tự vào app, đúng như quét bằng nút.

Nếu vừa đổi thư mục xuất trong Cài đặt, trên bản 1.0.21 hãy lưu xong các bản quét đang chờ, rồi đóng và mở lại app để nhận file ở vị trí mới. Từ bản 1.0.22, app nhận file ở vị trí mới ngay sau khi đổi. Bấm **Không thấy iPhone trong menu?** để mở đúng thư mục nhận. Nếu còn file ở thư mục cũ, hãy chọn lô cần nhập trước khi chuyển file sang thư mục mới.

Trên bản 1.0.21, nếu máy quét luôn tạo `Scanner.pdf`, hãy đặt tên riêng cho mỗi lần quét trước khi đưa file vào thư mục nhận, chẳng hạn `Lan-1.pdf` và `Lan-2.pdf`. Điều này đặc biệt quan trọng khi lượt trước còn đang chờ **Thử lại**.

Trên bản 1.0.21, khi chép JPEG hoặc PNG từ máy quét hay ổ khác, hãy chép xong vào thư mục tạm trên cùng ổ với **Nhận từ iPhone**, rồi chuyển file hoàn chỉnh vào thư mục nhận. Nếu trang đã lưu bị xám ở cuối ảnh hoặc mất nét chữ, đối chiếu với ảnh gốc và quét lại đúng trang đó.

Bản 1.0.22 giữ JPEG hoặc PNG chưa chép xong trong **Nhận từ iPhone**. Khi việc ghi hoàn tất, app tự nhập ảnh. Nếu file vẫn nằm đó sau khi máy quét đã dừng, hãy kiểm tra bản gốc trước khi quét lại.

Nếu máy quét tạo PDF bằng cách ghi thêm từng trang, hãy đợi máy ghi xong ở thư mục tạm trên cùng ổ, mở PDF kiểm tra số trang rồi chuyển vào **Nhận từ iPhone**. Nếu máy tạm dừng sau khi ghi xong trang đầu, app có thể nhận trang đó trước khi máy ghi các trang sau. Điều này vẫn có thể xảy ra ở 1.0.22.

Từ bản 1.0.22, nếu app báo PDF cần mật khẩu, hãy thay file trong thư mục nhận bằng bản đã mở khóa, giữ nguyên tên. Sau khi nhập thành công, app tự đóng thông báo mật khẩu của file đó.

Nhật ký chẩn đoán nằm ở `~/Library/Logs/SmartDocScanner/continuity.log`. File chỉ có kiểu dữ liệu và số lượng, không có nội dung hồ sơ.

## Camera trên bàn không có hình

- **Chưa thấy iPhone:** khóa iPhone, đặt cố định gần Mac, tốt nhất cắm cáp USB. Cùng Apple Account, bật Wi-Fi và Bluetooth.
- **Chưa có quyền camera:** bật SmartDoc Scanner trong System Settings → Privacy & Security → Camera.
- **Mất hình giữa chừng:** các trang đã báo lưu vẫn an toàn. Mở khóa iPhone có thể làm camera tạm dừng; khóa lại hoặc kiểm tra cáp, app nối lại đúng thiết bị đó. App không tự đổi sang camera khác.
- **Ảnh chưa lưu được:** nút Chụp khóa lại để giữ đúng thứ tự trang. Nhấn **Thử lại**. Đóng cửa sổ thì ảnh chuyển sang thông báo đỏ ở cửa sổ chính.
- **Trang còn cả nền bàn:** đọc dòng thông báo để biết lý do, rồi nhấn **Cắt lại**, kéo bốn góc vào mép giấy. Không cần chụp lại.
- **Ảnh mờ hoặc báo ảnh thấp:** chiếu sáng đều, đưa giấy kín khung hơn, hoặc dùng Scan Documents cho GCN.

## Quét căn cước mà app xếp vào GCN

Bấm **Quét GCN** rồi quét căn cước thì trang vào mục GCN. Chọn hồ sơ, nhấn **Chuyển** để chuyển sang GT hoặc đổi chỗ hai loại. Lần sau chọn **Quét GT trước**.

## Hồ sơ không có tên

- Trên bản 1.0.21, nếu đang gõ số seri, hãy đối chiếu xong rồi bấm **Xác nhận** hoặc **Lưu tên** trước khi đổi tab GCN/GT. Đổi tab khi còn gõ có thể làm ô nhập trở về số cũ.
- Mặt ngoài GCN phải là trang đầu tiên của lượt quét. Nếu quét ngược thứ tự, nhấn **Quét lại trang** ở trang 1 hoặc nhập số seri.
- App không lấy số từ trang nội dung, vì trang đó có các mã khác.

## Hai mặt GCN khác cỡ, hoặc lô báo cần xuất lại

Từ 1.0.10 app canh trang GCN theo hình giấy. Lô đã xuất trước đó có biểu tượng mũi tên tròn, hãy **Xuất lô** lại. Nếu đã tải lên Drive, app báo trùng tên khác nội dung và không ghi đè; hãy xóa bản cũ trên Drive rồi tải lại.

Nếu trên bản 1.0.21 bạn thấy một phần dấu hoặc nét mực sát mép PDF GCN bị cắt, mở đúng trang, nhấn **Chuyển → Giữ khổ trang gốc**. So lại nét mực trong bản xem trước rồi **Xuất lô** lại. Bạn cũng có thể dùng tùy chọn này cho từng trang muốn giữ nguyên khổ.

## Không thấy nút Xuất lô, Tải lên Drive

Các nút chính nằm ở góc trên bên phải cửa sổ và chỉ có biểu tượng, gồm **Lô mới**, **Mở lô**, **Nhập dữ liệu cũ**, **Xuất lô**, **Tải lên Drive** và **Cập nhật**. Rê chuột lên biểu tượng để xem tên.

## Nhập dữ liệu cũ

- **Báo không đủ dung lượng:** phần đã nhập vẫn giữ nguyên. Giải phóng dung lượng rồi nhập lại, app tiếp tục phần còn thiếu, không tạo bản trùng.
- **Có file bị bỏ qua:** app chỉ nhận PDF mở được và ZIP đọc được. PDF có mật khẩu, PDF hỏng, file loại khác và thư mục không có PDF đều bị bỏ qua và được đếm trong thông báo.
- **Thấy tên kiểu `(bản 2)`:** file cùng tên nhưng khác nội dung với bản đã có. App giữ cả hai, bản này nằm ở nhóm **PDF rời**.
- **Thanh bên báo Chưa dùng được dữ liệu đã nhập:** thư mục thư viện có vấn đề, lô đang quét không bị ảnh hưởng. Hết lỗi thì nhấn **Nhập dữ liệu cũ** lại để thử.

## Quét lên nhầm hồ sơ

Chọn hồ sơ, dùng **Xóa trang** hoặc **Quét lại trang**.

## Bản quét chưa lưu được

App hiện thông báo đỏ phía trên và vẫn giữ bản quét. Nhấn **Thử lại**. Nếu ổ đầy, giải phóng dung lượng trước.

Từ bản 1.0.22, bấm **Thử lại** nhiều lần cũng chỉ lưu mỗi bản quét một lần. **Bỏ một bản** bỏ bản đầu tiên còn chờ. Trong lúc bản đó đang ghi xuống đĩa, nút này tạm khóa.

Nếu trang đã được sửa trong lúc chờ quét lại, app giữ trang hiện tại và đưa lượt trả về vào danh sách chờ. Với bản quét lại ở đầu danh sách, chọn **Lưu bản sao PDF…** rồi chọn một thư mục riêng trên máy, bên ngoài thư viện SmartDoc và thư mục **Nhận từ iPhone**. PDF chứa các trang của lượt quét theo đúng thứ tự. Mở bản sao để kiểm tra trước khi chọn **Bỏ một bản**.

## Tên GCN hoặc GT chưa đúng mẫu

Chọn hồ sơ, rồi chọn **Sửa tên…** trong phần xem PDF. Nếu app báo trong lô đã có file trùng tên, chưa có file nào bị đổi. Sửa số seri hoặc xử lý file đó rồi thử lại.

## Không xuất được lô

Hộp thoại nêu rõ lý do. Mở từng hồ sơ có dấu cam hoặc đỏ để xử lý. Nếu đã có lô cùng tên ở thư mục xuất, app hỏi trước khi thay; bản cũ vào Thùng rác.

Từ bản 1.0.22, nếu **Xuất lô** hoặc **Tải lên Drive** báo một trang không đọc được, chọn **Mở trang lỗi**. Ví dụ, với trang 2 của `AB 100002-GT.pdf`, app mở tab **GT** của hồ sơ **AB 100002**. Chọn **Quét lại trang 2**, rồi bấm **Quét lại** và quét riêng trang vừa báo. Sau khi sửa các trang hỏng, chọn lại **Xuất lô** hoặc **Tải lên Drive**.

Nếu đang gõ số seri ở hồ sơ khác, chọn **Đóng** để tiếp tục sửa hoặc **Bỏ nháp và mở hồ sơ** để chuyển sang trang lỗi. Nếu bạn bắt đầu tìm hồ sơ khác hoặc gõ nháp mới trong lúc app kiểm tra lại trang, app giữ phần bạn vừa nhập. Bạn có thể bấm xuất lại khi sẵn sàng.

Nếu thông báo là **Chưa ghi được** một PDF hay file ZIP của lô, hoặc **Bộ nhớ đã đầy**, trang quét không có vấn đề, nên không cần quét lại. App không thay file đã xuất trước đó. Giải phóng chỗ trống hoặc kiểm tra quyền ghi của thư mục xuất, rồi chọn lại **Xuất ngày**, **Xuất lô** hoặc **Tải lên Drive**.

Nếu **Xuất ngày** báo một file của lô đã nhập hoặc đã mở không còn là PDF đọc được, file đó đã mất, đã đổi nội dung hoặc cần mật khẩu. App không xuất cả ngày, và bản xuất trước vẫn còn nguyên. Mở lại lô, xử lý file đó rồi xuất lại.

## macOS chặn app trên máy khác

App hiện ký bằng chứng chỉ Apple Development. Trên máy khác, vào **System Settings → Privacy & Security → Open Anyway**. Muốn mở thẳng, cần Developer ID và notarize. Không cần tắt Gatekeeper.

## Không cập nhật được

- Báo không có quyền ghi: chuyển app vào Applications rồi thử lại.
- Báo gói không hợp lệ: gói bị hỏng hoặc không phải bản do bạn phát hành. App cũ vẫn giữ nguyên.
- Dữ liệu nằm ngoài app nên không bị ảnh hưởng.

## Không tải được lên Drive

- **Chưa có Google Client ID:** nhập trong Cài đặt, xem phần Kết nối Google Drive bên dưới.
- **Không có quyền ghi hoặc không thấy thư mục:** app hiện lý do, nhấn **Chọn thư mục** và chọn thư mục tài khoản này ghi được, app tự tải tiếp. Muốn dùng tài khoản khác thì đăng xuất trong Cài đặt.
- **Báo khác tài khoản khi chọn thư mục:** trang Google đang dùng tài khoản khác với tài khoản hiện trong app. Chưa có gì bị đổi, hãy chọn lại đúng tài khoản.
- **Tải lại báo trùng tên khác nội dung:** lô đã tải bằng bản 1.0.14 trở về trước, hoặc lô đã sửa, tạo PDF mới khác file trên Drive. App không ghi đè; hãy xem file nào đúng.
- **Cần đăng nhập lại:** quyền đã hết hạn. Nếu lặp lại mỗi 7 ngày, ứng dụng OAuth còn ở trạng thái Testing.
- **Mất mạng:** nhấn Thử lại, app đi tiếp từ chỗ dừng và không tạo file trùng.

## Kết nối Google Drive

Làm một lần trong Google Cloud Console:

1. Tạo project, bật **Google Drive API** và **Google Picker API**.
2. Tạo OAuth consent screen loại External, thêm tài khoản của bạn làm test user. Muốn đăng nhập không hết hạn sau 7 ngày thì Publish.
3. Tạo OAuth client loại **Desktop app**.
4. Dán Client ID vào Cài đặt của app. Client secret chỉ cần nhập nếu app báo Google yêu cầu.

Mức quyền trong Cài đặt:

| Mức | App thấy gì | Đánh đổi |
| --- | --- | --- |
| Tối thiểu (mặc định) | Thư mục bạn chọn trong Google Picker và file app tạo | Có thể không thấy file đồng nghiệp tải lên, nên có thể không phát hiện được trùng với họ |
| Toàn bộ Drive | Mọi file của tài khoản | So trùng được với đồng nghiệp, nhưng cấp quyền rộng hơn nhiều |

## Ở đâu lưu gì

| Dữ liệu | Vị trí |
| --- | --- |
| Lô đang làm | `~/Library/Application Support/SmartDocScanner/Batches` |
| Dữ liệu cũ đã nhập | `~/Library/Application Support/SmartDocScanner/Imported` |
| Lô đã xuất | `~/Documents/SmartDoc` |
| PDF đã tải lên Drive, giữ để tải lại không trùng | Trong thư mục của lô, xóa cùng lô |
| Thư mục Drive đang nhớ, tài khoản | Cài đặt của app |
| Thư mục nhận từ Finder | Thư mục con `Nhận từ iPhone` tại vị trí xuất đã chọn. Mặc định là `~/Documents/SmartDoc/Nhận từ iPhone` |
| Nhật ký chẩn đoán | `~/Library/Logs/SmartDocScanner` |
| Phiên tải lên dở | `~/Library/Application Support/SmartDocScanner/Drive` |
| Quyền đăng nhập Google | Keychain |

Thư mục lô đang làm và dữ liệu đã nhập không vào Time Machine. Hãy giữ bản gốc của dữ liệu cũ.
