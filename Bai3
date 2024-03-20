from _anvil_designer import Form1Template
from anvil import *

class Form1(Form1Template):
    def __init__(self, **properties):
        # Set Form properties and Data Bindings.
        self.init_components(**properties)

    def merge_sort(self, arr):
        if len(arr) > 1:
            mid = len(arr) // 2
            left_half = arr[:mid]
            right_half = arr[mid:]

            self.merge_sort(left_half)
            self.merge_sort(right_half)

            i = j = k = 0

            while i < len(left_half) and j < len(right_half):
                if left_half[i] < right_half[j]:
                    arr[k] = left_half[i]
                    i += 1
                else:
                    arr[k] = right_half[j]
                    j += 1
                k += 1

            while i < len(left_half):
                arr[k] = left_half[i]
                i += 1
                k += 1

            while j < len(right_half):
                arr[k] = right_half[j]
                j += 1
                k += 1

    def Xep_click(self, **event_args):
        try:
            # Nhập dãy số nguyên từ người dùng và chuyển đổi thành list
            arr = [int(num.strip()) for num in self.NhapN.text.split(',')]

            # Thực hiện sắp xếp dãy số nguyên bằng thuật toán Merge Sort
            self.merge_sort(arr)

            # Hiển thị kết quả sắp xếp
            self.Ketqua.text = ', '.join(map(str, arr))
        except ValueError:
            # Xử lý nếu người dùng nhập không đúng định dạng số nguyên
            self.Ketqua.text = "Vui lòng nhập các số nguyên cách nhau bằng dấu phẩy"

    def NhapN_pressed_enter(self, **event_args):
        # Gọi sự kiện khi người dùng nhấn Enter trong ô nhập dãy số nguyên
        self.Xep_click()

    def Ketqua_pressed_enter(self, **event_args):
        # Gọi sự kiện khi người dùng nhấn Enter trong ô kết quả
        self.Xep_click()
