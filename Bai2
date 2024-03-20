#include <stdio.h>
#include <math.h>

// Hàm kiểm tra xem một số có phải là số chính phương hay không
int isPerfectSquare(int num) {
    int squareRoot = sqrt(num);
    return (squareRoot * squareRoot == num);
}

// Hàm đếm số lượng số chính phương nhỏ hơn n và in ra chúng
void countAndPrintPerfectSquares(int n) {
    int count = 0;
    printf("Cac so chinh phuong nho hon %d la:\n", n);
    for (int i = 1; i < n; i++) {
        if (isPerfectSquare(i)) {
            printf("%d ", i);
            count++;
        }
    }
    printf("\nTong so chinh phuong: %d\n", count);
}

// Hàm main để thực thi chương trình
int main() {
    int n;
    printf("Nhap vao so nguyen duong n: ");
    scanf("%d", &n);
    countAndPrintPerfectSquares(n);
    return 0;
}
