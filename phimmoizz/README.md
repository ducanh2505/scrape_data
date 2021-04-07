# Đồ ÁN CUỐI KỲ KHOA HỌC DỮ LIỆU VÀ ỨNG DỤNG
## Thành Viên nhóm 
- Đào Đức Anh - 171227
- Phan Hữu Tú - 1712861
## Vấn đề
Ngày nay nhu cầu giải trí là một mối quan tâm của nhiều người, đặc biệt là giới trẻ hiện nay. Lĩnh vực giải trí thì cũng baon gồm nhiều thể loại như gaming, nhạc, phim ảnh, ... Trong đồ án này, Nhóm sẽ tìm hiểu và phân tích nhữn yếu tố nào sẽ ảnh hưởng đến chất lượng của một bộ phim.!
## Ý nghĩa
- Giải quyết được câu hỏi những yếu tố nào sẽ ảnh hưởng đến chất lượng của một bộ phim là một tác vụ đơn giản nhưng có thể sẽ mang lại những lợi ích cho khán giả và các nhà sản xuất phim. 
- Khi biết được những yếu tố nào sẽ đánh giá tốt chất lượng bộ phim thì sẽ giúp được cho khán giả, người có nhu cầu tìm những bộ phim phù hợp với sở thích, phù hợp với bản thân và đặc biệt không phải tốn quá nhiều thời gian lựa chọn phim khi chưa có mục đích cụ thể khi thưởng thức phim.
- Ngoài ra sẽ giúp các nhà sản xuất hiểu được nhu cầu xem phim của khán giả từ đó sẽ có chiến lược sản xuất phim tốt hơn.
- Cuối cùng sẽ giúp cho các kênh phân phối, các video platform có thể dễ dàng đề xuất phim đến với người xem tốt nhất.

## Các Thức thu thập dữ liệu
- [http://phimmoizz.net/] có lẽ là một kênh phân phối phim, tuy là kênh phân phối phim không hợp pháp nhưng có lẽ là hầu như ai cũng biết qua trang này. Do đó nhóm sẽ thu thập dữ liệu về các bộ phim đã có trên trang web này để thu thập dữ liệu để thực hiện giải quyết vấn đề đã được đặt ra.
- Nhóm sử dụng phương pháp parse HTML để thu thập dữ liệu

## Tổng quan về dữ liệu
- Dữ liệu gồm 19 cột và có 5939 dòng
- Với dữ liệu như trên nhóm sẽ thực hiện dữ đoán giá trị điểm 'star'. Điểm 'star'là điểm số mà người xem đánh giá bộ phim trên thang điểm 10. Đây là điểm số thể hiện như quan tâm bộ phim này dựa trên nhu cầu giải trí chứ không dựa trên các điểm số từ các chuyên gia chuyên môn về lĩnh vực điện ảnh. Do đó điểm star sẽ thể hiện được mối quan tâm của một khán giả xem phim để giải trí, thể hiện được một bộ phim có thu hút được người xem hay không.

## Chi tiết thông tin về các trường thông tin đã thu thập được
- IMDb  `float`: số điểm IMDb được vote, là các số thực từ 0 cho đến 10
- IMDb_votes `int` : số lượng người vote ra chỉ số IMDb
- director `object`: giám đốc sản xuất phim
- nations `object`: quốc gia sỡ hữu bộ phim
- duration `int`: thời lượng diễn ra bộ phim (theo phút)
- quality `object`: chất lượng bộ phim (Full HD, CAM, ...)
- resolution `object`: độ phân giải của phim (1024x768, ... )
- language `object`: ngôn ngữ hỗ trợ khi xem phim (phụ đề việt, thuyết minh, ...)
- genres `object`: thể loại phim (tình cảm, hài kịch, hành động, ...)
- company `object`: công ty sản xuất phim
- vietnamese_name `object`: tên phim ở dạng tiếng việt
- name`object`: tên gốc của phim
- year `int`: năm sản xuất của phim
- id `int`: định danh 
- star `float`: số sao được vote cho phim
- recommendations `object`: các id phim được giới thiệu khi coi một phim bất kỳ
- film_content `object`: nội dung bộ phim
- actors `object`: các diễn viên có trong phim
- relase `object`: ngày phát hành phim
## Tự đánh giá 
- Kết quả với mô hình độ lỗi RMSE trên tập test là 0.99
- Với đồ án này nhóm chưa xử lý được việc dữ liệu khá lệch và thưa. 
- Việc giải quyết vấn đề đã được đặt ra chưa đạt được kết quả như kì vọng. 
## Phân công công việc
- Đức Anh :  Thu thập dữ liệu, Xây dựng mô hình dự đoán  (hoàn thành 80%)
- Hữu Tú : EDA, tổng hợp hoàn thiện đồ án (hoàn thành 90%)

## Usage
- run các cell có trong file crawler.ipynb để thu thập dữ liệu - trong quá trình thực hiện có thể sẽ có thêm file error.txt ta không cần quan tâm file này vì nó dùng để đánh dấu những link của các bộ phim thu thập bị lỗi trong quá trình thực hiện và sẽ được tự động thu thập lại các link này.
- run các cell trong file EDA.ipynb để hiện thị nội dung phân tích dữ liệu đã được thu thập
- file models.ipynb đung dể xây dựng các model. Run mục Tiền xử lý để thực tiền xử lý dữ liệu, Có thể bỏ qua mục Xây dựng các mô hình và Run mục Kết quả để đánh giá trên tập test. Hoặc có thể Run các cell trong mục Xây dựng các mô hình để có thể hiện thị kết quả dự đoán, đỗ lỗi trên những mô hình khác nhau.
