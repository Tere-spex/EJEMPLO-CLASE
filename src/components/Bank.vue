<template>
  <div><h1>Bank</h1></div>
  <div>Income: {{income}}€</div>
  <div>Outcome: {{outcome}}€</div>
  <div>Balance: {{income + outcome}}€</div>
</template>

<script>
export default {
data(){
    return {
        income: 100,
        outcome: -30,
    }
},
computed(){
    
},
}
</script>

<style>

</style>