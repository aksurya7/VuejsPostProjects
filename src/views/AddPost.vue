<template>
	<div class="add-post">       
     <div class="row mb-2">
         <div class="col text-right">
             <button class="btn btn-primary" v-on:click="formShow">Creat New Post</button>
         </div>
     </div>
     <div class="card mb-3" v-if="formDiv">

     <div class="card-body">
        <form @submit.prevent="addPost">
            <label for="">Post Title</label>
            <input v-model="title" type="text" name="title" class="form-control" >

            <label for="" >Post Details</label>
            <textarea v-model="body" name="body" class="form-control" placeholder="Details"></textarea>

            <div class="row my-3">
                <div class="col-6 mx-auto">
                    <button class="btn btn-success">Create Post</button>
                </div>
            </div>

        </form>
     </div>
     </div>
</div>

</template>


<script>
    export default{
        name:"AddPost",
        data(){
            return{
                formDiv:false,
                title: "",
                body: ""
            };
        },
        methods:{
            formShow(){
                this.formDiv = true;
            },
            addPost(){
                const newPost ={
                    title: this.title,
                    body: this.body
                };

                // send to parent
                this.$emit("add-post",newPost);
                (this.title=""),(this.body="");
            }
        }
    };
	
</script>

<style>
	
</style>