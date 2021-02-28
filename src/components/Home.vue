<template>
  <div class="hello">
      <header class="header">
            <div class="header__item">
                <img src="../assets/Img/top-logo-zepter.svg" height="64" alt="">
            </div>
        </header>
        <section class="container">
                <img src="../assets/Img/cookArt_RU.jpg" class="img" alt="">
        </section>
        <section class="container">
            <div class="wrapper">
                <p class="b-text">
                    Жақсы өмір сүріңіз  <br> Ұзақ өмір сүріңіз
                </p>
                <span class="line"></span>
            </div>
            <div class="wrap">
                <div class="wrap__info wrap__item">
                    <h1 class="logo__text">Қош келдіңіздер</h1>
                    <h1 class="bw-text">Біз сіздің армандарды іске асырудамыз</h1>
                    <p class="text">Zepter International – бұл негізінен тікелей сату жолымен, сондай-ақ бөлшек сауда желісі арқылы бүкіл әлем бойынша эксклюзивті, жоғары сапалы тұтыну тауарларын өндіретін және сататын мультибрендті халықаралық компания.
                                    Қаржы, банкітк және сақтандыру салаларында жұмыс жасайтын компания, Zepter Finance Holding AG компаниясымен бірге Zepter International Zepter Groupтің бір бөлігі болып табылады.</p>
                    <p class="link__text">Көбірек білу</p>
                </div>
                <div class="img wrap__item">
                    <img src="../assets/Img/home2.jpg" alt="">
                </div>
                <div class="img wrap__item">
                    <img src="../assets/Img/home3.jpg" class="image" alt="">
                </div>
            </div>
        </section>
        <section class="container">
            <div class="wrapper">
                <span class="line"></span>
                <p class="logo__text">Тауарлар</p>
                <h1 class="bw-text">Біздің өнімдер</h1>
                <div class="wrap">
                    <div class="btn" id="btn" @click="showProducts('Денсаулық')">Денсаулық</div>
                    <div class="btn" id="btn" @click="showProducts('Косметика')">Ас үй аспаптары</div>
                    <div class="btn" id="btn" @click="showProducts('Үй құралдары')">Үй құралдары</div>
                </div>
            </div>
            <div class="wrap cards" id="cards">
                <div class="card__item" v-for="(item,index) in cosmetic" :key="index" v-show="cosmetics">
                    <div class="card__descript">{{item.description}}</div>
                    <div class="img__wrap">
                        <img :src="item.img" id="cosm" class="card__img" alt="">
                    </div>
                    <div class="card__info">
                        <h1 class="card__head">{{item.title}}</h1>
                        <h3 class="card__option">{{item.option}}</h3>
                        <p class="card__text">{{item.amount | amountShow }}</p>
                    </div>
                </div>
                <div class="card__item" v-for="(item,index) in health" :key="index" v-show="healths">
                    <div class="card__descript">{{item.description}}</div>
                    <div class="img__wrap">
                        <img :src="item.img" id="heal" class="card__img" alt="">
                    </div>
                    <div class="card__info">
                        <h1 class="card__head">{{item.title}}</h1>
                        <h3 class="card__option">{{item.option}}</h3>
                        <p class="card__text">{{item.amount | amountShow}}</p>
                    </div>
                </div>
                <div class="card__item" v-for="(item,index) in home" :key="index" v-show="homes">
                    <div class="card__descript">{{item.description}}</div>
                    <div class="img__wrap">
                        <img :src="item.img" id="home" class="card__img" alt="">
                    </div>
                    <div class="card__info">
                        <h1 class="card__head">{{item.title}}</h1>
                        <h3 class="card__option">{{item.option}}</h3>
                        <p class="card__text">{{item.amount | amountShow}}</p>
                    </div>
                </div>
            </div>
        </section>
        <section class="container">
            <div class="wrap__line">
                <span class="line"></span>
            </div>
            <div class="compain__info">
                <div class="compain__item">
                    <img src="../assets/Img/icons2/profile.png" class="icon" alt="">
                    <h1 class="bw-text w-text">80.000.000+</h1>
                    <h1 class="logo__text a-text">Пайдаланушылар</h1>
                </div>
                <div class="compain__item">
                    <img src="../assets/Img/icons2/shop.png" class="icon" alt="">
                    <h1 class="bw-text w-text">60+</h1>
                    <h1 class="logo__text a-text">Елдердегі <br> дүкендер</h1>
                </div>
                <div class="compain__item">
                    <img src="../assets/Img/icons2/trophy.png" class="icon" alt="">
                    <h1 class="bw-text w-text">8</h1>
                    <h1 class="logo__text a-text">Алынған <br> марапаттар</h1>
                </div>
                <div class="compain__item">
                    <img src="../assets/Img/icons2/confetti.png" class="icon" alt="">
                    <h1 class="bw-text w-text">25</h1>
                    <h1 class="logo__text a-text">Қызмет <br> жылдары</h1>
                </div>
            </div>
        </section>
        <section class="container">
            <div class="wrap">
                <span class="line"></span>
            </div>
            <div class="wrap">
                <div class="about__item">
                    <img src="../assets/Img/cepter.jpg" alt="">
                </div>
                <div class="about__item">
                    <h1 class="b-text">Компания туралы</h1>
                    <p class="text about__text">
                        <div class="m__wrap">
                            <img src="../assets/Img/icons2/book-mark.png" class="icon__smart" alt="">
                            Zepter International – бұл негізінен тікелей сату жолымен, сондай-ақ бөлшек сауда желісі арқылы бүкіл әлем бойынша эксклюзивті, жоғары сапалы тұтыну тауарларын өндіретін және сататын мультибрендті халықаралық компания.
                        </div>
                        <div class="m__wrap">
                            <img src="../assets/Img/icons2/book-mark.png" class="icon__smart" alt="">
                            Қаржы, банкітк және сақтандыру салаларында жұмыс жасайтын компания, Zepter Finance Holding AG компаниясымен бірге Zepter International Zepter Groupтің бір бөлігі болып табылады.
                            Өзінің құрылу сәтінен бастап Zepter International сапаның өте жоғары стандарттарын орнатты және бүкіл әлемдегі миллиондаған адамдардың өмірінің ажырамас бөлігі болды.
                        </div>
                        <div class="m__wrap">
                            <img src="../assets/Img/icons2/book-mark.png" class="icon__smart" alt="">
                        Әлемде әрбір 10 секунд сайын Zepter өнімінің жаңа презентациясы басталады, өйткені Zepter компаниясы 60 елден астам жерде 5 құрлықта ұсынылған.
                        </div>
                        <div class="m__wrap">
                            <img src="../assets/Img/icons2/book-mark.png" class="icon__smart" alt="">
                        Zepter International компаниясына Швейцарияда, Германияда және Италияда 7 зауыт тиесілі, сондай-ақ әлемнің ең ірі мегаполистарында 320 000 м2 астам бизнес-кеңістік тиесілі.       
                        Соңғы 25 жыл өте сәтті болды: 80 000 000 астам адам Zepter өнімінің разы тұтынушылары атанды.
                        </div>
                        <div class="m__wrap">
                            <img src="../assets/Img/icons2/book-mark.png" class="icon__smart" alt="">
                        <p>Zepter көрінуі, тамаша сапа, инновациялық өнімдер және бүкіл әлемде 100 000 астам қызметкерлері және консультанттары бар сатудың бірегей жүйесі – бұл Zepter компаниясының жетістіктерінің негізі. Zepter оларды денсаулық пен сұлулықтың ғаламдық міндеті шабыттандыратын өзінің керемет дайындалған және жоғары дәлелді сату жөніндегі менеджерлерімен және консультанттарымен мақтанады:</p>
                        </div>
                </div>
            </div>
        </section>
        <section class="container">
            <div class="wrap">
                <span class="line"></span>
            </div>
            <div class="wrapper">
                    <h1 class="b-text">МИССИЯ</h1>
                    <div class="mission__container">
                        <div class="mission__info borders text">Zepter денсаулық миссиясы бес құрлыққа таралады. Жылдар өткен сайын ол дүние жүзі бойынша миллиондаған адамдардың өмір сүру сапасын жақсы жағына қарай өзгертуде. Өмірді қорғау бойынша өткізіліп жатқан бұл жаһандық кампания барлығын да қамтиды: оған білікті менеджерлердің жаңа ұрпағына үздіксіз білім беру және жұмысқа орналастыру, жоғары сапалы өнімді шығару мен тарату, сондай-ақ түрлі қаржы және сақтандыру қызметтерін талдау, жоспарлау және тарату кіреді.</div>
                        <div class="mission__info">
                            <img src="../assets/Img/icons2/number.png" class="icon__num" alt="">
                        </div>
                    </div>
                    <div class="mission__container">
                        <div class="mission__info"><img src="../assets/Img/icons2/number2.png" class="icon__num" alt=""></div>
                        <div class="mission__info l-borders text">Филип Цептер мырзаның тамаша идеясының арқасында пайда болған ізгі миссия бүкіл әлем бойынша жұмыс істейтін Zepter International қызметкерлерін бизнес туралы өз білімдерін үнемі арттыру және неғұрлым жоғары стандарттарға ұмтылу үшін, өз жақындарын ұзақ жылдар бойы дендері сау және бақытты етуге қанаттандырды. Zepter-дің өнімдері мен қызметтерін күнделікті өмірде пайдалануды бастай отырып, миллиондаған адамдардың денсаулықтары жақсарып, бақытты адамдарға айналды, ал жүздеген және мыңдаған адамдар Zepter табысының айрықша жүйесін басшылыққа ала отырып, өздерінің кәсіби менмендігін қанағаттандыруға қол жеткізді.</div>
                    </div>
                    <div class="mission__container">
                        <div class="mission__info borders text">«Табыс – бұл дені сау адам мен жоғары рухтың өзара тығыз іс-қимыл жасауының қалыпты нәтижесі. Денсаулық мықты болу үшін өзіңнің рухани және күш-жігер әлеуетіңді іске асыру керек. Денсаулықтың бұл түрі – аяққы мақсат, өйткені ол барлық қалған нәрселер үшін алғышарт болып табылады. Осыған қол жеткізген адам үшін ешқандай шектеу болмайды».
                            Филип Цептер</div>
                        <div class="mission__info"><img src="../assets/Img/icons2/number3.png" class="icon__num" alt=""></div>
                    </div>
                    <div class="mission__container">
                        <div class="mission__info"><img src="../assets/Img/icons2/number4.png" class="icon__num" alt=""></div>
                        <div class="mission__info l-borders text">ҚОРШАҒАН ОРТА ҮШІН ҚАУІПСІЗ ӨНІММЕН, САҚТАНДЫРУ ҚЫЗМЕТТЕРІМЕН ЖӘНЕ ЭКОЛОГИЯЛЫҚ САУАТТЫЛЫҚПЕН ҚОЛДАУ КӨРСЕТІЛЕТІН ДЕНСАУЛЫҚ, СҰЛУЛЫҚ ЖӘНЕ АДАМДАРДЫҢ ЖАҚСЫ КӨҢІЛ-КҮЙІ – МІНЕ, ZEPTER GROUP-ТІҢ ҰЗАҚМЕРЗІМДІ ҰМТЫЛЫСТАРЫ ОСЫЛАР.</div>
                    </div>
            </div>
        </section>
        <section class="container">
            <div class="wrapper">
                <span class="line"></span>
                <h1 class="bw-text">Біздің орналасқан жеріміз
                </h1>
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d5772.2028514555!2d51.15692752822399!3d43.66686037737684!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x41b4310ac2225b7b%3A0xb9ec5c5b8d4d075a!2z0JzQuNC60YDQvtGA0LDQudC-0L0gMjcsINCQ0LrRgtCw0YM!5e0!3m2!1sru!2skz!4v1614274477103!5m2!1sru!2skz"  style="border:0;" class="map" allowfullscreen="" loading="lazy"></iframe>
            </div>
        </section>
        <section class="container">
            <div class="wrapper">
                <img src="../assets/Img/Endre-bestilling-eller-avbestille-2048x1005.jpg" class="img__msg" alt="">
                <div class="message__info">
                    <p class="bw-text w-text m__wrap msg__text">Бізбен хабарласу</p>
                    <div class="btn m__wrap"><a href="https://wa.me/77713620001" class="link">WhatsApp ка жазу</a></div>
                </div>
            </div>
        </section>
        <footer class="footer">
            <div class='footer__item'>
                <div class="social">
                    <h1>Әлеуметтік желілер</h1>
                    <li class="social__item"><img src="../assets/Img/icons/facebook (1).png"  class="icons" alt=""><span class="span">Facebook</span></li>
                    <li class="social__item"><img src="../assets/Img/icons/whatsapp.png" class="icons"  alt=""> <span class="span">WhatsApp</span></li>
                    <li class="social__item"><img src="../assets/Img/icons/instagram.png"  class="icons" alt=""> <span class="span">Instagram</span></li>
                </div>
                <p>«Табыс – бұл дені сау адам мен жоғары рухтың өзара тығыз іс-қимыл жасауының қалыпты нәтижесі. Денсаулық мықты болу үшін өзіңнің рухани және күш-жігер әлеуетіңді іске асыру керек. Денсаулықтың бұл түрі – аяққы мақсат, өйткені ол барлық қалған нәрселер үшін алғышарт болып табылады. Осыған қол жеткізген адам үшін ешқандай шектеу болмайды». <br>Филип Цептер.</p>
            </div>
            <div class="footer__item">
                <h1 class="b-text">Бізбен байланыс</h1>
                <p>+7 (885) 589 69 85</p>
                <p>Zepter@info.com</p>
                <p>Казахстан, г.Актау мкр 27-22-15</p>
            </div>
        </footer>    
  </div>
