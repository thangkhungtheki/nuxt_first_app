<template>
<div class="container"> 
    <h2 class="text-center">Tạo trang trình bày Video bằng Bootstrap</h2> 
    <ul class="list-unstyled video-list-thumbs row"> 
     <li class="col-lg-3 col-sm-4 col-xs-6"> <a href="https://youtu.be/izXYJf11vFU" title="Cách sử dụng Bootstrap Grid System (Phần 8)" target="_blank">          \                             <img src="http://hocwebgiare.com/images/bootstrap-grid.jpg" alt="Barca" class="img-responsive" height="130px">         
       <h2>Cách sử dụng Bootstrap Grid System (Phần 8)</h2>          
       <span class="glyphicon glyphicon-play-circle"></span> <span class="duration">13:04</span> </a> 
     </li> 
     <li class="col-lg-3 col-sm-4 col-xs-6"> <a href="https://youtu.be/i71HcCtUG50" title="Cách sử dụng Bootstrap Grid System (Phần 7)" target="_blank">         
       <img src="http://hocwebgiare.com/images/bootstrap-grid.jpg" alt="Barca" class="img-responsive" height="130px">        
       <h2>Cách sử dụng Bootstrap Grid System (Phần 7)</h2>        
       <span class="glyphicon glyphicon-play-circle"></span> <span class="duration">19:27</span> </a> 
     </li> 
     <li class="col-lg-3 col-sm-4 col-xs-6"> <a href="https://youtu.be/ZgdhutOWz7A" title="Cách sử dụng Bootstrap Grid System (Phần 6)" target="_blank">         
      <img src="http://hocwebgiare.com/images/bootstrap-grid.jpg" alt="Barca" class="img-responsive" height="130px">        
      <h2>Cách sử dụng Bootstrap Grid System (Phần 6)</h2>        
       <span class="glyphicon glyphicon-play-circle"></span> <span class="duration">05:37</span> </a> 
     </li> 
     <li class="col-lg-3 col-md-4 col-sm-4 col-xs-6"> <a href="https://youtu.be/PVTzuQYnwao" title="Cách sử dụng Bootstrap Grid System (phần 5)" target="_blank">         
      <img src="http://hocwebgiare.com/images/bootstrap-grid.jpg" alt="Barca" class="img-responsive" height="130px">        
      <h2>Cách sử dụng Bootstrap Grid System (phần 5)</h2>        
      <span class="glyphicon glyphicon-play-circle"></span> <span class="duration">07:50</span> </a> 
     </li> 
     <li class="col-lg-3 col-md-4 col-sm-4 col-xs-6"> <a href="https://youtu.be/pCglq3U98hA" title="Cách sử dụng Bootstrap Grid System (phần 4)" target="_blank">         
      <img src="http://hocwebgiare.com/images/bootstrap-grid.jpg" alt="Barca" class="img-responsive" height="130px">        
      <h2>Cách sử dụng Bootstrap Grid System (phần 4)</h2>        
      <span class="glyphicon glyphicon-play-circle"></span> <span class="duration">16:01</span> </a> 
     </li> 
     <li class="col-lg-3 col-md-4 col-sm-4 col-xs-6"> <a href="https://youtu.be/NIKhV0kLpfE" title="Cách sử dụng Bootstrap Grid System (phần 3)" target="_blank">         
      <img src="http://hocwebgiare.com/images/bootstrap-grid.jpg" alt="Barca" class="img-responsive" height="130px">        
      <h2>Cách sử dụng Bootstrap Grid System (phần 3)</h2>        
      <span class="glyphicon glyphicon-play-circle"></span> <span class="duration">18:01</span> </a> 
     </li> 
     <li class="col-lg-3 col-md-4 col-sm-4 col-xs-6"> <a href="https://youtu.be/rNVxDithhlE" title="Cách sử dụng Bootstrap Grid System (phần 2)" target="_blank">         
      <img src="http://hocwebgiare.com/images/bootstrap-grid.jpg" alt="Barca" class="img-responsive" height="130px">        
      <h2>Cách sử dụng Bootstrap Grid System (phần 2)</h2>        
      <span class="glyphicon glyphicon-play-circle"></span> <span class="duration">17:45</span> </a> 
     </li> 
     <li class="col-lg-3 col-md-4 col-sm-4 col-xs-6"> <a href="https://youtu.be/2AggnP9GS0w" title="Cách sử dụng Bootstrap Grid System (phần 1)" target="_blank">         
      <img src="http://hocwebgiare.com/images/bootstrap-grid.jpg" alt="Barca" class="img-responsive" height="130px">        
      <h2>Cách sử dụng Bootstrap Grid System (phần 1)</h2>        
      <span class="glyphicon glyphicon-play-circle"></span> <span class="duration">15:52</span> </a> 
     </li> 
    </ul>
   </div>
</template>

<style type="text/css">.video-list-thumbs  li {    
    margin-bottom:12px;
    }
     
     
    .video-list-thumbs a { 
    display:block;  
    position:relative;  
    background-color: #111; 
    color: #fff;    
    padding: 8px; 
    border-radius:3px ;
    transition:all 500ms ease-in-out;   
    border-radius:4px
    }
     
    .video-list-thumbs a:hover {   
    box-shadow:0 2px 5px rgba(0, 0, 0, .3); 
    text-decoration:none
    }
     
    .video-list-thumbs h2 { 
    bottom: 0;  
    font-size: 14px;    
    height: 33px;   
    margin: 8px 0 0;
    }
     
    .video-list-thumbs .glyphicon-play-circle { 
    font-size: 60px;    
    opacity: 0.6;   
    position: absolute; 
    right: 39%; 
    top: 31%;   
    text-shadow: 0 1px 3px rgba(0, 0, 0, .5);   
    transition:all 500ms ease-in-out;
    }
     
    .video-list-thumbs a:hover .glyphicon-play-circle {    
    color:#fff; 
    opacity:1;  
    text-shadow:0 1px 3px rgba(0, 0, 0, .8);
    }
     
    .video-list-thumbs .duration {  
    background-color: rgba(0, 0, 0, 0.4);   
    border-radius: 2px; 
    color: #fff;    
    font-size: 11px;    
    font-weight: bold;  
    left: 12px; 
    line-height: 13px;  
    padding: 2px 3px 1px;   
    position: absolute; top: 12px;  
    transition:all 500ms ease;
    }
    .video-list-thumbs  li  a:hover .duration { 
    background-color:#000;
    }
     
    @media (min-width:320px) and (max-width: 480px) { 
    .video-list-thumbs .glyphicon-play-circle { 
    font-size: 35px; 
    right: 36%; 
    top: 27%;
    } 
     
    .video-list-thumbs h2 { 
    bottom: 0; 
    font-size: 12px; 
    height: 22px; 
    margin: 8px 0 0;
    }
    }</style>