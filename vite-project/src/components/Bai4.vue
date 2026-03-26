<template>
    <div class="container mt-5">
        <h1 class="text-center">Truyện tiên hiệp</h1>
        <div class="row">
            <div class="col-sm-4">
                <div class="card">
                    <img :src="items[0].image" alt="Hình ảnh" />
                    <div class="card-body">
                        <h3 class="card-title">{{ items[0].title }}</h3>
                        <p class="card-text">{{ items[0].content }}</p>
                        <button class="btn btn-info">Xem chi tiết </button>
                    </div>
                </div>
            </div>
            <div class="col-sm-4">
                <div class="card">
                    <img :src="items[1].image" alt="Hình ảnh" />
                    <div class="card-body">
                        <h3 class="card-title">{{ items[1].title }}</h3>
                        <p class="card-text">{{ items[1].content }}</p>
                        <button class="btn btn-info">Xem chi tiết </button>
                    </div>
                </div>
            </div>
            <div class="col-sm-4">
                <div class="card">
                    <img :src="items[2].image" alt="Hình ảnh" />
                    <div class="card-body">
                        <h3 class="card-title">{{ items[2].title }}</h3>
                        <p class="card-text">{{ items[2].content }}</p>
                        <button class="btn btn-info">Xem chi tiết </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
// Import hình ảnh từ thư mục assets
import img1 from '../assets/vcct.jpg';
import img2 from '../assets/tracpham.jpg';
import img3 from '../assets/ytk.jpg';
const items = ([
    {
        title: 'Vạn Cổ Chí Tôn', content: 'Vạn Cổ Chí Tôn là một tiểu thuyết tiên hiệp – huyền huyễn nổi bật, do Thái Nhất Sinh Thủy sáng tác, lần đầu được phát hành vào năm 2014 trên các nền tảng tiểu thuyết trực tuyến Trung Quốc. Với hơn 3800 chương và đã hoàn thành, tác phẩm nhanh chóng thu hút một lượng lớn độc giả yêu thích thể loại tu tiên, trọng sinh và hành động pha hài hước.', image: img1
    },
    {
        title: 'Đại Quản Gia là Ma Hoàng', content: 'Đại Quản Gia là Ma Hoàng là một trong những bộ truyện tranh huyền huyễn, trọng sinh kịch tính và phức tạp nhất hiện nay. Nội dung truyện xoay quanh Trác Phàm, vốn là một Ma Hoàng đứng trên đỉnh cao, nhưng vì sở hữu Cửu U Bí Lục mà bị đồ đệ phản bội, dẫn đến bi kịch tự bạo. May mắn thay, anh có cơ hội tái sinh trong thân xác của một gia nô tên Trác Phàm thuộc Lạc gia, một gia tộc đang trên đà suy vong.',
        image: img2
    },
    {
        title: 'Yêu Thần Ký', content: 'Truyện Yêu Thần Ký kể về Nie Li, một thiên tài bị diệt tộc trong kiếp trước nhưng may mắn quay về quá khứ khi còn mười ba tuổi. Sở hữu ký ức và kinh nghiệm chiến đấu vượt xa tất cả, cậu thề sẽ thay đổi định mệnh bi thảm, bảo vệ người thân và thành phố Thánh Lan khỏi thảm họa diệt vong. Yêu Thần Ký truyện chữ chinh phục độc giả bằng cốt truyện kịch tính, hệ thống cảnh giới yêu thần ký logic và những trận chiến nghẹt thở khiến fan không thể rời mắt.', image:
            img3
    },
]);
</script>