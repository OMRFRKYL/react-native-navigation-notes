# react-native-navigation-notes

*-*-* React Navigation *-*-*

Tüm uygulamayı NavigationContainer yapısı ile saran, sayfalar arası hiyerarşinin component mantığında kurulduğu esnek bir yapıya sahip yönlendirme paketidir.React ile birlikte gelen
dahili paketlerden değil harici kütüphanelerdendir.

Kurulum için https://reactnavigation.org/ sitesinden gerekli adımar uygulanarak faydalanılabilir.<br/>
"npm/yarn install @react-navigation/native" ile kurulumu gerçekleştirebiliriz. <br/>
"npm install react-native-screens react-native-safe-area-context" sırasıyla bu kodu çalıştıralım. <br/>
"npx pod-install ios" Eğer "ios/Mac" kullanıcıysanız bu kodu çalıştırınız.Android için gerekli değildir. <br/>
Android cihazlar için "android/app/src/main/java/MainActivity.java" dizinini takip ediniz.Ardından <br/>
"@Override
protected void onCreate(Bundle savedInstanceState) {
  super.onCreate(null);
}"  kodu yapıştırınız ve en üste "import android.os.Bundle;" ekleyiniz.

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

Eskiden react-navigation kurulumunda stack-tab-drawer kurulu geliyordu.Fakat gereksiz kullanım ve performans <br/>
kazanımı için ayrı ayrı kuruluma geçildi. <br/>

"npm install @react-navigation/native-stack" ile sayfadan sayfaya geçiş işlemi yapabiliriz.


Sayfalar arası veri transferi yapmak uygundur.Bunu props mantığıyla bir json obje formatında diğer sayfalara aktarabiliriz.Görüntülemek istediğimiz sayfada "props.route.params" ile yakalayıp görüntüleyebiliriz.