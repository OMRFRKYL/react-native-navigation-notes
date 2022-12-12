# react-native-navigation-notes

*-*-* React Navigation *-*-*

Tüm uygulamayı NavigationContainer yapısı ile saran, sayfalar arası hiyerarşinin component mantığında kurulduğu esnek bir yapıya sahip yönlendirme paketidir.React ile birlikte gelen
dahili paketlerden değil harici kütüphanelerdendir.

Kurulum için https://reactnavigation.org/ sitesinden gerekli adımar uygulanarak faydalanılabilir.<br/>
"npm/yarn install @react-navigation/native" ile kurulumu gerçekleştirebiliriz. 

Kapsadığı tüm ekranlara navigation ve router adından iki özel prop gönderir. Bu proplar sayesinde geçiş yapılan sayfaya ait parametreleri yakalayabilir ya da navigasyon fonksiyonlarını tetikleyebiliriz.

*-* Stack *-*
  Adından da anlaşılacağı üzere yığın mantığında sayfa geçisi sağlar. En temel sayfa transferi yapısıdır. Kullanıcıya uygulama bazında navigasyon geçmişi ile yönlendirme sağlanır.

*-* Tab *-*
  Ekranın alt bölümde, menü tarzında bir tasarıma sahip sayfa yönlendirmesine yapan navigasyon yapısıdır. Instagram, Twitter vb uygulamarın ana yönlendirme stilidir.

*-* Drawer *-*
  Yandan açılır menü şeklinde yönlendirme stiline sahip navigasyon yapısıdır. Genellikle material design uygulamaları bu tarzı tercih eder.
  
*-* Nested Navigation *-*
  Navigatorler arasında iç içe hiyerarşi kurulabilir. Tek bir adet NavigationContainer olacağından kullanıcı herhangi bir sayfadan tüm hiyerarşideki başka bir sayfaya geçebilir.

Ancak her navigator kendi routing history'sine sahiptir.