</template>

<script>



export default {
    name: 'home',
    beforeCreated(){
        this.showProducts("Косметика");
    },
    data:()=>{
        return{
          cosmetics:true,
          healths:false,
          homes:false,
          cosmetic : [
              {
                  title:'КАСТРЮЛЯ, 5 Л, Ø28 СМ',
                  img:    require('../assets/Img/kitchen/ImageHandler3.png'),
                  option:'ПРИГОТОВЛЕНИЕ',
                  amount:203040,
                  description:`Наслаждайтесь бесконечным количеством рецептов: рагу, карри, ризотто и морепродукты со второй по величине 5-литровой кастрюлей 28 см в диаметре.`
                  
              },
              {
                  title:'СИСТЕМА ДЛЯ ПРИГОТОВЛЕНИЯ НА ПАРУ, 4л',
                  img:    require('../assets/Img/kitchen/ImageHandler4.png'),
                  option:'ПРИГОТОВЛЕНИЕ',
                  amount:71910,
                  description:`Хотя, используя посуду Zepter Masterpiece вы уже можете оценить ее непревзойденные свойства - приготовление пищи без воды и при низких температурах, есть определенные продукты, приготовление которых требует дополнительных навыков- шпинат спаржа, нежное филе рыбы, пельменей.`
              },
              {
                  title:'КРЫШКА SYNCRO-CLIK, Ø20 СМ',
                  img:    require('../assets/Img/kitchen/ImageHandler5.png'),
                  option:'ПРИГОТОВЛЕНИЕ',
                  amount:127370,
                  description:`Оснащенная дополнительной системой безопасности, крышка Syncro-Clik® превращает вашу посуду Masterpiece от Zepter в функциональную, полезную систему приготовления под давлением.`
              },
              {
                  title:'НАБОР PRINCE ДЛЯ ЛИКЕРА (6 ПРЕДМЕТОВ)',
                  img:require('../assets/Img/kitchen/ImageHandler.png'),
                  option:'СТОЛОВАЯ ПОСУДА',
                  amount:164500,
                  description:`Для повседневного использования или для особых моментов - Prince придает элегантность любым случаям. Когда ваши друзья и семья собираются, чтобы поднять бокал, отметьте это событие незабываемо с бокалами из нержавеющей стали Prince для ликера.`
              },
              {
                  title:'НАБОР PRINCE (25 ПРЕДМЕТОВ), ПОЛНАЯ ПОЗОЛОТА',
                  img:require('../assets/Img/kitchen/ImageHandler1.png'),
                  option:'СТОЛОВАЯ ПОСУДА',
                  amount:2223100,
                  description:`Для повседневного использования или для особых моментов - Prince придает элегантность любым случаям.`
              },
              {
                  title:'НАБОР PRINCE ДЛЯ ЛИКЕРА (6 ПРЕДМЕТОВ), ПОЛНАЯ ПОЗОЛОТА"',
                  img:require('../assets/Img/kitchen/ImageHandler2.png'),
                  option:'СТОЛОВАЯ ПОСУДА',
                  amount:415950,
                  description:`Для повседневного использования или для особых моментов - Prince придает элегантность любым случаям.`
              }
          ],
          health : [
              {
                  title:'БИОПТРОН МЕДОЛЛ СО СТОЙКОЙ',
                  img:require('../assets/Img/health/ImageHandler.png'),
                  option:'СВЕТОТЕРАПИЯ',
                  amount:590790,
                  description:`Компактный прибор подходит для применения как в домашних условиях, так и в медицинских учреждениях. Диаметр фильтра составляет 5 см, имеется таймером, позволяющий точно выставить время сеанса. `
                  
              },
              {
                  title:'СТЕРИЛЬНЫЙ БИОПТРОН ОКСИ-СПРЕЙ',
                  img:require('../assets/Img/health/ImageHandler1.png'),
                  option:'СВЕТОТЕРАПИЯ',
                  amount:7050,
                  description:`Уникальный стерилизованный, насыщенный кислородом водяной спрей из Швейцарии для придания максимальной свежести. `
              },
              {
                  title:'БИОПТРОН PRO1 С НАСТОЛЬНОЙ СТОЙКОЙ',
                  img:require('../assets/Img/health/ImageHandler2.png'),
                  option:'СВЕТОТЕРАПИЯ',
                  amount:1170300,
                  description:`Средняя по диаметру фильтра модель прибора БИОПТРОН, сочетающая мобильность и функциональность. Для использования как в домашних, так и в профессиональных условиях. `
              },
              {
                  title:'ФИЛЬТР КРАСНЫЙ ДЛЯ BIOPTRON PRO1',
                  img:require('../assets/Img/health/ImageHandler3.png'),
                  option:'СВЕТОТЕРАПИЯ',
                  amount:58280,
                  description:`Красный — это теплый цвет с самой длинной волной в видимом спектре. Красный свет оказывает стимулирующее воздействие как на нашу психическую, так и на физическую энергию. `
              },
              {
                  title:'ОЧИСТКА ВОЗДУХА THERAPY AIR® ION',
                  img:require('../assets/Img/health/ImageHandler4.png'),
                  option:'СВЕТОТЕРАПИЯ',
                  amount:419710,
                  description:`TherapyAir iOn — это сложная и высокоэффективная система очистки и ионизации воздуха, которая удаляет 99,99% взвешенных в воздухе частиц. Очищенный на 99,99% лечебный воздух, свободный от вирусов, бактерий.`
              },
              {
                  title:'ФИЛЬТР ЖЕЛТЫЙ ДЛЯ BIOPTRON PRO1',
                  img:require('../assets/Img/health/ImageHandler5.png'),
                  option:'СВЕТОТЕРАПИЯ',
                  amount:58280,
                  description:`Цель Цветотерапии Bioptron - помочь восстановить душевное, эмоциональное и физическое равновесие в организме. Цветотерапия Bioptron безопасна и проста в использовании в любом месте в любое время. Желтый цвет производит яркое и радостное впечатление.
                  `
              }
          ],
          home : [
              {
                  title:'МАГНИТНЫЙ УМЯГЧИТЕЛЬ ВОДЫ CLEANSYMAG',
                  img:require('../assets/Img/Home/ImageHandler.png'),
                  option:'УМЯГЧИТЕЛЬ ВОДЫ',
                  amount:84600,
                  description:`Инновационный магнитный умягчитель воды способен повысить качество вашей жизни. Устройство CleanSymag через катушку (спец. провода, входящие в комплект) создает электромагнитное поле, воздействующее на воду, протекающую в трубе. `
                  
              },
              {
                  title:'TUTTOSTEAMY GOLD - ЭФФЕКТИВНЫЙ ПАРООЧИСТИТЕЛЬ И МОЩНЫЙ ПАРОВОЙ УТЮГ',
                  img:require('../assets/Img/Home/ImageHandler1.png'),
                  option:'БЫТОВАЯ ТЕХНИКА',
                  amount:413600,
                  description:`TUTTOSTEAMY – это инновационный прибор от ZEPTER, объединяющий 2 устройства в 1 - эффективный пароочиститель (148°C) и мощный паровой утюг. TUTTOSTEAMY позволяет легко и быстро избавиться от пыли, грязи, пылевых клещей и любых других микроорганизмов, живущих в вашем доме, не прибегая при этом к дорогим и вредным химическим средствам. `
              },
              {
                  title:'СИСТЕМА ОЧИСТКИ ВОДЫ EDELWASSER, ЧЕРНЫЙ ЦВЕТ',
                  img:require('../assets/Img/Home/ImageHandler2.png'),
                  option:'ФИЛЬТРЫ ДЛЯ ВОДЫ',
                  amount:313490,
                  description:`5-ступенчатая система очистки воды на основе самой эффективной технологии обратного осмоса. Система не требует подключения к электрической сети и великолепно справляется с очисткой воды тогда, когда Вам это необходимо. `
              },
              {
                  title:'ГЛАДИЛЬНАЯ ДОСКА/СТРЕМЯНКА CLEANSY ACROBAZ',
                  img:require('../assets/Img/Home/ImageHandler3.png'),
                  option:'БЫТОВАЯ ТЕХНИКА',
                  amount:69090,
                  description:`Красный — это теплый цвет с самой длинной волной в видимом спектре. Красный свет оказывает стимулирующее воздействие как на нашу психическую, так и на физическую энергию. `
              },
              {
                  title:'ПЫЛЕСОС-ПАРОГЕНЕРАТОР TUTTOLUXO 6S BLACK',
                  img:require('../assets/Img/Home/ImageHandler4.png'),
                  option:'БЫТОВАЯ ТЕХНИКА',
                  amount:925430,
                  description:`Мощная и интеллектуальная система 6 в 1, которая, благодаря сочетанию передовых технологий и естественной силе пара, легко и эффективно избавит ваш дом от грязи и пыли. Система TUTTOLUXO 6SB справится с уборкой любой поверхности и сделает ваш дом идеально чистым и безопасным!`
              },
              {
                  title:'СИСТЕМА ОЧИСТКИ ВОДЫ AQUEENAPRO',
                  img:require('../assets/Img/Home/ImageHandler5.png'),
                  option:'ФИЛЬТРЫ ДЛЯ ВОДЫ',
                  amount:662330,
                  description:`AqueenaPro – это высокотехнологичная система очистки воды, разработанная с использованием самой эффективной технологии обратного осмоса. 5-ти ступенчатая система фильтрации обеспечивает максимальную степень очистки от загрязняющих веществ, бактерий, вирусов и тяжелых металлов - вода становится кристально чистой и полезной.`
              }
          ]
        }
      },
      filters:{
          amountShow(msg){
              return msg + ".00" + ' KZT';
          }
      },
      methods:{
          showProducts(msg){
                if( msg === "Денсаулық"){
                    this.healths = true;
                    this.cosmetics = false;
                    this.homes = false;
                }else if(msg === "Косметика"){
                    this.healths = false;
                    this.cosmetics = true;
                    this.homes = false;
                }else{
                    this.homes = true;
                    this.healths = false;
                    this.cosmetics = false;
                }
            }
          }
    
}
</script>

