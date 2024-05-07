<p align="center">
<picture>
<img width="160" height="160"  alt="XPanel" src="https://github.com/iPmartNetwork/iPmart-SSH/blob/main/images/logo.png">
</picture>
  </p> 
<p align="center">
<h1 align="center"/>v6to4</h1>
<h6 align="center">6to4 Multi Tunnel<h6>
</p>



نام پروژه : تانل 6to4 - پرایوت ایپی (امکان تانل بین 5 سرور خارج و 1 ایران و برعکس)
---------------------------------------------------------------

------------------------
  **امکان تانل بین 5 سرور خارج و 1 سرور ایران و برعکس**
- مانند قبل سرور های خارج خودتان را اول کانفیگ کنید و بعد سرور ایران
- امکان تانل بین 5 سرور خارج و یک سرور ایران و برعکس
- از این پرایوت ایپی ها برای لود بالانس که به زودی قرار میدم هم میتوان استفاده کرد
- دقت نمایید اگر ارتباط پینگ بین دو طرف سرور در حین ساخت 5 سرور خارج و یک سرور ایران و برعکس ، انجام نشد؛ یک بار تمام سرور ها را با هم، هم زمان ریبوت کنید و احتمال زیاد درست شود.
- روش دیگر این است که ببینید کدام سرور مشکل اتصال دارد . مثلا اگر تانل 5 سرور خارج و یک سرور ایران است و به فرض مثال سرور 3 خارج مشکل دارد. بدون انکه چیزی را دست بزنید ، تنها سرور 3 را Uninstall کنید و دوباره اقدام به کانفیگ سرور 3 بکنید . این هم مشکل شما را حل میکند.
- دقت کنید که برای کانفیگ های سرور هایتان باید بدانید کدامین، سرور 1 2 3 4 5 است که به اشتباه از دو ایپی پرایوت یکسان استفاده نکنید که در تانل شما مشکل به وجود می اورد.
- به طور مثال برای 5 سرور خارج و 1 سرور ایران : در نظر بگیرید که سرور اول من سرور ترکیه و سرور دوم من سرور المان میباشد. شما باید در کانفیگ سرور خارج 1 و سرور ایران، برای سرور 1 خارج از ایپی سرور ترکیه استفاده کنید و در کانفیگ سرور 2 خارج و همچنین سرور ایران ، برای سرور 2 خارج از ایپی سرور المان استفاده نمایید . در غیر این صورت تانل، درست کار نخواهد کرد.
- اطمینان پیدا کنید که قبل از کانفیگ تاتل 6to4 میتوانید از سرور ایران به سرور های خارجتان، ssh برقرار کنید یا پینگ میتوانید بگیرید.
- مورد دیگه این هست که به طور مثال در تانل 5 سرور خارج و 1 سرور ایران ، داخل سرور ایران برای هر سرور خارج یک ایپی پرایوت جدا خواهیم داشت که باید به اینها برای کانفیگ های تانلتان دقت کنید .اگر تانل پنل به پنل هست که تنها نیاز به ایپی خارج هر سرور میباشد. اگر تانل هایی مانند FRP میباشد که نیاز به ایپی پرایوت های هر سرور خارج در سرور ایران دارید.
- به طور مثال در سرور ایران برای سرور ترکیه، یک ایپی پرایوت دارید و برای سرور المان، یک پرایوت ایپی دیگه دارید.
- مورد دیگر اینکه اگر تانل پنل به پنل هست، باید پرایوت ایپی ها را باز کنید.
- با آزمون و خطا، میتوانید تانل ها را به درستی کانفیگ نمایید.
 
 ---------------------------------

