<template>
 <div id="vcomments"></div>
</template>
 
<script>
export default {
 name: 'Valine',
 mounted: function(){
  // require window 
  const Valine = require('valine');
  if (typeof window !== 'undefined') {
   this.window = window
   window.AV = require('leancloud-storage')
    
  }
    
  new Valine({
   el: '#vcomments' ,
   appId: 'A9E0wglWeUDqd0bQPfrXnEFh-MdYXbMMI',// your appId
   appKey: 'x5JipUK8WxuVpiA38rAuYYh7', // your appKey
   notify:false, 
   verify:false, 
   avatar:'mm', 
   placeholder: 'just go go'
  });
 },
}
</script>