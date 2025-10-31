# BTH3_ubuntu
ubuntu

#!/bin/bash
# =====================================
# BÀI TẬP THỰC HÀNH CNMM3 – HỆ THỐNG TẬP TIN
# Sinh viên: [Tên của bạn]
# =====================================

echo "=== BẮT ĐẦU BÀI THỰC HÀNH CNMM3 ==="

# 1. Tạo cây thư mục
cd ~
mkdir -p tailieu/giaotrinh tailieu/baigiang \
phanmem/laptrinh/{common,Java,php,shellscript} \
phanmem/tienich

# 2. Tạo file modau
echo "Gioi thieu mon hoc" > tailieu/baigiang/modau

# 3. Sao chép & đổi tên
cp tailieu/baigiang/modau tailieu/giaotrinh/gioithieu.sh

# 4. Thêm nội dung cuối file
echo "Cong nghe ma nguon mo" >> tailieu/giaotrinh/gioithieu.sh

# 5. Tạo file shell1 trong shellscript
echo "Bai thuc hanh shell dau tien" > phanmem/laptrinh/shellscript/shell1

# 6. Quyền đọc + ghi cho user, đọc cho group/others
chmod 644 tailieu/giaotrinh/gioithieu.sh

# 7. Quyền đọc+ghi+thực thi cho user, đọc+thực thi cho group/others
chmod 755 phanmem/laptrinh/shellscript/shell1

# 8. Di chuyển file
mv tailieu/giaotrinh/gioithieu.sh phanmem/laptrinh/shellscript/

# 9. Xóa thư mục baigiang
rm -r tailieu/baigiang

# 10. Xóa file gioithieu.sh
rm phanmem/laptrinh/shellscript/gioithieu.sh

# 11. Hard link
ln phanmem/laptrinh/shellscript/shell1 phanmem/hlkgioithieu

# 12. Thêm dòng vào hard link
echo "He dieu hanh Linux" >> phanmem/hlkgioithieu

# 13. Kiểm tra nội dung file shell1
echo "--- Nội dung shell1 ---"
cat phanmem/laptrinh/shellscript/shell1

# 14. Tạo symbolic link
ln -s phanmem/laptrinh/shellscript/shell1 phanmem/slkshell

# 15. Xem nội dung symbolic link
echo "--- Nội dung symbolic link ---"
cat phanmem/slkshell

16.xem file

# 17. Liệt kê thư mục /etc vào file thongke
ls /etc > phanmem/laptrinh/common/thongke

# 18. Xem theo trang
echo "--- Xem thongke (trang đầu) ---"
head -n 10 phanmem/laptrinh/common/thongke

# 19. Xem 5 dòng đầu tiên
echo "--- 5 dòng đầu ---"
head -n 5 phanmem/laptrinh/common/thongke

# 20. Xem 5 dòng cuối cùng
echo "--- 5 dòng cuối ---"
tail -n 5 phanmem/laptrinh/common/thongke

# 21. Thiết lập quyền tập tin thongke
chmod 644 phanmem/laptrinh/common/thongke

# 22. Thiết lập quyền thư mục common
chmod 755 phanmem/laptrinh/common

echo "=== HOÀN THÀNH BÀI THỰC HÀNH ==="
