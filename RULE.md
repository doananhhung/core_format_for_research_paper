# QUY TẮC TRÌNH BÀY TÀI LIỆU SEMINAR

## 1. Cấu trúc Trình bày Mỗi Mục (Section)

### 1.1. Yêu cầu Bắt buộc

Sau khi viết **tiêu đề mục chính** (ví dụ: `\section{Giới thiệu}`), **BẮT BUỘC** phải có một đoạn văn giới thiệu tổng quan trước khi đi vào các mục con (`\subsection`).

### 1.2. Nội dung Đoạn Giới thiệu

Đoạn giới thiệu này phải bao gồm **ba thành phần** sau:

1. **Giải thích tóm tắt mục đích của mục**
   - Mục này sẽ làm gì?
   - Tại sao mục này quan trọng trong bối cảnh tài liệu?

2. **Tóm tắt nội dung trong mục**
   - Mục này bao gồm những phần nào?
   - Các khái niệm/chủ đề chính được đề cập?

3. **Tích hợp trích dẫn ngay lập tức**
   - Trích dẫn ngay sau câu hoặc mệnh đề chứa thông tin tham khảo
   - **KHÔNG** dồn tất cả trích dẫn xuống cuối đoạn văn
   - Ví dụ: "...theo nghiên cứu của A [1], trong khi B đề xuất [2]..."

### 1.3. Ví dụ Minh họa

#### ❌ **SAI** (Thiếu đoạn giới thiệu):
```latex
\section{Giới thiệu}

\subsection{Tổng quan về single-leader-multi-follower games}
Trò chơi phân cấp mô tả các tình huống ra quyết định...
```

#### ✅ **ĐÚNG** (Có đoạn giới thiệu đầy đủ):
```latex
\section{Giới thiệu}

Mục này cung cấp nền tảng lý thuyết cho bài nghiên cứu [3], giới thiệu về mô hình 
single-leader-multi-follower games (SLMF) và các khái niệm liên quan. Nội dung 
bao gồm tổng quan về lý thuyết trò chơi phân cấp [9], cấu trúc cơ bản của SLMF, 
và các phương pháp giải Nash equilibrium [15].

\subsection{Tổng quan về single-leader-multi-follower games}
Trò chơi phân cấp mô tả các tình huống ra quyết định...
```

---

## 2. Mục đích của Quy tắc

- **Tăng tính mạch lạc**: Người đọc hiểu được bức tranh tổng thể trước khi đi vào chi tiết
- **Minh bạch nguồn tài liệu**: Rõ ràng về nguồn tham khảo ngay từ đầu mỗi mục
- **Cấu trúc học thuật**: Tuân theo chuẩn mực trình bày khoa học chuyên nghiệp

---

## 3. Checklist Tự Kiểm tra

Trước khi hoàn thiện một mục, kiểm tra:

- [ ] Đã có đoạn văn giới thiệu sau tiêu đề mục chính?
- [ ] Đoạn giới thiệu có giải thích **mục đích** của mục?
- [ ] Đoạn giới thiệu có tóm tắt **nội dung** của mục?
- [ ] Đoạn giới thiệu có liệt kê **các trích dẫn** được sử dụng?
- [ ] Đoạn giới thiệu có độ dài phù hợp (1-2 đoạn văn)?

---

## 4. Lưu ý Bổ sung

- Đoạn giới thiệu **không cần quá dài**, chỉ cần súc tích và đầy đủ thông tin
- Nếu mục có nhiều subsection, nên **liệt kê rõ ràng** các subsection trong phần tóm tắt nội dung
- Trích dẫn cần đặt **chính xác** sau thông tin được tham khảo (không đợi hết câu nếu thông tin nằm giữa câu)

---

## 5. Quy tắc Trích dẫn

### 5.1. Nguyên tắc Chung

Khi liệt kê nhiều tài liệu tham khảo, sử dụng **một lệnh `\cite{}` duy nhất** với các keys cách nhau bởi dấu phẩy.

### 5.2. Cách Thực hiện

