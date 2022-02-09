<template>
  <div class="new_post_root">
      <div class="new_post_wrapper">
        <div class="new_post_headline">Add New Post</div>
        <div class="new_post_description">Please fill out the details down below</div>
        <div class="new_post_title_wrapper">
            <div class="input_title">Post Title</div>
            <input class="new_post_title_input" v-model="title" placeholder="Is TrickBot Indestructible?" />
        </div>
        <div class="new_post_category_and_tag_wrapper">
            <div class="new_post_category_wrapper">
                <div class="input_title">Choose A Category</div>
                 <select class="new_post_select" v-model="category">
                    <option disabled value="">Please select one</option>
                    <option>Data Leaks</option>
                    <option>Vulnerabilities</option>
                    <option>Cyber Attacks</option>
                </select>
            </div>
            <div class="new_post_tag_wrapper">
                <div class="input_title">Choose A Tag</div>
                 <select class="new_post_select" v-model="tag">
                    <option disabled value="">Please select one</option>
                    <option>News</option>
                    <option>Articles</option>
                </select>
            </div>
        </div>
        <div class="new_post_post_description">
            <div class="input_title">Post Description</div>
            <textarea class="post_description_input" v-model="description" placeholder="After a takedown attempt in 2020 by the global law enforcement, that somehow wasn't that successful, a new TrickBot versi n has arrived."></textarea>
        </div>
      </div>
      <div class="new_post_submit_button">
        <Button label="Submit Post"/>
      </div>
      <div class="new_post_close_button">X</div>
  </div>
</template>

<script>
import Button from './Button.vue'

export default {
    name: "NewPost",
    data() {
    return {
      title: '',
      tag:'',
      category:'',
      description:'',
    }
  },
    components: {
    Button,
  }
}
</script>

<style>
    .new_post_root{
        width:774px;
        height:1034px;
        background-color:white;
        border-radius: 20px;
        display: flex;
        flex-direction: column;
        position: relative;
    }

    .new_post_wrapper{
        margin: 54px 88px ;
        position: absolute;
    }

    .new_post_headline{
        font-size:30px;
        font-weight:bold;
        text-align:center;
    }

    .new_post_description{
        text-align:center;
        font-size:18px;
        margin-top: 12px;
    }

    .new_post_title_wrapper{
        margin-top:40px;
    }

    .input_title{
        font-size:18px;
        margin-bottom: 11px;
    }

    .new_post_title_input{
        width: 100%;
        background: #F3F3F3 0% 0% no-repeat padding-box;
        height: 58px;
        font-size: 18px;
    }

    .new_post_category_and_tag_wrapper{
        margin-top: 40px;
        display:flex;
        justify-content: space-between;
    }

    .new_post_select{
        width: 278px;
        height: 58px;
        background: #F3F3F3 0% 0% no-repeat padding-box;
        font-size: 18px;
    }

    .new_post_post_description{
        margin-top: 40px;
    }

    .post_description_input{
        width: 599px;
        height: 197px;
        background: #F3F3F3 0% 0% no-repeat padding-box;
        font-size: 22px;
        font-family: 'Roboto';
    }

    .new_post_submit_button{
        position: absolute;
        bottom: 0;
        right: 50%;
        transform: translate(20%, -50px);
    }

    .new_post_close_button{
        position: absolute;
        top: 25px;
        left: 25px;
        color: #D6D6D6;
        cursor: pointer;
    }
</style>