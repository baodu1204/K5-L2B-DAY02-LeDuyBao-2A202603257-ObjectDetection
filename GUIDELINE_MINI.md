# Mini guideline — bài làm cá nhân

> Điền nội dung này trước khi bắt đầu gán nhãn. Giữ lại các quyết định sau khi self-QC.

## Định nghĩa lớp

| Lớp | Định nghĩa của bạn | Ví dụ/điểm phân biệt |
| --- | --- | --- |
| `car` | Xe con thông thường: sedan, hatchback, SUV, taxi, xe bán tải/cabin nhỏ nếu không rõ là tải hoặc bus. | Nếu thân xe nhỏ gọn, có 2-5 chỗ ngồi hoặc là xe gia đình/xe cá nhân, chọn `car`; không dùng cho xe buýt, xe tải, van chở hàng. |
| `truck` | Xe tải chở hàng, xe tải thùng, xe đầu kéo hoặc phương tiện có thùng/tải rõ ràng. | Nếu phần phía sau có thùng hàng, cabin lớn hoặc hình dạng tải chở hàng rõ rệt, chọn `truck`; khác với `car` và `van` vì có cấu trúc chuyên dụng cho hàng hóa. |
| `bus` | Xe buýt/coach/minibus chở khách lớn. | Xe dài hơn, nhiều cửa, phần thân lớn và kiểu dáng chở khách; phân biệt với `van` bằng kích thước và mục đích chở khách tập trung. |
| `van` | Xe van/minivan chở hàng hoặc chở người nhỏ-vừa. | Xe thân cao, hình hộp, có thể mang hàng hoặc khách nhưng nhỏ hơn bus; không phải xe con thông thường và không phải xe tải rõ ràng. |

## Quy tắc chung

- Box bám sát vật thể nghĩa là: ôm sát phần thân xe nhìn thấy được, không lấy thêm mặt đường, mép trời, cột điện, biển báo, khoảng trống xung quanh; chỉ giữ vùng thực sự là xe.
- Vật thể bị che khuất: nếu phần xe còn nhìn thấy đủ để nhận diện lớp và vị trí, vẫn gán box; nếu chỉ còn mảnh quá nhỏ hoặc không đủ thông tin để xác định lớp, không đoán và bỏ qua.
- Vật thể bị cắt bởi rìa ảnh: gán box đến biên ảnh, nhưng không đoán phần xe nằm ngoài khung; chỉ lấy phần còn thấy và giữ bám sát thân xe.
- Vật thể rất nhỏ/mơ hồ: nếu quá nhỏ, mờ, hoặc không thể chắc chắn lớp, bỏ qua; không tự suy đoán từ kích thước hoặc màu sắc để chọn `car`/`van`/`truck` khi không đủ bằng chứng.

## Ghi lại quyết định cho ít nhất ba ca mơ hồ

| Ảnh | Tình huống | Quyết định cuối | Lý do theo schema |
| --- | --- | --- | --- |
| `drive_012` | Xe có thân cao, hình hộp, bị mờ ở phía sau nhưng vẫn nhìn rõ phần cabin và thân chính | `van` | Dạng van/minivan chở hàng/chở người; hình dáng cao và dài hơn xe con nhưng nhỏ hơn xe buýt, nên không chọn `bus` hay `car`. |
| `drive_031` | Xe buýt lớn xuất hiện ở góc xa, cắt một phần bởi khung ảnh | `bus` | Tỷ lệ chiều dài/chiều cao và hình dạng chở khách nổi bật; dù bị cắt khung, phần còn thấy đủ để xác định là xe buýt, nên giữ box đến biên ảnh. |
| `drive_028` | Xe minivan có cửa sổ và thân cao, nằm trên lề góc trái cạnh một sedan | `car` | Mục tiêu là phân loại theo loại phương tiện, không phải trạng thái; thân cao và hình hộp hơn `car`, nên chọn `van` thay vì `car`. |

## Ghi chú cá nhân

- Mỗi box phải là một vật thể riêng; nếu có hai xe chồng lấn hoặc đứng sát nhau, vẽ hai box riêng nếu có thể phân biệt được.
- Không gán người đi bộ, xe máy, biển báo, đèn tín hiệu, phản chiếu trong kính hay hình ảnh quảng cáo trên tường.
- Sau khi hoàn thành self-QC, giữ nguyên các quyết định trên và chỉ điều chỉnh khi có bằng chứng rõ ràng từ ảnh hoặc feedback từ gold set.
