# persian-comment-sentiment-analysis
![photo10554143897](https://github.com/faeghe-kashani/persian-comment-sentiment-analysis/assets/52905775/67e1b130-54d5-4542-addf-a0c059b6dce0)

Digikala's artificial intelligence challenge



دیجی‌کالا به عنوان اولین مقصد خرید آنلاین در نظر دارد، با برگزاری این رقابت شما را با کار کردن بر روی مسائل کاربردی و دیتای واقعی به چالش بکشد تا مهارت‌های خود را در بستر دیتای بزرگترین فروشگاه آنلاین کشور محک بزنید.

سوال3_ دسته‌بندی مقصود نظرات کاربران
در این چالش نظرات کاربران را بر اساس مقصودشان دسته بندی می‌کنیم. (Nlp)

دسته‌بندی مقصود نظرات کاربران
در دیجیکالا یکی از خدمت‌هایی که به کاربران ارائه می‌شود، نظرات کاربران دیگر در مورد محصولات است. این طیف متنوع از نظرات، می‌تواند به کاربران قدرت انتخاب بیشتری دهد و کاربران کالای مناسب‌تر برای خود را پیدا کنند. در راستای ارائه دید بهتر از نظرات، قصد طراحی محصولی را داریم که بتوان کامنت‌ها را دسته‌بندی کرد و نظرات مرتبط با یک دسته‌بندی (مانند کیفیت محصول) را در یک دسته قرار داد. در این مسئله از شما می‌خواهیم که این دسته‌بندی را برای ما انجام دهید. به این منظور ۲ فایل در دسترس شما قرار گرفته‌است. این داده‌ها به منظور آموزش مدل و دیگری به منظور تست مدل شماست.

ساختار داده

ستون های داده های آموزش به شکل زیر است:
•	id
•	comment
•	intent

ستون اول شناسه نظرات کاربران است که در اختیار شما قرارگرفته‌است. ستون دوم متن نظر است که بر اساس آن باید مقصود کاربر شناسایی شده و دسته‌بندی انجام شود. ستون سوم، کلاس پیش‌بینی‌شده برای نظر است. به این شکل که اگر یک دسته‌بندی برای آن پیدا شده‌باشد، یک عدد متناظر با کلاس داده و اگر چندین موضوع مورد بررسی قرارگرفته‌باشد، عدد‌ها با comma از هم جدا شده‌اند و کلاس‌های مختلف نظر را نشان می‌دهند.
هرکدام از اعداد به یکی از دسته‌بندی‌های نظرات مرتبط است:
•	کلاس ۱ : جنس و کیفیت
•	کلاس ۲: قیمت و ارزش خرید
•	کلاس ۳: سایز و اندازه
•	کلاس ۴: مطابقت کالای ارسالی و کالای داخل سایت
•	کلاس ۵ : عطر و طعم

قالب پاسخ

داده تست نیز که در اختیار شما قرارگرفته‌است فقط ستون آخر از آن حذف‌شده‌است و شما می‌بایست با استفاده از مدل خود، کلاس یا کلاس‌های هر نظر را پیش بینی کرده و در آن ستون قرار دهید. ستون سوم را با همان نام intent به فایل تست اضافه کنید و در پاسخ ارسال نمایید شما باید یک فایل csv با نام result.csv بارگزاری کنید که شامل ستون intent باشد . ترتیب داده تست را حفظ نمایید. در صورتی که برای یک نظر بیش از یک کلاس پیش‌بینی کردید، کلاسها را به‌وسیله ویرگول از هم جدا کنید .دقت کنید که فایل جواب حاوی سلول خالی و یا Nan نباشد.

معیار ارزیابی
در این مسئله precision مدل شما معیار محاسبه امتیاز شماست.


سوال4_ پیش‌بینی فروش Digikala Fresh
در این چالش فروش هر دسته‌بندی برای هر کاربر در digikala fresh را پیش بینی می‌کنیم.

پیش‌بینی فروش Digikala Fresh
پیش‌بینی فروش هر دسته‌بندی برای هر کاربر در digikala fresh دیجی‌کالا، بزرگترین فروشگاه اینترنتی ایران، امکان خرید و بررسی طیف متنوعی از محصولات را برای کاربران فراهم می‌کند. در این فروشگاه اقلام متنوعی از کالا‌ها ارائه می‌شود. یکی از دسته‌بندی‌هایی که در سال گذشته به دیجی‌کالا اضافه شد، دسته‌بندی کالاهای سوپرمارکتی بود. این بخش با عنوان فِرِش در دیجی‌کالا راه‌اندازی شد و امکان خرید کالاهای سوپرمارکتی برای کاربران فراهم شد.
هدف از این چالش، پیش بینی خرید هر کاربر در بازه دو ماهه بعد از آخرین خرید داده‌های آموزشی است.

ساختار داده

در این مسئله داده خرید تعدادی از کاربران دیجی‌کالافِرِش در بازه زمانی ۷ ماهه در اختیار مسابقه‌دهندگان قرار گرفته است (فایل filtered_train_data.csv). این داده‌ها از داده‌های واقعی sample و encode شده و در اختیار کاربران قرار گرفته است. فایل filtered_train_data.csv که داده های آموزشی مسئله است دارای ستون‌هایی است که در ادامه به توضیح آنها میپردازیم:
•	:date تاریخ و زمان خرید کاربر
•	:nuser_id کد کاربری فرد خرید کننده
•	:norder_id شماره سفارش
•	:product_id کد کالا
•	:category نام دسته بندی کالا
•	:ncategory کد دسته بندی کالا
•	:quantity تعداد خریداری شده از کالا در آن سفارش

قالب پاسخ

فایل filtered_sample_output.csv نمونه خروجی است که کاربر باید در سایت بارگزاری کند. این فایل دارای ۶۷ ستون است. ستون اول یعنی nuser_id شماره کاربر است به صورت کد شده در هر دو فایل آموزش و تست وجود دارد و اعداد 0 تا 156072 است. این اعداد در هر دو فایل هماهنگ است یعنی یک عدد خاص در هر دو فایل به یک کاربر اشاره دارد. به ازای هر کاربر یک ردیف در فایل تست وجود دارد. ستون‌های دیگر این فایل اعداد ۰ تا ۶۵ هستند که کد همه دسته‌بندی‌های موجود فایل آموزش است. این اعداد هم با داده‌های آموزشی هماهنگ است و یک عدد خاص در هر دو فایل به یک دسته‌بندی اشاره می‌کند.
خروجی به صورت باینری باید در قالب ذکر شده پر شود و در سایت بارگزاری شود. یعنی همه کاربران به ترتیب باید در فایل خروجی آورده شوند، و برای هرکدام دسته‌بندی‌های ۰ تا ۶۵ با اعداد ۰ و ۱ پر شود. ۰ نشان از عدم خرید کاربر در آن دسته بندی و ۱ نشان از خرید آن کاربر در آن دسته‌بندی است. در این مسئله میزان خرید مهم نیست و فقط خرید یا عدم خرید کاربر در هر دسته‌بندی مهم است. اعداد پر شده در جدول باید به صورت عددی و صحیح (integer) باشند. در فایل نمونه به صورت پیش‌فرض همه داده‌ها با صفر پرشده‌اند و کاربر باید فایل را با اعداد ۱ که پیش‌بینی می‌کند، پر کند.
شما باید یک فایل csv با نام result.csv بارگزاری کنید که شامل ستون ‍‍‍‍nuser_id و ۶۶ ستون دیگر برای ۶۶ نوع مختلف کالا باشد . ترتیب داده تست را حفظ نمایید.

معیار ارزیابی
دقت داشته‌باشید همانطور که از ماهیت مسئله پیداست، بیشتر اعداد داخل فایل باید ۰ باشد و چون نوع خروجی از نوع داده‌های نامتوازن است، معیار ارزیابی فایل کاربر فقط دقت نیست. در این مسئله معیار ارزیابی امتیاز F1 فایل بارگزاری‌شده‌ خواهدبود.
