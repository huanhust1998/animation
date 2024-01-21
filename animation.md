I> keyframe : dùng để định nghĩa các animation

II> animation properties

- timeline: Dòng thời gian được định nghĩa trong @keyframe(0% => 50% => 100%)

1. animation-duration: 
    - Xác định thời lượng diễn ra animation trong bao lâu.
    - Giá trị mặc định là 0, khi này animation vẫn diễn ra, nhưng nó nhanh đến mức mà bạn không thể nhìn thấy.
    - Đây nên là một giá trị, và không thể thêm giá trị âm cho nó.

2. animation-timing-function
    - Tính toán tốc độ của animation tại mỗi thời điểm.
    - Giá trị: linear, ease, ease-in, ease-out, ease-in-out.(Giá trị mặc định là ease)
    - Hoặc có thể sử dụng cubic-bezier() để tính (https://cubic-bezier.com/#.17,.67,.83,.67)
    - Chia khoảng thời gian bằng các khoảng bằng nhau: step(number, direction)
        +> number: số bước animation sẽ chạy
        +> direction: mặc định là `end` (các step kết thúc ở cuối dòng thời gian)
                      hoặc có là `start`(step đầu tiên được tính là trạng thái ngay khi bắt đầu, nên vì vậy nó sẽ ít hơn `end` một step)

3. animation-iteration-count
    - Xác định số lần animation sẽ chạy
    - Giá trị mặc định là 1 và không thể là số âm
    - infinite: để làm cho animation lặp vô hạn

4. animation-direction
    - Định hướng timeline(dòng thời gian) trong keyframes định nghĩa trước đó
    - Các giá trị:
        +> normal: giá trị mặc định, chạy xuôi theo timeline.
        +> reverse: chạy ngược lại timeline.
        +> alternate: đối với lần animation chạy, timeline sẽ chạy xuôi hoặc người luân phiên nhau.
        +> alternate-reverse: ngược lại so với alternate.

5. animation-delay
    - Định nghĩa khoảng thời gian đợi đến khi bắt đầu animation.
    - Giá trị mặc định là 0s.
    - Chúng ta có thể đặt giá trị âm cho nó. Ví dụ khi animation-duration là 10s và đặt giá trị của animation-delay là -5s, thì animation sẽ bắt đầu ở khoảng 5s.

6. animation-play-state
    - Cho phép chúng ta play hoặc pause animation
    - Giá trị mặc định là `running` nếu xét là `paused` thì animation sẽ dừng lại.

7. animation-fill-mode
    - Xác định giá trị nào trong timeline của keyframe sẽ tồn tại trước khi animation chạy hoặc sau khi kêt thúc
    - Các giá trị: 
        +> none: Đây là giá trị mặc định, khi animation kết thúc, các giá trị trong timeline sẽ bị loại bỏ.
        +> forwards: Giá trị cuối cùng của timeline trong keyframe sẽ tồn tại, phụ thuộc vào animation-direction.
        +> backwards: Giá trị đầu tiên của timeline trong keyframe sẽ tồn tại, phục thuộc vào animation-direction.
        +> both: tuân theo quy tắc của forwards và backwards

8. animation shorthand - tổng hợp lại gồm 8 giá trị
    - animation: animation-name 
                 animation-duration 
                 animation-iteration-count 
                 animation-timing-function 
                 animation-direction 
                 animation-delay 
                 animation-play-state 
                 animation-fill-mode
BTVN: https://codepen.io/zanewesley/pen/NWRVJVN

