## 1. Đại số tuyến tính (Linear Algebra)

- **Vector & Ma trận (Matrix):**
  - **Bản chất:** Vector là một điểm trong không gian dữ liệu nhiều chiều. Ma trận là một "hàm số" hoặc "phép biến đổi" làm thay đổi (kéo giãn, xoay) không gian chứa vector đó.
  - **Kỹ thuật Feynman:** Tưởng tượng không gian là một tấm lưới cao su. Một vector là một mũi tên vẽ trên tấm lưới. Phép nhân ma trận chính là hành động bạn dùng tay kéo giãn hoặc xoay tấm lưới đó, làm mũi tên bị biến dạng theo.
- **Trị riêng & Vector riêng (Eigenvalues & Eigenvectors):**
  - **Bản chất:** Khi nhân một ma trận (kéo giãn tấm lưới), hầu hết các vector đều bị đổi hướng. Những vector hiếm hoi CHỈ bị thay đổi độ dài (không đổi hướng) gọi là Vector riêng. Độ dài bị thay đổi bao nhiêu lần chính là Trị riêng.
  - **Kỹ thuật Feynman:** Giống như một chiếc đĩa CD đang quay. Hầu hết các điểm trên đĩa đều thay đổi vị trí không ngừng. Nhưng trục ở giữa đĩa chỉ quay tại chỗ (không đổi hướng) - đó là Vector riêng.
- **SVD (Singular Value Decomposition):**
  - **Bản chất:** Phân rã một ma trận dữ liệu khổng lồ thành 3 ma trận nhỏ hơn, trích xuất ra các "đặc trưng ẩn" quan trọng nhất. Đây là cốt lõi của hệ thống gợi ý và giảm chiều dữ liệu.

## 2. Giải tích (Calculus)

- **Đạo hàm riêng (Partial Derivative) & Gradient:**
  - **Bản chất:** Đạo hàm riêng đo tốc độ thay đổi của hàm số khi chỉ thay đổi 1 biến (giữ nguyên các biến khác). Gradient là một vector gom tất cả các đạo hàm riêng lại, luôn chỉ về hướng hàm số tăng dốc nhất.
  - **Kỹ thuật Feynman:** Bạn đứng trên một sườn núi nhấp nhô (Hàm mất mát). Đạo hàm riêng theo trục x là độ dốc nếu bạn chỉ bước sang trái/phải. Gradient là mũi tên la bàn chỉ trực tiếp lên đỉnh núi dốc nhất. Đi ngược chiều mũi tên đó là Gradient Descent (đi xuống đáy thung lũng).

## 3. Xác suất Thống kê (Probability & Statistics)

- **Định lý Bayes (Bayes' Theorem):**
  - **Bản chất:** Cập nhật niềm tin (xác suất) của bạn về một giả thuyết khi có thêm bằng chứng mới.
  - **Kỹ thuật Feynman:** Bạn đoán trời hôm nay 10% sẽ mưa (Niềm tin ban đầu). Đột nhiên bạn thấy mây đen kéo đến (Bằng chứng). Bạn dùng công thức Bayes để tính lại xác suất mưa bây giờ lên tới 80% (Niềm tin được cập nhật).

## 4. Tối ưu hóa (Optimization)

- **Hàm mục tiêu & Ràng buộc (Objective Function & Constraints):**
  - **Bản chất:** Mô hình hóa một bài toán thực tế thành toán học. Tìm giá trị lớn nhất/nhỏ nhất của hàm mục tiêu trong ranh giới cho phép của các ràng buộc.
  - **Kỹ thuật Feynman:** Tối đa hóa niềm vui khi đi du lịch (Hàm mục tiêu) nhưng bị giới hạn bởi số ngày nghỉ phép và ngân sách tài khoản (Các ràng buộc).

---

<a id="cheat-sheet"></a>

### 1. Đại số tuyến tính:

- **Tích vô hướng (Dot Product):** Đo lường mức độ tương đồng giữa 2 vector.
  $$\vec{u} \cdot \vec{v} = \sum_{i=1}^{n} u_i v_i = \|\vec{u}\| \|\vec{v}\| \cos(\theta)$$
  _(Quy tắc: Nếu 2 vector vuông góc, tích vô hướng = 0. Nếu cùng hướng, đạt giá trị lớn nhất)._
- **Norm (Chuẩn Vector - L1, L2):** Dùng trong Regularization (L1: Lasso, L2: Ridge).
  $$L1: \|\vec{x}\|_1 = \sum_{i=1}^{n} |x_i| \quad \quad L2: \|\vec{x}\|_2 = \sqrt{\sum_{i=1}^{n} x_i^2}$$
- **Phân rã SVD:** $A = U \Sigma V^T$
- **Định thức Ma trận $2 \times 2$:** $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \rightarrow \det(A) = ad - bc$. Nếu $\det(A) = 0$, ma trận không nghịch đảo được.

### 2. Giải tích & Tối ưu:

- **Quy tắc chuỗi (Chain Rule):** $\frac{\partial z}{\partial x} = \frac{\partial z}{\partial y} \cdot \frac{\partial y}{\partial x}$
- **Cập nhật Gradient Descent:** $w_{t+1} = w_t - \alpha \nabla J(w_t)$
- **Hàm Sigmoid:** $\sigma(x) = \frac{1}{1 + e^{-x}}$

### 3. Xác suất Thống kê:

- **Định lý Bayes:** $P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$
- **Kỳ vọng & Phương sai:** $E[X] = \sum x_i P(x_i) \quad \quad Var(X) = E[X^2] - (E[X])^2$
- **Phân phối Chuẩn (Gaussian):** $f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}$
