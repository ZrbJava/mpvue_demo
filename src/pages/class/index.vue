<template>
    <div>
        <header>这是{{title}}</header>
       
       
    </div>
</template>

<script>
    export default {
        data(){
            return{
                title:"分类",
                data:{"message":null,"data":{"list":[{"id":27,"name":"妙洁棉柔抹布（三片装）","description":"吸水又去油，擦拭好轻松。（温馨提示：使用前，请先浸水将棉柔抹布的浆质洗掉；使用后，请将挂起晾干，可以延长使用寿命。）","state":0,"categoryId":4,"point":3000,"changeAmount":21,"createTime":1551409086000,"goodsPicUrls":"http://img.jidiankj.cn/2d00d45e-826e-4588-b52b-6508e3b692d4.jpg","picUrlList":["http://img.jidiankj.cn/2d00d45e-826e-4588-b52b-6508e3b692d4.jpg"]},{"id":26,"name":"超萌蘑菇玻璃杯","description":"简洁、方便携带的玻璃杯","state":0,"categoryId":4,"point":2500,"changeAmount":86,"createTime":1545982219000,"goodsPicUrls":"http://img.jidiankj.cn/9401f148-f89e-4c5f-97e7-6aa561ef3020.jpg","picUrlList":["http://img.jidiankj.cn/9401f148-f89e-4c5f-97e7-6aa561ef3020.jpg"]},{"id":25,"name":"可爱暖手抱枕","description":"小小手捂大大温暖-款式随机派送","state":0,"categoryId":5,"point":3000,"changeAmount":71,"createTime":1545973507000,"goodsPicUrls":",http://img.jidiankj.cn/0e8742e2-4c8c-444f-b5ae-8d8eff38f559.jpg","picUrlList":["http://img.jidiankj.cn/0e8742e2-4c8c-444f-b5ae-8d8eff38f559.jpg"]},{"id":7,"name":"大容量双肩背包","description":"小三轮-大容量背包，适用于徒步、穿越和日常使用。","state":0,"categoryId":5,"point":6000,"changeAmount":148,"createTime":1537075044000,"goodsPicUrls":"http://img.jidiankj.cn/b61089cf-3b56-4f61-b17d-1b266f72b225.png","picUrlList":["http://img.jidiankj.cn/b61089cf-3b56-4f61-b17d-1b266f72b225.png"]},{"id":6,"name":"实用-电热水壶","description":"小三轮-电热水壶","state":0,"categoryId":5,"point":6500,"changeAmount":187,"createTime":1537075000000,"goodsPicUrls":"http://img.jidiankj.cn/2f65219c-36c9-4fe6-a74a-ebe61811e798.png","picUrlList":["http://img.jidiankj.cn/2f65219c-36c9-4fe6-a74a-ebe61811e798.png"]},{"id":4,"name":"（小三轮）指甲钳套装","description":"指甲钳套装-精致、实用","state":0,"categoryId":3,"point":1500,"changeAmount":333,"createTime":1537074452000,"goodsPicUrls":"http://img.jidiankj.cn/a7886dd5-01f1-48e5-90d2-994e67e55066.png","picUrlList":["http://img.jidiankj.cn/a7886dd5-01f1-48e5-90d2-994e67e55066.png"]}],"total":6},"success":true,"code":200}
            }
        }
    }
</script>

<style scoped >

.shopListItem{
    display: flex;
    justify-content:space-between;
    font-size: 16px;
    /* align-items: center; */
    
}
img{
        /* width:220px; */
    }
.shopTitle{
    text-overflow:-o-ellipsis-lastline;
    overflow:hidden;
    text-overflow:ellipsis;
    display:-webkit-box;
    -webkit-line-clamp:2;
    -webkit-box-orient:vertical;
    align-content:center;

}
</style>