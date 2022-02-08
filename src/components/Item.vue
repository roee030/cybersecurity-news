<template>
  <div class="item_root">
      <img class="item_image" src="../assets/itemCover.png" alt="img"/>
      <div class="item_details">
          <div class="item_headline">{{item.headLine}}</div>
          <div class="item_tag">
            <img class="tag_icon" src="../assets/tag.svg" alt="img"/>
              {{item.tag}}</div>
          <div class="item_description">{{item.description}}</div>
          <div class="item_actions">
            <div class="item_action">
                <img src="../assets/like.svg" alt="img"/>
                like</div>
            <div class="item_action">
                <img src="../assets/bookmark.svg" alt="img"/>
                bookmark</div>
            <div class="item_action">
                <img src="../assets/comments.svg" alt="img"/>
                comments ({{item.comments}})</div>
            <div class="item_action">
                <img src="../assets/share.svg" alt="img"/>
                share</div>
          </div>
      </div>
      <div class="item_created_date">
          January 30, 2021
      </div>
  </div>
</template>

<script>
export default {
    name: 'Item',
    props:{
        item: Object,
    }
}
</script>

<style>
.item_root{
    padding: 33px 30px;
    display: flex;
    position: relative;
    width: 858px;
}

.item_image{
    width:241px;
    height: 231px;
    margin-right: 20px;
}

.item_details{
    display: flex;
    flex-direction: column;
}

.tag_icon{
    width:14px;
    height: 14px;
}

.item_headline{
    font-size: 22px;
}    

.item_tag{
    text-decoration: underline;
    margin-bottom: 26px;
}

.item_created_date{
    position: absolute;
    right: 0;
    top: 10;
}

.item_action{
    cursor: pointer;
}
.item_action:hover{
    opacity: 0.7;
}
.item_actions{
    margin-top: auto;
    font-size:16px;
    width: 597px;
    height: 36px;
    background-color: #F0F1F8;
    display:flex;
    align-items: center;
    justify-content: space-around;
    bottom:0;
}
</style>