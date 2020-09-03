# A-simple-front-end-solution-for-unlimited-menu
一个简单无限级菜单的前端实现 


##原理
<br>
1、点击无限极菜单时产生的变化：<br>
当前点击菜单的子菜单块未显示，点击后显示；<br>
当前点击菜单的子菜单块显示 ，点击后隐藏<br>
<br>
2、选中菜单项：<br><br>
显示菜单项所属的菜单块；<br>
显示所属菜单块对应的菜单项（又是一个选中菜单项的操作）...直到没有需要显示的菜单块为止<br>
<br>
##基本结构
<br><br>
1、菜单项：<br><
``` 
<li class='menu-item'>
<a>菜单名</a>
</li>
``` 
<br>
2、多个菜单项组成菜单块<br>
<ul class='menu-block'>
 <li  class='menu-item'><a/></li>
 <li  class='menu-item'><a/></li>
</ul>
<br>
3、菜单项中添加子菜单块，<br>
<li class='menu-item'>
<a/>
/*子菜单块*/
<ul class='menu-block'>
 <li  class='menu-item'/><a/>
 <li  class='menu-item'/><a/>
</ul>
/*子菜单块*/
</li>
<br>
##dom的表现：
<br>
1、菜单块默认不显示<br>
即
.menu-item>.menu-block
{
display:none;
}
<br>
2、当点击菜单项时，其中的菜单块显示<br>
即 
.menu-item.chosen>.menu-block
{
display:block;
}
<br>
3、显示菜单块的状态下，再点击所属菜单项，则菜单块隐藏（去掉chosen）


 
