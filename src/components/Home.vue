<template>
<div>
    <NavBar/>
    <SignUp name="Mani"/>
    
    
</div>
</template>
<script>
import SignUp from './SignUp.vue'
import NavBar from './NavBar.vue'
export default {
    name: 'HomeNew',
    components:{
        NavBar,
        SignUp,

    }

}
</script>