```latex
✅ ĐÚNG:
\cite{ref1, ref2, ref3, ref4}
% Kết quả: [2, 3, 4, 7] hoặc [2-4, 7] tùy theo style
```

```latex
❌ SAI (Viết tách riêng):
\cite{ref1}\cite{ref2}\cite{ref3}\cite{ref4}
% Kết quả: [2][3][4][7] (tách rời không đẹp)
```

### 5.3. Ví dụ Đầy đủ

```latex
Các tài liệu tham khảo chính được sử dụng trong chương này là 
\cite{MultiLeaderFollowerSurvey, BilevelPolymatrix2020, SolvingMultiFollower2023, CardinalitySLMF2025}.
```

**Kết quả:** `[2, 3, 4, 5]` hoặc `[2-5]` (tùy theo citation style được cấu hình)

### 5.4. Lưu ý

- Citation style (compressed hay expanded) phụ thuộc vào package và options được sử dụng (ví dụ: `natbib`, `biblatex`)
- Nếu muốn hiển thị đầy đủ (không nén), cấu hình trong preamble thay vì viết tách

---

**Ngày cập nhật**: 2026-02-02  
**Lý do**: Đơn giản hóa cách viết citation, tuân theo chuẩn LaTeX thông thường  
**Áp dụng cho**: Tất cả các trích dẫn trong tài liệu

---

## 6. Quy tắc Dấu Câu cho Công thức Toán học

### 6.1. Nguyên tắc Chung

Công thức toán học (equations) là **một phần của câu văn**, do đó **BẮT BUỘC** phải có dấu câu phù hợp sau mỗi công thức.

### 6.2. Quy định Cụ thể

- **Nếu câu chưa kết thúc** sau công thức → Dùng **dấu phẩy (,)**
- **Nếu câu kết thúc** sau công thức → Dùng **dấu chấm (.)**

### 6.3. Ví dụ Minh họa

#### ❌ **SAI** (Không có dấu câu):
```latex
Hàm mục tiêu của leader được định nghĩa là
\begin{equation}
    \max_{x_L} f_L(x_L, x_F)
\end{equation}
trong đó $x_L$ là biến quyết định của leader
```

#### ✅ **ĐÚNG** (Có dấu phẩy - câu chưa kết thúc):
```latex
Hàm mục tiêu của leader được định nghĩa là
\begin{equation}
    \max_{x_L} f_L(x_L, x_F),
\end{equation}
trong đó $x_L$ là biến quyết định của leader.
```

#### ✅ **ĐÚNG** (Có dấu chấm - câu kết thúc):
```latex
Nash equilibrium được xác định bởi điều kiện
\begin{equation}
    \nabla f_i(x_i^*, x_{-i}^*) = 0, \quad \forall i.
\end{equation}
```

### 6.4. Lưu ý Kỹ thuật

- Dấu câu được đặt **trước** lệnh `\end{equation}` hoặc `\end{align}`
- Áp dụng cho tất cả loại môi trường toán: `equation`, `align`, `gather`, `multline`, v.v.
- Công thức inline (`$...$`) cũng cần tuân thủ quy tắc này

### 6.5. Checklist

- [ ] Mọi công thức đều có dấu câu (phẩy hoặc chấm)?
- [ ] Dấu phẩy được dùng khi câu tiếp tục sau công thức?
- [ ] Dấu chấm được dùng khi câu kết thúc sau công thức?

---

**Ngày cập nhật**: 2026-01-28  
**Lý do**: Đảm bảo tính nhất quán trong trình bày công thức toán học theo chuẩn văn bản khoa học  
**Áp dụng cho**: Tất cả các công thức toán học trong tài liệu

---

## 7. Quy tắc Sử dụng Chữ In Đậm

### 7.1. Nguyên tắc Chung

Chữ in đậm (bold text) chỉ được sử dụng cho **tiêu đề** và **đề mục**. **KHÔNG được** sử dụng chữ in đậm trong nội dung văn bản chính.

### 7.2. Quy định Cụ thể

