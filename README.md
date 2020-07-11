## IV. Hafta Ödevleri:
- [ ] Geri dönen bilgiye göre yeşil renkte onay mesajı gösterilmesi. (örneğin:view bag)
- [ ] AddMVC - AddMVCCore - AddDateAnnotations nedir? Nerelerde eklenmelidir?
- [ ] Snapshot nedir? nasıl değişir? neden alınır?
- [ ] Jquery Calender--> [Datapicker](https://jqueryui.com/datepicker/) --> DueAt'i takvim tipinde eklemek nasıl yapılır? Araştırınız. (DateTimeUffset tipinden atamalar oluşucak)
- [ ] First- FirstOrDefault ve Single- SingleOrDefault nedir? Aralarındaki farkı araştırınız.
- [ ] En kısa null check nasıl yapılır?
- [ ] Partial View nedir?
- [ ] Farklı authentication bulup,aynı işleri farklı yollar ile yapanları araştırınız.
- [ ] Razor Pages/MVC Projects karşılaştırmasını yapınız.

#### AddMvc, AddMvcCore nedir?
AddMvcCore () ve AddMvc (), MVC hizmetlerini daha fazla yapılandırmak için kullanılabilecek bir IMvcBuilder döndürür.
AddMvcCore (), adından da anlaşılacağı gibi, yanlizca MVC çekirdek bileşenlerini ekler. Projeniz için gerekli katmanlar varsa kendiniz eklemeniz gerekmektedir.
AddMvc () dahili olarak AddMvcCore () öğesini çağırır ve Razor görünüm motoru, JSON formatlayıcılar, CORS vb. Gibi diğer ara katman yazılımlarını ekler.

#### AddDataAnnotation Nedir?
MVC uygulamasında veri tabanı tablolarını Code First yöntemi ile oluşturmaya başladığımızda yapılan validasyon işlemlerine Data Annotations denir.

#### Snapshot nedir? nasıl değişir? neden alınır?
snapshot’ı kısa süreli çalışmalar öncesinde backup almak yerine snapshot’ı kullanabiliriz. Snapshot sayesinde sanal makinamızın anlık ekran görüntüsü alınır ve siz herhangi bir sebepten dolayı sanal makina üzerinde yaptığınız işlemleri geri almak istediğinizde almış olduğunuz snapshot’a revert diyerek eski haline geri dönüş yapabilirsiniz.

#### Jquery Calender
Bu [link üzerinden](https://stackoverflow.com/questions/38711170/datetimeoffset-in-fullcalendar-using-asp-net-mvc) incelenebilir:

#### First- FirstOrDefault ve Single- SingleOrDefault nedir? 
SingleOrDefault: Eğer dizi içinden sadece bir tane sayı seçmek istiyorsak ve seçim şartımız sağlanmıyorsa, bu durumda int tipinin varsayılan değeri olan 0(sıfır) döndürülsün istiyorsak SingleOrDefault seçimini kullanmalıyız.
Single: Eğer seçimimiz sonucunda sadece bir tane eleman geleceği garanti ise, bu durumda Single seçimini kullanabiliriz. Eğer şartımızı sağlayan hiçbir eleman dönmezse veya şartımızı sağlayan birden fazla eleman dönerse, bu iki durumda da istisnalar fırlatılacak ve hata ile karşılaşmış olacağız.
FirstOrDefault: Bu seçimde de mantık SingleOrDefault ile aynıdır. Ancak bu seçimde istenen şartta ilk eleman seçilir. Örneğin dizinin ilk elemanı, dizinin 2’den büyük ilk elemanı gibi.
First: Mantık Single ile aynıdır, ancak seçilen ilk elemandır.

#### En kısa null check nasıl yapılır?
String.IsNullOrEmpty(String) kullanılarak yapılır. Belirtilen dizenin null mi yoksa boş bir dize mi ("") olduğunu gösterir.

#### Partial View nedir?
Asp.net MVC Partial View kullanımı, büyük web projelerinde arayüzü yönetmek için başvurabileceğiniz yöntemlerden birisidir. Layout ile sayfaların genel iskeletini oluşturup daha optimal bir arayüz elde ederken, Partial View kullanımı ile arayüzü modüler bir hale getirebilirsiniz. Örneğin sitenizde yayınladığınız reklamları daha kolay bir şekilde diğer dosyalardan ve _Layout.cshtml dosyasından bağımsız bir şekilde yönetebilirsiniz.

#### Razor Pages/MVC Projects
Razor Pages, asp.net core 2 ile birlikte gelen yeni bir özellik. Daha önce kullandığımız asp.net web forms çatısına yaklaşım olarak benzemekle birlikte klasik asp.net webforms’u kullanmadan asp.net mvc üzerine geliştirilmiştir. Razor Pages, sayfa bazlı senaryolar için bildiğimiz mvc (model view controller)’a göre daha kolay uygulama geliştirmeyi sağlayan bir platformdur. Frontend çatılarda kullanılan yaklaşım olan mvvm (model view view model) yapısına benzeşen çift yönlü bağlantı (two way binding) özelliğini desteklemektedir. Razor Pages’in tek sorumluluk prensibine (single responsibility) uygun bir yaklaşımı vardır.