<style scoped>
  html,body{
    width: 100%;
    margin: 0;
    padding: 0;
}
.header{
    display: flex;
}
.header__item{
    display: flex;
    justify-content: center;
    flex-basis: 100%;
    align-items: center;
}
.header__item:nth-child(2){
    justify-content: flex-start;
}
.menu__item{
    list-style: none;
    color: #000;
    transition: all .45s ease-in-out;
    cursor: pointer;
    margin: 0px 25px;
}
.menu__item:hover{
    color: #e23737;
}
.menu__item:nth-child(1){
    color: #e23737;
}
.container{
    margin: 50px 0px;
    max-width: 100%;
}
.img{
    max-height: 100%;
    max-width: 100%;
}
.wrapper{
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.wrap{
    display: flex;
    justify-content: space-around;
}
.b-text{
    font-family: 'Times New Roman', Times, serif;
    font-size: 50px;
    font-weight: 500;
    text-align: center;
}
.bw-text{
    font-family: 'Poppins', sans-serif;
    font-size: 40px;
    font-weight: 900;
}
.wrap__item{
    flex-basis: 33%;
    margin: 50px 0px;   
}
.w-text{
    color: #fff;
    margin: 0;
}
.wrap__item:nth-child(2){
    display: flex;
    justify-content: center;
}
.wrap__item:nth-child(3){
    display: flex;
    justify-content: center;
}
.logo__text{
    font-family: Georgia, 'Times New Roman', Times, serif;
    color: #e23737;
    font-weight: bold;
    letter-spacing: 5px;
}
.a-text{
    text-align: center;
}
.line{
    display: block;
    height: 100px;
    width: 2px;
    background-color: red;
    margin: 20px 0px;
}
.container:nth-child(3){
    padding: 0px 10% 0px 15%;
}
.text{
    font-family: 'Times New Roman', Times, serif;
    font-size: 17px;
    line-height: 25px;
}
.link__text{
    font-family: 'Times New Roman', Times, serif;
    
    font-size: 20px;
    cursor: pointer;
    color: #000;
    transition: all 1s ease-in-out;
}
.link__text:hover{
    transform: translateX(15px);
    color: #e23737;
}
.btn{
    height: 50px;
    width: 250px;
    border: 1px solid #e23737;
    color: #fff;
    transition: all .55s ease-in-out;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    background-color: #e23737;
}
.btn:hover{
    background-color: #991212;
}
.cards{
    perspective: 1000px;
    flex-wrap: wrap;
    padding: 0px 15%;
    margin: 100px 0px 0px 0px;
}
.link{
    text-decoration: none;
    color: #fff;
    transition: all .45s ease-in-out;
}
.card__item{
    border-radius: 10px ;
    flex-basis: 30%;
    align-items: center;
    justify-content: space-around;
    position: relative;
    margin: 20px;
    box-shadow: 0px 0px 30px 3px rgb(145, 145, 145);
    animation: Animate .65s ease-in-out;
}
.card__info{
    display: flex;
    flex-direction: column;
    padding: 20px 10px;
}
.card__descript{
    position: absolute;
    top:1%;
    left:5%;
    height: auto;
    width: 50%;
    background-color: #e23737;
    color: #fff;
    padding: 30px;
    border-bottom-right-radius: 50px;
    border-top-left-radius: 50px;
    opacity: 0;
    transition: all .65s ease-in-out;

}
.card__head{
    margin: 0;
    text-transform: capitalize;
    font-size: 18px;
}
.card__option{
    font-size: 14px;
    color: #e23737;
}
.card__text{
    font-size: 18px;
    color: rgb(145, 145, 145);
}
.card__img{
    height: 300px;
    width: 300px;
}
.img__wrap{
    width: 100%;
    background-color: rgb(238, 238, 238);
    display: flex;
    justify-content: center;
}
.card__item:hover .card__descript{
    opacity: 1;
}
.footer{
    display: flex;
    max-width: 100%;
    background-color: #e23737;
    color: #000;
    font-weight: bold;
    font-family: 'Poppins', sans-serif;
    justify-content: space-around;
    padding: 100px 10% ;
    align-items: center;
}
.footer__item{
    flex-basis: 50%;
    display: flex;
    font-size: 18px;
    flex-direction: column;
}
.footer__item:nth-child(2){
    align-items: center;
}   
.social{
    display: flex;
    flex-direction: column;
}
.social__item{
    list-style: none;
    display: flex;
    cursor: pointer;
}
.icon{
    padding: 0px 10px;
    margin: 50px 0px;
}
.span{
    font-family: 'Times New Roman', Times, serif;
    font-size: 20px;
    margin: 0px 10px;
}
.map{
    width:800px;
    height:450px;
    border-radius: 10px;
    /* box-shadow: 0px 10px 40px 20px rgba(0,0,0,.45); */
}
.wrap__line{
    max-width: 100%;
    display: flex;
    justify-content: center;
}
.compain__info{
    display: flex;
    justify-content: space-around;
    max-width: 100%;
    padding: 100px 10%;
    background-color: #171717;
    flex-wrap: wrap;
}
.compain__item{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    flex-basis: 25%;
}
.about__item{
    display: flex;
    flex-basis: 45%;
    justify-content: space-around;
    margin: 0px 2.5%;
}
.about__item:nth-child(2){
    flex-direction: column;
    align-items: center;
}
.about__text{
    display: flex;
    margin: 0px 210px;
}
.icon__smart{
    height: 24px;
    width: 24px;
}
.m__wrap{
    margin: 10px 0px;
}
.mission__info{
    width: 100%;
    flex-basis: 50%;
    display: flex;
    justify-content: center;
    padding: 25px 20px;
    align-items: center;
}
.icon__num{
    height: 84px;
    width: 84px;
}
.borders{
    border-right: 4px solid rgb(71, 198, 240);
    border-bottom:4px solid rgb(71, 198, 240);
}
.l-borders{
    border-left: 4px solid rgb(71, 198, 240);
    border-bottom:4px solid rgb(71, 198, 240);
}
.mission__container{
    width: 50%;
    display: flex;
    justify-content: center;
}
.message__info{
    position: absolute;
    top: 40%;
    left: 40%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
}
.msg__text{
    font-size: 40px;
}
.img__msg{
    width: 100%;
    max-height: 600px;
    object-fit: fill;
}

@keyframes Animate{
    0%{
        opacity: 0;
        transform: translateY(300px) ; 
    }100%{
        opacity: 1;
    }
}

@media screen and (max-width:1500px) {
    .wrap__item:nth-child(2){
        display: none;
    }
}
@media screen and (max-width:1250px) {
    .footer{
        flex-direction: column;
        align-items: flex-start;
    }
    .footer__item{
        max-width: 70%;
    }
}

@media screen and (max-width:990px) {
    .wrap:nth-child(2){
        flex-direction: column;
        text-align: center;
        justify-content: center;
    }   
    .wrap:nth-child(4){
        flex-direction: column;
        text-align: center;
        justify-content: center;
    }   
    .footer{
        align-items: center;
        padding: 100px  0px;
    }
    .map{
        max-width: 70%;
    }
}
@media screen and (max-width:700px) {
    .message__info{
        top: 30%;
        left: 20%;
    }
}
@media screen and (max-width:500px) {
    .message__info{
        top: 20%;
        left: 5%;
    }
    @keyframes Animate{
        0%{
            opacity: 0;
            transform: translateX(300px) ; 
        }100%{
            opacity: 1;
        }
    }
}

@media screen and (max-width:440px) {
    .cards{
        padding: 0;
    }
    .wrap__item{
        overflow: hidden;
    }
}
@media screen and (max-width:430px) {
    .msg__text{
        font-size: 25px;
    }
}
</style>