**✅ Được phép sử dụng:**
- Tiêu đề section: `\section{...}`, `\subsection{...}`, `\subsubsection{...}`
- Đề mục trong bảng, hình
- Tiêu đề cột trong bảng (table headers)

**❌ Không được phép:**
- Nhấn mạnh từ khóa trong đoạn văn
- Làm nổi bật thuật ngữ kỹ thuật
- Đánh dấu khái niệm quan trọng trong nội dung

### 7.3. Ví dụ Minh họa

#### ❌ **SAI** (Dùng bold trong nội dung):
```latex
Phương pháp \textbf{KKT-MPEC} là cách tiếp cận cổ điển để giải 
bài toán SLMF. Ưu điểm chính là \textbf{nghiệm chính xác} khi 
hàm lồi.
```

#### ✅ **ĐÚNG** (Không dùng bold trong nội dung):
```latex
Phương pháp KKT-MPEC là cách tiếp cận cổ điển để giải 
bài toán SLMF. Ưu điểm chính là nghiệm chính xác khi 
hàm lồi.
```

#### ✅ **ĐÚNG** (Chỉ dùng bold cho headers):
```latex
\subsection{Phương pháp KKT-MPEC}

\begin{table}[H]
\begin{tabular}{|l|l|}
\hline
\textbf{Phương pháp} & \textbf{Độ chính xác} \\
\hline
KKT-MPEC & Chính xác \\
\hline
\end{tabular}
\end{table}
```

### 7.4. Lý do

- **Tính nhất quán**: Văn bản khoa học chuyên nghiệp tránh lạm dụng formatting
- **Dễ đọc**: Quá nhiều chữ in đậm gây rối mắt và mất tập trung
- **Chuẩn mực**: Tuân theo các journal và conference guidelines quốc tế

### 7.5. Thay thế

Nếu cần nhấn mạnh, sử dụng:
- **Thuật ngữ kỹ thuật**: Để in nghiêng (`\emph{...}` hoặc `\textit{...}`)
- **Khái niệm quan trọng**: Đặt trong ngữ cảnh câu rõ ràng, không cần format đặc biệt
- **Định nghĩa**: Sử dụng equation environment hoặc cấu trúc câu phù hợp

---

**Ngày cập nhật**: 2026-01-28  
**Lý do**: Đảm bảo tính chuyên nghiệp và tuân thủ chuẩn mực văn bản khoa học  
**Áp dụng cho**: Toàn bộ nội dung văn bản (trừ tiêu đề và table headers)

---

## 8. Quy tắc Định dạng Bài toán Optimization

### 8.1. Nguyên tắc Chung

Bài toán tối ưu hóa (optimization problems) phải được trình bày theo chuẩn quốc tế với:
- Sử dụng **tiếng Anh** cho từ khóa toán học ("subject to", "minimize", "maximize")
- Căn chỉnh cột rõ ràng bằng `align` environment
- Numbering hợp lý (chỉ đánh số dòng quan trọng)

### 8.2. Quy định Cụ thể

**✅ Sử dụng:**
- `\begin{align}...\end{align}` thay vì `\begin{equation}\begin{aligned}...\end{aligned}\end{equation}`
- `\text{subject to}` hoặc `\text{s.t.}` thay vì "sao cho"
- Dấu `&` để căn chỉnh objective function và constraints
- `\nonumber` cho các dòng không cần đánh số

**❌ Tránh:**
- Tiếng Việt trong công thức toán ("sao cho", "với điều kiện")
- Thiếu căn chỉnh cột
- Đánh số mọi dòng (gây rối)

### 8.3. Ví dụ Minh họa

#### ❌ **SAI** (Tiếng Việt, căn chỉnh kém):
```latex
\begin{equation}
\begin{aligned}
\min_{x, y} \quad & F(x, y) \\
\text{sao cho} \quad & x \in X, \quad g(x,y) \leq 0 \\
& h(x,y) = 0
\end{aligned}
\end{equation}
```

