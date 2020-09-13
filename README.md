# prominenceSand
sand box


````
//name,w,h,x,y,z,fontlcr
bases,320,240,0,0,0,l
baseborder,320,240,0,0,0,l
basesplit,320,2,0,140,0,l
images,140,110,0,0,0,l
tlistL,210,50,110,0,0,l
tlistR,210,50,210,0,0,r
plistL,320,100,0,140,0,l
plistCl,210,100,110,140,0,l
plistCr,210,100,110,140,0,r
plistR,210,100,210,140,0,r
mes,210,90,110,50,0,c
infoborder,110,10,160,120,100,c
blink,16,16,0,0,100,c

//
.tl //left
.tr //right
.tc //center
.debug
.border
.bordertop
.underbar
.white
.red
.green
.gray
````




```
//drawer

/*
 .main
  canvas
  canvas
*/
let vw={}
vw.$firstflg=false
vw.$w=320
vw.$h=240
vw.$html=`<div class="main">
 <canvas id="c" width="${vw.$w}" height="${vw.$h}" style="position:absolute;top:0;left:0"></canvas>
 <canvas id="c2" width="${vw.$w}" height="${vw.$h}" style="position:absolute;top:0;left:0"></canvas>
</div>`
vw.$ctx=void 0
vw.$ctx2=void 0
vw.$font='16px boxdrawing,monospace'
vw.$green='#00ff00'
vw.$red='#ff0000'
vw.$white='#ffffff'
vw.$gray=vw.grey='#aaaaaa'
vw.$transparent='#00000000'
vw.$black='#000000'
;
//fillText(text, x, y [, maxWidth ] )

function drawer(){
 function init(){
  if(vw.$ctx)return;
  let a=document.querySelectorAll('canvas')
  if(!a.length)return document.body.innerHTML=vw.$html,init();
  ;
  return vw.$ctx=a[0].getContext('2d'),vw.$ctx2=a[1].getContext('2d')
  ;
 }
 init()
 ;
 function save(){
  if(vw.$firstflg)return;
  vw.$ctx.font=vw.$font
  vw.$ctx2.font=vw.$font
  vw.$ctx.strokeStyle=vw.$white
  vw.$ctx2.strokeStyle=vw.$white
  vw.$ctx.fillStyle=vw.$transparent
  vw.$ctx2.fillStyle=vw.$transparent
  return vw.$firstflg=true
 }
 save()
 ;
 function restore(){
  return vw.$ctx.restore(),vw.$ctx2.restore()
 }
 restore()
 ;
 ;
 //vw.$xyz 

}

requestAnimationFrame=drawer();

```







