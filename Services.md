**سرویس**


در ابتدا باید فایل های زیر را در پروژه خود بروزرسانی کنید:
**IInAppBillingService.aidl
IabHelper.java**

'**شرح متدها :** 

۱. برای دریافت لیستی از Achievement هایی که یک کاربر در بازی شما بدست آورده به صورت زیر فراخوانی میشود.

```aidl
mHelper.getUserAchievements(“your.app.package.name”);
```

ورودی ها :
```String packageName``` 
این مقدار باید همواره  مطابق با اطلاعات اپلیکیشن شما در پنل باشد

توجه داشته باشید استفاده از این متد الزامی نیست و صرفا برای بررسی است.

خروجی ها :

```String userAchievements``` 
لیستی از Achievement هایی که کاربر توانسته بدست آورد، البته در آینده شاید تغییرات داشته باشد.

۲. برای آزاد کردن یک Achievement از این متد میتوانید استفاده کنید، برای اینکه

```java
mHelper.unlockUserAchievement(view.getContext().getPackageName(), "1");
```
