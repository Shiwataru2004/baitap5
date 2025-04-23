# baitap5
baitap5_NguyenGiangLong_K225480106043_HQTCSDL


BÀI TẬP VỀ NHÀ 05, Môn Hệ quản trị csdl.

**SUBJECT: Trigger on mssql**

**A. Trình bày lại đầu bài của đồ án PT&TKHT:**
1. Mô tả bài toán của đồ án PT&TKHT, 
   đưa ra yêu cầu của bài toán đó
2. Cơ sở dữ liệu của Đồ án PT&TKHT :
   Có database với các bảng dữ liệu cần thiết (3nf),
   Các bảng này đã có PK, FK, CK cần thiết
 
**B. Nội dung Bài tập 05:**
1. Dựa trên cơ sở là csdl của Đồ án
2. Tìm cách bổ xung thêm 1 (hoặc vài) trường phi chuẩn
   (là trường tính toán đc, nhưng thêm vào thì ok hơn,
    ok hơn theo 1 logic nào đó, vd ok hơn về speed)
   => Nêu rõ logic này!
3. Viết trigger cho 1 bảng nào đó, 
   mà có sử dụng trường phi chuẩn này,
   nhằm đạt được 1 vài mục tiêu nào đó.
   => Nêu rõ các mục tiêu 
4. Nhập dữ liệu có kiểm soát, 
   nhằm để test sự hiệu quả của việc trigger auto run.
5. Kết luận về Trigger đã giúp gì cho đồ án của em.
# Bài làm:
A. Trình bày đầu bài của đồ án PT&TKHT:
1 . Yêu cầu đồ án: Phân tích thiết kế phần mềm quản lý chi tiêu cá nhân
2 . Với những yêu cầu cần thiết về bài tập, em tạo các bảng như sau 
- Bảng Quản lý thu:

  ![image](https://github.com/user-attachments/assets/7dda544b-938a-437d-88da-d0e1f63eb699)

- Bảng Quản Lý chi:

  ![image](https://github.com/user-attachments/assets/6cd327a7-78e9-4db0-94f7-4fa5beaa2e48)

- Bảng Tài Khoản:

  ![image](https://github.com/user-attachments/assets/6847d925-3e08-4e05-a16b-103a361af0f1)

Tạo khóa ngoại liên kết cho bảng: 

![image](https://github.com/user-attachments/assets/c53d8380-5bf8-4472-92ce-ac1f9ebeafdd)

![image](https://github.com/user-attachments/assets/8b524501-d5bd-4209-b963-ac44b8f687b9)

B.Nội dung Bài tập 05:
Dựa trên CSDL của đồ án, bầy giờ em cần phải set trigger để tự dộng cập nhật số dư (Tong Tien)
Viết trigger cho các bảng để đạt được mục tiêu:
   - Bấm dấu "+" vào bảng và chuột phải vào Triggers ---> new trigger

![image](https://github.com/user-attachments/assets/e3041cfe-8314-452f-9bfc-4417cbe0ca33)

Trigger thêm chi:

![image](https://github.com/user-attachments/assets/c2e55275-ca63-4e72-8025-42ea54f8dd80)

Trigger thêm thu:

![image](https://github.com/user-attachments/assets/1255ce65-ecc6-4812-9491-a747a179ebb3)

Trigger cho QLChi
+Thêm chi(Giảm Tiền):

![image](https://github.com/user-attachments/assets/88273131-524c-4fef-8e51-27bf6225bb95)

+Xóa chi(Hoàn tiền):

![image](https://github.com/user-attachments/assets/5bfb1dcf-7b3b-4436-8e51-6f7763627dda)

+Sửa chi(Điều chỉnh):

![image](https://github.com/user-attachments/assets/daaf6f51-9861-44bc-85a6-2040937bba68)

Trigger cho QLThu:
+Thêm Thu(tăng tiền):

![image](https://github.com/user-attachments/assets/742fd3a4-fedb-4ef1-9b4a-a9310210d0fb)

+Xóa thu(Giảm tiền):

![image](https://github.com/user-attachments/assets/1ef3719f-c820-4489-b353-730ad75b66f2)

+Sửa thu(Điều Chỉnh):

![image](https://github.com/user-attachments/assets/49232afa-5608-4c06-98e5-72bd16dae606)

Test trigger:
Ban đầu:
![image](https://github.com/user-attachments/assets/a2ef8e24-199c-45b5-a111-6df927bb3347)

Sau chi:
![image](https://github.com/user-attachments/assets/611d0236-6d0e-415d-abbf-d9a2ce0351eb)

Kết quả:
![image](https://github.com/user-attachments/assets/485fe78a-7ff2-4e88-a245-1997d37fca0d)
(Em buồn ngủ nên e xin phép demo 1 ex thôi ạ :>)

KẾT LUẬN: Những Trigger trên đã giúp em hoàn thành bài tập được giao,  ngăn chặn việc cố gắng chèn thêm những dữ liệu phi chuẩn vào bảng và tự động cập nhật dữ liệu 1 cách logic từ các bảng có liên kết khi dữ liệu của 1 hoặc nhiều trong các bảng bị thay đổi.