![check](https://github.com/Azumi67/PrivateIP-Tunnel/assets/119934376/13de8d36-dcfe-498b-9d99-440049c0cf14)
**امکانات**
 <div dir="rtl">&bull; ساخت تانل 6to4 بین چندین سرور [Anycast] & [PrivateIP]</div>
 <div dir="rtl">&bull; تانل بین 5 سرور خارج و 1 سرور ایران و برعکس</div>
 <div dir="rtl">&bull; امکان استفاده از ایپی در سرور های دیگر (توصیه نمیشود) [Anycast]</div>
 <div dir="rtl">&bull; استفاده از cronjob به جای service</div>
 <div dir="rtl">&bull; امکان  حذف کردن تانل ها</div>
 <div dir="rtl">&bull; پس از این تانل، میتوانید از ایپی های ساخته شده برای تانل اصلی یا پورت فوروارد استفاده نمایید</div>
  <div dir="rtl">&bull; امکان استفاده در لود بالانس FRP</div>
 <div dir="rtl">&bull;امکان ساخت چندین پرایوت ایپی برای سرور های شما</div>
 
 ------------------------------------------------------
  
  ![6348248](https://github.com/Azumi67/PrivateIP-Tunnel/assets/119934376/398f8b07-65be-472e-9821-631f7b70f783)
**آموزش**

------------------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP_multipleSERVERS/assets/119934376/dd030326-0687-412d-bd38-092e7492ddef)
**ساخت پرایوت ایپی بین یک سرور خارج و ایران**

  <p align="right">
  <img src="https://github.com/Azumi67/PrivateIP-Tunnel/assets/119934376/d92b4e8f-b368-4938-b639-5efea493e184" alt="Image" />
</p>



<div dir="rtl">&bull; ساخت پرایوت ایپی : از سرور خارج شروع کنید.</div>
 <div dir="rtl">&bull; ایپی 4 خارج و ایران را وارد نمایید</div> 
  <div dir="rtl">&bull; ساب نت 64 را وارد نمایید</div>
   <div dir="rtl">&bull; تعداد ایپی پرایوتی که نیاز دارید را وارد نمایید</div>
    <div dir="rtl">&bull; ایپی های ساخته شده را در notepad برای استفاده در تانل بنویسید</div>
     <div dir="rtl">&bull; به صورت اتوماتیک ایپی پرایوت وسرویس پینگ به منظور جلوگیری از اختلال برای شما ساخته خواهد شد</div>
      <div dir="rtl">&bull; سپس همین مراحل را برای سرور ایران هم انجام بدهید</div>

--------------------------------------

**5 سرور ایران و 1 سرور خارج**

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج**

 


 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/eedfceb3-fe05-4772-a0c3-ec57fb6fc2e8" alt="Image" />
</p>
 <div dir="rtl">&bull;در این تانل از 2 سرور ایران و 1 سرور خارج استفاده میکنیم.  </div>
  <div dir="rtl">&bull; همیشه کانفیگ تانل را از سرور خارج شروع نمایید</div>
   <div dir="rtl">&bull;تعداد سرور ایرانی که دارید را وارد نمایید ( بیشترین مقدار مجاز 5 عدد میباشد) </div>
    <div dir="rtl">&bull; برای هر سرور ایران، ایپی یکسان خارج ( به طور مثال ترکیه ) را قرار دهید و ایپی های سرور ایران خود را به ازای هر سرور، وارد نمایید</div>
     <div dir="rtl">&bull; .توجه کنید که اگر به طور مثال ایپی اروان را برای سرور یک ایران وارد نمایید، همان ایپی اروان را برای کانفیگ سرور 1 ایران وارد نمایید </div>
     <div dir="rtl">&bull;به این معنی که اگر برای سرور یک از ایپی اروان و سرور دوم از ایپی شاتل استفاده کردید، در کانفیگ سرور های ایران هم سرور اول ایپی اروان و سرور دوم ایپی شاتل خواهد بود در غیر اینصورت تانل برقرار نخواهد شد </div>
      <div dir="rtl">&bull; تعداد ایپی که برای هر سرور نیاز دارید را وارد نمایید</div>
       <div dir="rtl">&bull; برای اینکه cronjob برای سرور های شما ساخته شود، تعداد سرور ها را با فاصله وارد نمایید. به طور مثال اگر 2 سرور ایران دارید اینگونه وارد نمایید ( 2 1 )</div>


----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران 1**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/143f1dd2-0c63-4f6a-9b40-0034eabefb35" alt="Image" />
</p>
 <div dir="rtl">&bull; حالا باید برای هر سرور ایران، کانفیگ را جداگانه انجام دهیم</div>
 <div dir="rtl">&bull; مثلا برای سرور یک ایران در عکس قبل از سرور اروان استفاده کردیم، پس باید اینجا هم برای سرور یک ایران از سرور اروان استفاده نماییم</div>
  <div dir="rtl">&bull; سرور خارج برای تمامی سرور های ایران یکسان است چون تانل 3 سرور ایران و 1 سرور خارج میباشد</div>
   <div dir="rtl">&bull; تعداد ایپی هایی که میخواهید را وارد نمایید</div>

--------------------------------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815)**سرور ایران 2**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/3bae7757-360b-4460-bd2b-adbbcfaad8d0" alt="Image" />
</p>
 <div dir="rtl">&bull; سرور دوم ایران را برای کانفیگ سرور دوم ایران وارد نمایید</div>
  <div dir="rtl">&bull; سرور خارج برای تمامی سرور های خارج یکسان میباشد</div>
   <div dir="rtl">&bull; تعداد ایپی که میخواهید را وارد نمایید</div>
    <div dir="rtl">&bull; اگر سرور سوم ایران دارید، مانند نمونه کانفیگ را انجام دهید</div>
     <div dir="rtl">&bull; برای حذف تانل ها از قسمت مربوطه اقدام به حذف تانل نمایید</div>