#### ✅ **ĐÚNG** (Tiếng Anh, căn chỉnh chuẩn):
```latex
\begin{align}
\min_{x,y} \quad & F(x, y) \nonumber \\
\text{subject to} \quad & x \in X, \\
& g(x,y) \leq 0, \nonumber \\
& h(x,y) = 0. \nonumber
\end{align}
```

### 8.4. Ví dụ Thực tế: MPEC từ Section 3.1

Đây là ví dụ **thực tế** từ file `03_phuong_phap_giai.tex` đã được cải thiện:

#### ❌ **BEFORE** (Không đạt chuẩn):
```latex
\begin{equation}
\begin{aligned}
\min_{x, y, \lambda} \quad & F(x, y) \\
\text{sao cho} \quad & x \in X, \quad \nabla_{y_i} \mathcal{L}_i(x, y, \lambda_i) = 0, \quad i = 1, \ldots, N \\
& g_i(x, y) \leq 0, \quad \lambda_i \geq 0, \quad \lambda_{ij} \cdot g_{ij}(x, y) = 0, \quad \forall i, j.
\end{aligned}
\end{equation}
```

**Vấn đề:**
- ❌ Sử dụng `equation+aligned` thay vì `align`
- ❌ "sao cho" (tiếng Việt)
- ❌ Constraints quá dài trên cùng 1 dòng
- ❌ Khoảng trắng thừa trong subscript: `x, y, \lambda`
- ❌ Không kiểm soát numbering

---

#### ✅ **AFTER** (Chuẩn quốc tế):
```latex
\begin{align}
\min_{x,y,\lambda} \quad & F(x, y) \nonumber \\
\text{subject to} \quad & x \in X, \\
& \nabla_{y_i} \mathcal{L}_i(x, y, \lambda_i) = 0, \quad i = 1, \ldots, N, \nonumber \\
& g_i(x, y) \leq 0, \quad \lambda_i \geq 0, \nonumber \\
& \lambda_{ij} \cdot g_{ij}(x, y) = 0, \quad \forall i, j. \nonumber
\end{align}
```

**Cải thiện:**
- ✅ `align` environment
- ✅ "subject to" (tiếng Anh)
- ✅ Mỗi constraint/nhóm constraint trên 1 dòng riêng
- ✅ Subscript gọn: `x,y,\lambda` (không có space)
- ✅ Chỉ dòng `x \in X,` được đánh số
- ✅ Căn chỉnh cột hoàn hảo với `&`

---

### 8.5. Template Chuẩn

**Cho bài toán minimization:**
```latex
\begin{align}
\min_{x_1,\ldots,x_n} \quad & f(x) \nonumber \\
\text{subject to} \quad & g_i(x) \leq 0, \quad i = 1,\ldots,m, \\
& h_j(x) = 0, \quad j = 1,\ldots,p. \nonumber
\end{align}
```

**Cho bài toán maximization:**
```latex
\begin{align}
\max_{x} \quad & f(x) \nonumber \\
\text{s.t.} \quad & x \in \mathcal{X}. \nonumber
\end{align}
```

**Cho bài toán MPEC (với complementarity):**
```latex
\begin{align}
\min_{x,y,\lambda} \quad & F(x,y) \nonumber \\
\text{subject to} \quad & x \in X, \\
& \nabla_y L(x,y,\lambda) = 0, \nonumber \\
& g(x,y) \leq 0, \quad \lambda \geq 0, \nonumber \\
& \lambda \cdot g(x,y) = 0. \nonumber
\end{align}
```

---

### 8.6. Quy tắc Chi tiết về Spacing

#### Subscript Variables
**❌ SAI:**
```latex
\min_{x, y, \lambda}     % Có khoảng trắng sau dấu phẩy
```

**✅ ĐÚNG:**
```latex
\min_{x,y,\lambda}       % KHÔNG có khoảng trắng
```

#### Between Components
**Sử dụng `\quad` để tạo khoảng cách:**
```latex
\min_{x} \quad & f(x)                    % \quad giữa min và f(x)
g_i(x) \leq 0, \quad i = 1,\ldots,n     % \quad giữa constraint và index range
```

---

