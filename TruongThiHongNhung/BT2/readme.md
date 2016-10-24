- Bài toán: Kiểm tra năm nhuận
- Mô tả bài toán: Năm nhuận là năm chia hết cho 4 và không chia hết cho 100. Hoặc năm chia hết cho 400.
- Hàm cần kiểm thử:
  public class App {
    public int getNumber(int year) {
        int result = -1;

        if (year < 0) {
            return result;
        }

        result = 0;
        if (year % 4 == 0 && year % 100 != 0
                || year % 400 == 0) {
            while (year != 0) {
                result = result * 10 + year % 10;
                year /= 10;
            }
        }
        return result;
    }
}
_Tiêu chuẩn MDCD cho điều kiện 
  if(year % 4 == 0 && year % 100 != 0
                || year % 400 == 0)
  Kết quả: T | T | F | T T | T | T | T F | T | F | T F | T | T | F
_Độ bao phủ câu lệnh: 89%
