 <h3> SQL INJECTION NEDİR ? </h3>
<hr />
<ul>
  <li> SQL enjeksiyonu, SQL sorgularını dinamik olarak zehirleyerek veritabanı sunucularını ele geçirmek için kullanılan bir saldırıdır.
</li>
</ul>


 <h3> SQL INJECTION ENGELLEMEK İÇİN YAPILABİLECEKLER ? </h3>
 
 
 
 <ul>
   <li> 
	QueryString Kullanımlarında karşımıza çıkan sorunlardan kaynaklı olarak günümüzde bu zaafiyet genellikle gün yüzüne çıkmaktadır. Bu durumu engellemek için günümüzde ORM cihazları tercih edilmektedir.
	</li>
	<li>
		Sql parametreleri programlamadaki değişkenler gibi düşünülebilirler. Sql sorgusuna çalışma zamanında kontrollü biçimde yerleştirilirler.
		<p style="color:red;"> "SELECT * FROM Users WHERE UserId = @0";</p>
	</li>
	<li>
		Saklı yordamlar (SP), geliştiricinin bir yürütme planı oluşturmak için bir veya daha fazla SQL ifadesini mantıksal bir birime gruplandırmasını gerektirir. Sonraki yürütmeler, ifadelerin otomatik olarak parametreleştirilmesine izin verir. Basitçe söylemek gerekirse, daha sonra saklanabilen ve birçok kez kullanılabilen bir kod türüdür.Bu nedenle, sorguyu yürütmeniz gerektiğinde, tekrar tekrar yazmak yerine, saklı yordamı çağırabilirsiniz. 
	</li>
	<li>
		Her bir veritabanı yönetim sistemi (DBMS) tarafından sağlanan kullanıcı tarafından sağlanan giriş için her zaman karakterden kaçan(Escaping) işlevleri kullanın. Bu, DBMS'nin asla geliştirici tarafından sağlanan SQL ifadesiyle karıştırılmamasını sağlamak için yapılır.
	</li>
	<li>
		Kök erişimi olan bir hesap kullanarak uygulamanızı veritabanına bağlamayın. Saldırganlar tüm sisteme erişebileceğinden, bu yalnızca kesinlikle gerekliyse yapılmalıdır. Yönetimsel olmayan hesaplar sunucusu bile bir uygulama üzerinde risk oluşturabilir, hatta veritabanı sunucusu birden fazla uygulama ve veritabanı tarafından kullanılıyorsa daha da fazla risk oluşturabilir.

Bu nedenle, uygulamayı SQL enjeksiyonuna karşı savunmak için veritabanında en az ayrıcalık uygulamak daha iyidir. Her uygulamanın kendi veritabanı kimlik bilgilerine sahip olduğundan ve bu kimlik bilgilerinin uygulamanın ihtiyaç duyduğu minimum haklara sahip olduğundan emin olun.

Hangi erişim haklarını elinizden almanız gerektiğini belirlemeye çalışmak yerine, uygulamanızın ihtiyaç duyduğu erişim haklarını veya yükseltilmiş izinleri belirlemeye odaklanın. Bir kullanıcının yalnızca bazı parçalara erişmesi gerekiyorsa, bu işleve kesinlikle hizmet eden bir mod oluşturabilirsiniz.
	</li>
	<li>
		SQL enjeksiyon saldırılarını belirlemeye yönelik en iyi uygulamalardan biri, bir web uygulaması güvenlik duvarına (WAF) sahip olmaktır. Web sunucularının önünde çalışan bir WAF, web sunucularına giren ve çıkan trafiği izler ve tehdit oluşturan kalıpları belirler. Esasen, web uygulaması ile İnternet arasına konulan bir engeldir.

Bir WAF, tanımlanmış özelleştirilebilir web güvenlik kuralları aracılığıyla çalışır. Bu politika grupları, WAF'a hangi zayıflıkları ve trafik davranışını araması gerektiğini bildirir. Dolayısıyla, bu bilgilere dayanarak, bir WAF, kötü niyetli trafiği bulmak ve engellemek için aldığı uygulamaları ve GET ve POST isteklerini izlemeye devam edecektir.

Bir WAF'nin değeri, kısmen ilke değişikliğinin uygulanabilme kolaylığından gelir. Kısa sürede yeni politikalar eklenebilir, bu da hızlı kural uygulamasına ve hızlı olay yanıtına olanak tanır.
	</li>
</ul>
<p> Herhangi bir başka görüşe sahip iseniz <a href="https://www.linkedin.com/in/sefa-dudu-320a93205/">Buradan</a> benimle iletişime geçebilirsiniz.