### 8.7. Quy tắc Chi tiết về Constraints

#### Constraint dài → Tách thành nhiều dòng

**❌ SAI (quá dài, khó đọc):**
```latex
& x \in X, \quad g_i(x,y) \leq 0, \quad \lambda_i \geq 0, \quad \lambda_{ij} \cdot g_{ij}(x,y) = 0, \quad \forall i,j.
```

**✅ ĐÚNG (tách thành 3 dòng):**
```latex
& x \in X, \\
& g_i(x,y) \leq 0, \quad \lambda_i \geq 0, \nonumber \\
& \lambda_{ij} \cdot g_{ij}(x,y) = 0, \quad \forall i,j. \nonumber
```

#### Nhóm ràng buộc logic

**Nhóm feasibility:**
```latex
& g_i(x,y) \leq 0, \quad \lambda_i \geq 0, \nonumber \\
```

**Nhóm complementarity:**
```latex
& \lambda_{ij} \cdot g_{ij}(x,y) = 0, \quad \forall i,j. \nonumber
```

---

### 8.8. Numbering Strategy

**Quy tắc:**
- Chỉ đánh số **1 dòng** trong toàn bộ optimization problem
- Thường chọn dòng **constraint đầu tiên** sau "subject to"
- Tất cả dòng khác dùng `\nonumber`

**Ví dụ:**
```latex
\begin{align}
\min_{x} \quad & f(x) \nonumber \\          ← Không số
\text{s.t.} \quad & x \in X, \\            ← Có số (11)
& g(x) \leq 0. \nonumber \\                 ← Không số
\end{align}
```

**Lý do:** 
- Tránh rối mắt với nhiều số (11a, 11b, 11c...)
- Dễ tham chiếu: chỉ cần 1 số duy nhất cho cả optimization problem

---

### 8.9. Punctuation trong Optimization

**Tuân thủ Rule #6:**

- Dấu phẩy (`,`) sau mỗi constraint nếu còn constraint tiếp theo
- Dấu chấm (`.`) sau constraint cuối cùng

**Ví dụ:**
```latex
\text{subject to} \quad & x \in X,        \\    ← Phẩy (còn constraint sau)
& g(x) \leq 0, \nonumber \\                     ← Phẩy (còn constraint sau)
& h(x) = 0. \nonumber                           ← Chấm (constraint cuối)
```

---

### 8.10. Lưu ý Kỹ thuật

| Aspect | Quy tắc | Ví dụ |
|--------|---------|-------|
| **Environment** | Dùng `align` | `\begin{align}...\end{align}` |
| **Keywords** | Tiếng Anh | `\text{subject to}` hoặc `\text{s.t.}` |
| **Subscript** | Không space | `_{x,y,z}` ❌ `_{x, y, z}` |
| **Spacing** | Dùng `\quad` | `\min_{x} \quad & f(x)` |
| **Numbering** | 1 dòng duy nhất | Dòng constraint đầu |
| **Line breaks** | Mỗi constraint/nhóm = 1 dòng | Tách constraints dài |
| **Punctuation** | Rule #6 | Phẩy giữa, chấm cuối |

---

### 8.11. Checklist Tự Kiểm tra

- [ ] Sử dụng `align` environment thay vì `equation+aligned`?
- [ ] "subject to" bằng tiếng Anh (không phải "sao cho")?
- [ ] Căn chỉnh cột với `&` ở vị trí đồng nhất?
- [ ] Subscript không có khoảng trắng thừa (`x,y,z` không phải `x, y, z`)?
- [ ] Chỉ đánh số 1 dòng, các dòng khác có `\nonumber`?
- [ ] Constraints dài đã được tách thành nhiều dòng?
- [ ] Có dấu câu phù hợp (phẩy giữa, chấm cuối)?
- [ ] Sử dụng `\quad` để tạo spacing hợp lý?

---

**Ngày cập nhật**: 2026-01-28  
**Lý do**: Mở rộng với ví dụ MPEC thực tế và quy tắc chi tiết cho spacing, constraints, numbering  
**Áp dụng cho**: Tất cả các bài toán tối ưu hóa (minimization, maximization, MPEC, bilevel, etc.)

