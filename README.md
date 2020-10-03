# INT3401_8 Pacman_01_Search
# Thái Phi Hoàng _ 18020019

1. **Q1: DFS**:
   Tạo stack, duyệt qua từng phần tử của stack, sau đó cứ mỗi phần tử lại lấy phần tử chưa duyệt qua cho vào stack, duyệt cho đến khi stack rỗng qua mỗi lần duyệt công kết quả với hướng của cái tiếp theo, nếu lúc duyệt có 1 phần tử là điểm kết thúc thì trả về mảng các hướng
2. **Q2: BFS**:
   Tương tự bài 1, thay stack bằng queue
3. **Q3: UCS**:
   Tương tự 2 bài trên,thay bằng hàng đợi ưu tiên
4. **Q4: Astar**:
   Tương tự bài 3, thêm xét độ ưu tiên là khoảng cách lấy từ nullHeuristic
5. **Q5: FInding All the Corners**:
   Tạo 1 trạng thái đã đi qua 4 điểm góc chưa, truyền cho giá trị trả về của từng điểm (sau khi dùng getSuccessor hoặc getStartState) Ở hàm getSuccessor chúng ta dựa vào trạng thái của 4 góc và từ đó tính toán cho 4 hướng đi của nó, trả về dạng như trên. Xét kết thúc khi 4 góc là true (đã đi qua)
6. **Q6: Corners Problem: Heuristic**:
Ta chỉ cần tạo 1 mảng lưu khoảng cách manhattan từ ví trí hiện tại đến những góc chưa đi qua. Rồi trả về giá trị lớn nhất của mảng để ước lượng.
7. **Q7: Eating All the Dots**:
   Giống như bài trước chỉ cần trả về 1 giá trị cụ thể. Và đích trong vài này là ăn hết đồ ăn trong mê cung. Em dùng hàm mazeDistance để do khoảng cách giữa 2 điểm trong trạng thái bất kì của mê cung (thời gian lâu nhưng số node duyệt ngắn hơn). Lưu chúng lại thàng mảng rồi trả về giá trị lớn nhất.
8. **Q8: Suboptimal Search**:
   Ở bài này đề muốn ta ăn hết những dot trên ma trận, do đó chúng ta thiết lập đích đến cho từng lần tìm kiếm là từng dot trên ma trận, mỗi lần thuật toán findPathClosetDot sẽ tìm đường đến điểm đó, vì thế để tìm nhanh nhất chúng ta sẽ dùng A* cho hàm này để tiết kiệm về mặt thời gian và đồng thời đi đến điểm gần nhất (đáp ứng yêu cầu phản xạ nhanh của bài toán)
