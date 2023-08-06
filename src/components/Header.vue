<template>
    <header>
        <nav>
            <h2 class="logo">Evaluation test(Vue-js)</h2>
            <ul>
                <li><router-link to="/">Test</router-link></li>
                <li><router-link to="/about">Countries</router-link></li>
            </ul>
        </nav>
       
    </header>
</template>

<script>
export default {

}
</script>

<style scoped>
    header{
        background: hsl(295, 95%, 45%);
        color: hsl(0, 24%, 93%);
        width: 100%;  
    }
    nav{
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 50px;
    }
    .logo{
        margin-left: 12px;
    }
    li{
        display: inline;
        list-style: none;
        font-size: 20px;
        gap: 20px;
        margin-inline: 30px;
    }
    li a{
        color: hsl(0, 24%, 93%);
    }
    li a:link{
        color: hsl(0, 24%, 93%);
        text-decoration: none;
    }
    li a:visited{
        color: hsl(0, 24%, 93%);
    }
    li a:hover{
        color: hsl(54, 92%, 48%);
    }
    li a.router-link-exact-active{
        color: hsl(180, 95%, 45%);
    } 
</style>