---

## 9. Quy tắc Cách Đoạn Văn bằng `\medskip`

### 9.1. Nguyên tắc Chung

Khi cần **cách đoạn văn** trong tài liệu LaTeX, **BẮT BUỘC** phải sử dụng lệnh `\medskip`. KHÔNG được sử dụng dòng trống liên tiếp hoặc lệnh `\\` để tạo khoảng cách giữa các đoạn.

### 9.2. Quy định Cụ thể

**✅ Được phép:**
- Sử dụng `\medskip` để tạo khoảng cách vừa phải giữa các đoạn văn
- Có thể kết hợp với dòng trống để rõ ràng trong source code

**❌ Không được phép:**
- Sử dụng nhiều dòng trống liên tiếp để tạo khoảng cách
- Sử dụng `\\` hoặc `\\[length]` để cách đoạn văn
- Sử dụng `\vspace{...}` trừ khi có lý do đặc biệt

### 9.3. Ví dụ Minh họa

#### ❌ **SAI** (Dùng dòng trống hoặc `\\`):
```latex
Đây là đoạn văn thứ nhất. Nội dung mô tả về phương pháp nghiên cứu.


Đây là đoạn văn thứ hai. Nội dung tiếp tục.

\\

Đây là đoạn văn thứ ba.
```

#### ✅ **ĐÚNG** (Dùng `\medskip`):
```latex
Đây là đoạn văn thứ nhất. Nội dung mô tả về phương pháp nghiên cứu.

\medskip
Đây là đoạn văn thứ hai. Nội dung tiếp tục.

\medskip
Đây là đoạn văn thứ ba.
```

### 9.4. Các Level Spacing Khác

Nếu cần khoảng cách khác nhau, có thể sử dụng:

| Lệnh | Khoảng cách | Sử dụng khi |
|------|-------------|-------------|
| `\smallskip` | Nhỏ (~3pt) | Cách nhẹ giữa các ý trong cùng đoạn |
| `\medskip` | Vừa (~6pt) | **Mặc định** - cách giữa các đoạn văn |
| `\bigskip` | Lớn (~12pt) | Cách giữa các phần/mục lớn |

### 9.5. Lý do

- **Nhất quán**: Đảm bảo khoảng cách đồng đều trong toàn bộ tài liệu
- **Kiểm soát**: Dễ dàng thay đổi spacing toàn cục nếu cần
- **Chuyên nghiệp**: Tuân theo best practices của LaTeX typesetting
- **Tránh lỗi**: `\\` giữa các đoạn có thể gây warning "There's no line here to end"

### 9.6. Checklist Tự Kiểm tra

- [ ] Sử dụng `\medskip` để cách đoạn thay vì dòng trống?
- [ ] Không có `\\` đứng riêng lẻ giữa các đoạn?
- [ ] Không có nhiều dòng trống liên tiếp (>1)?
- [ ] Spacing nhất quán trong toàn bộ tài liệu?

---

**Ngày cập nhật**: 2026-02-02  
**Lý do**: Đảm bảo cách đoạn nhất quán và chuyên nghiệp trong tài liệu LaTeX  
**Áp dụng cho**: Tất cả các đoạn văn trong tài liệu

---

## 10. Quy tắc Giải thích và Trích dẫn Khái niệm Mới

### 10.1. Nguyên tắc Chung

Khi **đề cập đến một khái niệm kỹ thuật, thuật ngữ chuyên môn, hoặc hiện tượng mới** lần đầu tiên trong tài liệu, **BẮT BUỘC** phải:
1. **Giải thích ngắn gọn** ý nghĩa của khái niệm đó, HOẶC
2. **Trích dẫn nguồn tài liệu** cho phép người đọc tìm hiểu thêm, HOẶC
3. **Cả hai** (giải thích + trích dẫn) nếu khái niệm phức tạp

### 10.2. Quy định Cụ thể