---------------------------------

**5 سرور خارج و 1 سرور ایران**

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/2c1ae043-4bc5-4738-b1d4-6951c8fecbdc)**سرور خارج 1**



<p align="right">
  <img src="https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/b8f47148-227b-440d-8d7e-c782a6a61a78" alt="Image" />
</p>

<div dir="rtl">&bull; همیشه کانفیگ تانل را از سرور خارج شروع نمایید</div>
<div dir="rtl">&bull; حالا باید برای هر سرور خارج، کانفیگ را جداگانه انجام دهیم</div>
  <div dir="rtl">&bull; سرور ایران برای تمامی سرور های خارج یکسان است چون تانل 3 سرور خارج و 1 سرور ایران میباشد</div>
   <div dir="rtl">&bull; تعداد ایپی هایی که میخواهید را وارد نمایید</div>
 
------------------------------------------------------------------------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/2c1ae043-4bc5-4738-b1d4-6951c8fecbdc)**سرور خارج 2**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/af8fd4f2-174b-4560-9875-ac33a5b5e6c5" alt="Image" />
</p>

 <div dir="rtl">&bull; سرور دوم خارج را برای کانفیگ سرور دوم خارج وارد نمایید</div>
  <div dir="rtl">&bull; سرور ایران برای تمامی سرور های خارج یکسان میباشد</div>
   <div dir="rtl">&bull; تعداد ایپی که میخواهید را وارد نمایید</div>
    <div dir="rtl">&bull; اگر سرور سوم خارج دارید، مانند نمونه کانفیگ را انجام دهید</div>
     <div dir="rtl">&bull; برای حذف تانل ها از قسمت مربوطه اقدام به حذف تانل نمایید</div>


---------------------------------------------------------------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/2e325267-240d-4e20-ba5a-ff408331d5a0)**سرور ایران**


  <p align="right">
  <img src="https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/6a683c0c-a602-44af-9085-5d0094b379ba" alt="Image" />
</p>
<div dir="rtl">&bull;در این تانل از 2 سرور خارج و 1 سرور ایران استفاده میکنیم.  </div>
   <div dir="rtl">&bull;تعداد سرور خارجی که دارید را وارد نمایید ( بیشترین مقدار مجاز 5 عدد میباشد) </div>
    <div dir="rtl">&bull; برای هر سرور خارج، ایپی یکسان ایران ( به طور مثال اروان ) را قرار دهید و ایپی های سرور خارج خود را به ازای هر سرور، وارد نمایید</div>
     <div dir="rtl">&bull; توجه کنید که اگر به طور مثال ایپی ترکیه را برای سرور یک خارج وارد نمایید، همان ایپی را برای کانفیگ سرور 1 خارج وارد نمایید</div>
       <div dir="rtl">&bull;به این معنی که اگر برای سرور یک از ایپی ترکیه و سرور دوم از ایپی آلمان استفاده کردید، در کانفیگ سرور های خارج هم سرور اول ایپی ترکیه و سرور دوم ایپی آلمان خواهد بود در غیر اینصورت تانل برقرار نخواهد شد </div>
      <div dir="rtl">&bull; تعداد ایپی که برای هر سرور نیاز دارید را وارد نمایید</div>
       <div dir="rtl">&bull; برای اینکه cronjob برای سرور های شما ساخته شود، تعداد سرور ها را با فاصله وارد نمایید. به طور مثال اگر 2 سرور خارج دارید اینگونه وارد نمایید ( 2 1 )</div>


-------------------------------
**تانل 6to4 به دو صورت**

**تانل 6to4 بدون Anycast**


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/d30892cf-cd26-4695-886d-9a4a47ade691)**سرور خارج**

  <p align="right">
  <img src="https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/81a38493-7df2-46f5-b51b-fee1c7e03349" alt="Image" />