**✅ Cần giải thích/trích dẫn:**
- Thuật ngữ kỹ thuật tiếng Anh (LICQ, MFCQ, MPEC, NEP, etc.)
- Hiện tượng/khái niệm chuyên ngành (duck curve, bounded rationality, etc.)
- Phương pháp/kỹ thuật mới (smoothing, aggregation, etc.)
- Điều kiện toán học (constraint qualification, complementarity, etc.)

**❌ Không cần giải thích:**
- Khái niệm đã được định nghĩa trước đó trong tài liệu
- Thuật ngữ cơ bản mà đối tượng độc giả chắc chắn biết
- Ký hiệu toán học chuẩn ($\min$, $\max$, $\nabla$, etc.)

### 10.3. Ví dụ Minh họa

#### ❌ **SAI** (Không giải thích, không trích dẫn):
```latex
Các điều kiện chính quy như LICQ hay MFCQ cũng cần thiết để đảm bảo 
KKT là điều kiện cần cho tối ưu.
```

**Vấn đề:**
- LICQ, MFCQ là gì? Người đọc không biết
- Không có nguồn tham khảo để tìm hiểu thêm

#### ✅ **ĐÚNG** (Có giải thích + trích dẫn):
```latex
Các điều kiện chính quy (constraint qualification) cũng cần thiết để 
đảm bảo điều kiện KKT là điều kiện cần cho tối ưu \cite{MPECMethods2000}. 
Hai điều kiện phổ biến nhất là LICQ (Linear Independence Constraint 
Qualification) --- yêu cầu các gradient của ràng buộc tích cực phải 
độc lập tuyến tính, và MFCQ (Mangasarian-Fromovitz Constraint 
Qualification) --- điều kiện yếu hơn cho phép sự phụ thuộc tuyến tính 
nhưng đòi hỏi tồn tại hướng khả thi nghiêm ngặt.
```

#### ✅ **ĐÚNG** (Hiện tượng với giải thích + trích dẫn):
```latex
...và hiện tượng duck curve (đường cong hình vịt) \cite{GameTheoreticEnergy2023} 
--- đồ thị nhu cầu điện trong ngày có hình dạng con vịt do điện mặt trời 
sản xuất dư thừa giữa trưa (tạo phần ``bụng vịt'') nhưng nhu cầu tăng 
đột biến vào buổi tối khi mặt trời lặn (tạo phần ``cổ vịt'').
```

### 10.4. Cấu trúc Giải thích Chuẩn

Khi giải thích một khái niệm, nên tuân theo cấu trúc:

```
[Tên khái niệm] ([Dịch nghĩa/viết tắt đầy đủ]) \cite{...} --- [giải thích ngắn gọn ý nghĩa].
```

**Ví dụ:**
```latex
bounded rationality (tính hợp lý hạn chế) \cite{BehavioralEcon2020} --- giả định 
rằng người ra quyết định có giới hạn về thời gian, thông tin và năng lực tính toán.
```

### 10.5. Lý do

- **Tính dễ hiểu**: Người đọc không cần tra cứu riêng
- **Tính chính xác**: Đảm bảo định nghĩa nhất quán
- **Tính học thuật**: Minh bạch nguồn gốc thông tin
- **Tính tiếp cận**: Hỗ trợ người đọc có nền tảng khác nhau

### 10.6. Checklist Tự Kiểm tra

- [ ] Mọi thuật ngữ kỹ thuật tiếng Anh đều có giải thích hoặc viết tắt đầy đủ?
- [ ] Mọi khái niệm chuyên môn đều có trích dẫn nguồn?
- [ ] Hiện tượng/kỹ thuật đặc thù đã được giải thích ý nghĩa?
- [ ] Giải thích ngắn gọn, đủ để người đọc hiểu được bản chất?

---

**Ngày cập nhật**: 2026-02-05  
**Lý do**: Đảm bảo tính dễ hiểu và minh bạch học thuật khi trình bày khái niệm mới  
**Áp dụng cho**: Tất cả thuật ngữ kỹ thuật, khái niệm chuyên môn, và hiện tượng mới trong tài liệu