</p>
<div dir="rtl">&bull;در این تانل از یک سرور خارج و یک سرور ایران استفاده میکنیم.  </div>
   <div dir="rtl">&bull; کانفیگ تانل را از سرور خارج آغاز میکنیم. ایپی سرور ایران و خارج را وارد نمایید </div>
    <div dir="rtl">&bull; تعداد ایپی که نیاز دارید را وارد نمایید</div>
     <div dir="rtl">&bull; برای اینکه سرویس پینگ فعال شود، لطفا طبق اسکرین شات ایپی 4 سرور ایران را وارد نمایید</div>
    

----------------------------------------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/d30892cf-cd26-4695-886d-9a4a47ade691)**سرور ایران**


  <p align="right">
  <img src="https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/dae46cda-ae43-474a-b795-2772e355303f" alt="Image" />
</p>
<div dir="rtl">&bull;در این تانل از یک سرور خارج و یک سرور ایران استفاده میکنیم.  </div>
   <div dir="rtl">&bull; ایپی سرور ایران و خارج را وارد نمایید </div>
    <div dir="rtl">&bull; تعداد ایپی که نیاز دارید را وارد نمایید</div>
     <div dir="rtl">&bull; برای اینکه سرویس پینگ فعال شود، لطفا طبق اسکرین شات ایپی 4 سرور خارج را وارد نمایید</div>
    


-------------------------------
**تانل 6to4 با Anycast**

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/d30892cf-cd26-4695-886d-9a4a47ade691)**سرور خارج**

  <p align="right">
  <img src="https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/fddfce1e-7e27-4d39-b3cb-38f5da53c798" alt="Image" />
</p>
<div dir="rtl">&bull;در این تانل از یک سرور خارج و یک سرور ایران استفاده میکنیم.  </div>
   <div dir="rtl">&bull; کانفیگ تانل را از سرور خارج آغاز میکنیم. ایپی سرور خارج را وارد نمایید </div>
    <div dir="rtl">&bull; تعداد ایپی که نیاز دارید را وارد نمایید</div>
     <div dir="rtl">&bull; برای اینکه سرویس پینگ فعال شود،  ایپی 4 سرور ایران را وارد نمایید</div>
    <div dir="rtl">&bull; از این ایپی میتوانید در سرور های دیگر هم استفاده نمایید و پینگ بگیرید اما پینگ تایم بستگی به سرور شما دارد و ممکن است مناسب نباشد</div>

----------------------------------------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/d30892cf-cd26-4695-886d-9a4a47ade691)**سرور ایران**


  <p align="right">
  <img src="https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/ae470272-77ee-439c-984e-d4e5b4ec6155" alt="Image" />
</p>
<div dir="rtl">&bull;در این تانل از یک سرور خارج و یک سرور ایران استفاده میکنیم.  </div>
   <div dir="rtl">&bull; ایپی سرور ایران را وارد نمایید </div>
    <div dir="rtl">&bull; تعداد ایپی که نیاز دارید را وارد نمایید</div>
     <div dir="rtl">&bull; برای اینکه سرویس پینگ فعال شود، لطفا ایپی 4 سرور خارج را وارد نمایید</div>
     <div dir="rtl">&bull; از این ایپی میتوانید در سرور های دیگر هم استفاده نمایید و پینگ بگیرید اما پینگ تایم بستگی به سرور شما دارد و ممکن است مناسب نباشد</div>


-------------------------------
## نصب 
----------------


```
apt install curl -y && bash <(curl -Ls https://raw.githubusercontent.com/ipmartnetwork/6to4/main/6to4.sh --ipv4)
```


# تلگرام

[@ipmart_network](https://t.me/ipmart_network)

[@iPmart Group](https://t.me/ipmartnetwork_gp)




 # حمایت از ما :hearts:
حمایت های شما برای ما دلگرمی بزرگی است<br> 
<p align="left">
<a href="https://plisio.net/donate/kB7QU7f7" target="_blank"><img src="https://plisio.net/img/donate/donate_light_icons_mono.png" alt="Donate Crypto on Plisio" width="240" height="80" /></a><br>
	
|                    TRX                   |                       BNB                         |                    Litecoin                       |
| ---------------------------------------- |:-------------------------------------------------:| -------------------------------------------------:|
| ```TJbTYV1fFo2485sYMyajxGPLFzxmNmPrNA``` |  ```0x4af3de9b303a8d43105e284823d95b4c600961a3``` | ```MPrkzFiNtw4Rg67bbZB6gCxa9LV87orABM``` |	

</p>	




<p align="center">
<picture>
<img width="160" height="160"  alt="XPanel" src="https://github.com/iPmartNetwork/iPmart-SSH/blob/main/images/logo.png">
</picture>
  </p> 

  
  

