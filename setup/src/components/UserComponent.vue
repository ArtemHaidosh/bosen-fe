<template>
    <div ref="download">
        <header>
            <div class="header-text">
                <h1>Bosen Group</h1>
                <h2>Najlepšia realitná kancelária</h2>
            </div>
        </header>

        <div class="container">
            <div class="user">
                <div class="header-img">
                    <img :src="user.photo_url" alt="1724682873955" border="0">
                </div>
                <h2>{{ user.first_name }} {{ user.last_name }} </h2>
                <p class="position">{{ user.position }}</p>
                <!-- мне нужно создать 4 кнопки полукругом с разными иконками -->
                <div class="buttons" ref="lol">
                    <button class="btn" @click="downloadPDF"><i class="fas fa-download"></i></button>
                    <a href="https://www.bosen.sk/" target="_blank"><button class="btn"><i
                                class="fas fa-globe"></i></button></a>
                    <div>
                        <button @click="isPopupVisible = true" class="btn"><i class="fas fa-qrcode"></i></button>
                        <div v-if="isPopupVisible" class="popup">
                            <div class="popup-content">
                                <span class="close" @click="isPopupVisible = false">&times;</span>
                                <h3>Scan QR Code</h3>
                                <qrcode-canvas :background="'#fff'" :foreground="'#000'" :value="url"></qrcode-canvas>
                                <p>{{ url }}</p>
                            </div>
                        </div>
                    </div>
                    <div>
                        <button @click="isSharePopupVisible = true" class="btn"><i class="fas fa-share"></i></button>
                        <div v-if="isSharePopupVisible" class="share-popup">
                            <div class="share-popup-content">
                                <span class="close" @click="isSharePopupVisible = false">&times;</span>
                                <h3>Copy link</h3>
                                <textarea>{{ url }}</textarea>
                                <br>
                                <button class="copy" @click="copyToClipboard"><i class="fas fa-copy"></i></button>
                            </div>
                        </div>
                    </div>
                </div>
                <ul class="custom-list">
                    <li><i class="fas fa-envelope special"></i>{{ user.email }}</li>
                    <li><i class="fas fa-phone special"></i> {{ user.phone }}</li>
                    <li><i class="fas fa-map special" ></i> {{ user.address }}</li>
                </ul>
                <div class="text">
                    <h2>O nás</h2>

                 <p>„Veríme, že náš výnimočný prístup, vytrvalosť a zmysel pre dizajn sú základnými prvkami pri vytváraní špičkovej služby. 
                    Sme hrdí na prácu, ktorú robíme a na klientov, ktorých zastupujeme“<br>

                    Bosen Real Estate Group je renomovanou realitnou kanceláriou na slovenskom realitnom trhu od roku 2014 s počtom viac ako 80 realitných maklérov. 
                    Sme progresívnou firmou, ktorá prináša inovatívne riešenia v prípade, že sa jedná o kúpu, predaj alebo prenájom nehnuteľnosti. 
                    Naša realitná kancelária pôsobí na celom území Slovenskej republiky s pobočkami v mestách Bratislava, Galanta, Lučenec, Malacky, Nitra, Šamorín a Trenčín.
                     V ponuke máme viac ako 500 nehnuteľností a prekročili sme hranicu 1200 úspešne realizovaných realitných obchodov v objeme viac ako 320 miliónov eur.</p><br>
                </div>
    <br><br>
    <div>
    <div class="header-text">
        <h1>NAŠA PONUKA</h1>
        <p class="position">Nehnuteľností | Novostavieb </p>
        <div class="img">
        <a href="https://www.bosen.sk/nehnutelnosti"><img src="https://i.ibb.co/QXSZ1Lq/ponuka-Bosen.png" alt="ponuka-Bosen"></a>
    </div>
    <a href="https://www.bosen.sk/nehnutelnosti" style="color: var(--orange)">Click to open the link...</a>
<br>
<br>
</div>
            </div>
            <div class="partneri">
                
                <div class="textF">
                    <h2>Partneri</h2>
                    <p>Našim cieľom je byť realitnou kanceláriou na najvyššej možnej úrovni, práve preto spolupracujeme len s overenými partnermi s dlhoročnými skúsenosťami vo svojom obore.
                        V prípade spolupráce s našimi partnermi získate výhodné podmienky a nadštandardný prístup.
                        Zabezpečíme Vám všetko "pod jednou strechou" tak, aby ste mali čo najmenej starostí.</p>
                        <ul>
                           <a href="https://www.bosen.sk/partneri"><img src="https://i.ibb.co/0XNnwF8/p1.jpg" alt="p1" border="0"></a>
                           <a href="https://www.bosen.sk/partneri"><img src="https://i.ibb.co/zsSTRDc/p2.jpg" alt="p2" border="0"></a>
                           <a href="https://www.bosen.sk/partneri"><img src="https://i.ibb.co/f8d6V2d/p3.jpg" alt="p3" border="0"></a>
                           <a href="https://www.bosen.sk/partneri"><img src="https://i.ibb.co/dKnmbSw/p4.jpg" alt="p4" border="0"></a>
                        
                           <a href="https://www.bosen.sk/partneri"><img src="https://i.ibb.co/XWqR0Zw/p6.jpg" alt="p6" border="0"></a>
                           <a href="https://www.bosen.sk/partneri"><img src="https://i.ibb.co/CJZXwYT/p7.jpg" alt="p7" border="0"></a>
                           <a href="https://www.bosen.sk/partneri"><img src="https://i.ibb.co/zs2wL4R/p8.jpg" alt="p8" border="0"></a>
                           <a href="https://www.bosen.sk/partneri"><img src="https://i.ibb.co/vBgCBJg/p9.jpg" alt="p9" border="0"></a>

                        </ul>
                    </div>
            </div>
            <div class="contact">
                <h2>Kontakt</h2>
                <img src="https://i.ibb.co/ZLnYVhB/image.png" alt="image" border="0"><br>
                <p>+421 910 777 796</p><br>
                <p>Ružinovská 42, 821 03 <br>
                    BRATISLAVA</p>
                    <a class="emphasis" href="mailto:info@bosen.sk"><p class="emphasis">info@bosen.sk</p></a>
                </div>
            </div>

<br><br><br>

        <footer>
                <p>© 2024 Bosen Real Estate Group</p><br>
                <p>Created by KHH team: Kozlov, Haidosh, Hryshchenko</p>
        </footer>
        </div>
    </div>
</template>

<script>
import '@fortawesome/fontawesome-free/css/all.css';
import '@fortawesome/fontawesome-free/js/all.js';
import html2pdf from 'html2pdf.js';
import axios from 'axios'
import { QrcodeCanvas } from 'qrcode.vue';

export default {
    data() {
        return {
            user: {},
            isPopupVisible: false,
            isSharePopupVisible: false,
            url: window.location.href,
            buttons : this.$refs.lol,


        }
    },

    watch: {
        '$route.params.id': 'fetchUser'
    },

    mounted() {
        this.fetchUser()
    },

    methods: {
        fetchUser() {
            const id = this.$route.params.id;
            axios.get('http://localhost:3000/api/realtors/' + id)
                .then(response => {
                    this.user = response.data
                    console.log(response.data)
                })
                .catch(error => {
                    console.log(error)
                })
        },
        async downloadPDF() {
            const element = this.$refs.download; // Reference to the template content
            const buttons = this.$refs.lol; // Reference to the buttons
            // Check if the element is defined
            if (!element) {
                alert('Content to print is not available!');
                return;
            }

            const userName = this.user.first_name; // Full name (e.g., "John Doe")
            const userSurname = this.user.last_name; // Extract surname (e.g., "Doe")
            const userInitial = userName.charAt(0).toLowerCase(); // First letter of the name (e.g., "j")

            if (buttons) {
                buttons.style.display = 'none'; // Скрываем кнопки
            }

            // Create the PDF filename based on initials and surname
            const pdfFilename = `${userInitial}${userSurname}.pdf`; // Example: "jdoe.pdf"
            const options = {
                margin: 0,
                filename: pdfFilename,
                image: { type: 'jpeg', quality: 0.98 },
                html2canvas: { scale: 4, useCORS: true },
                jsPDF: { unit: 'in', format: 'a4', orientation: 'portrait' }
            };

            console.log('Downloading PDF...');
            console.log('Options:', options);
            console.log('Element:', element);

            try {
                // Generate the PDF
                await html2pdf().from(element).set(options).save();
                alert('Your PDF is ready to download!');
            } catch (error) {
                console.error('Error generating PDF:', error);
                alert('Failed to generate PDF. Check the console for errors.');
            }

            if (buttons) {
                buttons.style.display = 'flex'; // Показываем кнопки
            }

        },
        copyToClipboard() {
            navigator.clipboard.writeText(this.url).then(() => {
                alert('Link copied to clipboard!');
            }, () => {
                alert('Failed to copy link to clipboard!');
            });
        }
    },
    components: {
        'qrcode-canvas': QrcodeCanvas
    }
}



</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=Dancing+Script:wght@400..700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Afacad+Flux:wght@100..1000&family=Kameron:wght@400..700&display=swap');
@import "../assets/main.css";

body, html {
  margin: 0;
  padding: 0;
  height: 100%;
}

.user {
    padding-bottom: 2.5rem;
    width: 100%;
    display: flex;
    /* justify-content: center; */
    align-items: center;
    flex-direction: column;
   
}

.user p{
    max-width: 320;
    word-break: break-word;
}

header {
    width: 100%;
    margin: 0 auto;
    padding: 2em;
    background-image: url("https://blenderartists.org/uploads/default/original/4X/6/9/2/692b2e29c5a043f7e2d510acd750003ad0fe13d2.jpeg");
    background-color: #fff;
    background-blend-mode: multiply;
    background-size: cover;
    color: #fff;
    padding: 1em;
    align-items: center;
    height: 50vh;
}

.buttons {
    padding: 2em;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    gap: 4em;
    margin: 0 auto;
}

/* Стили для кнопок */
.btn {
    width: 60px;
    /* Устанавливаем ширину и высоту одинаковыми для создания круга */
    height: 60px;
    border-radius: 50%;
    /* Радиус круга */
    display: flex;
    align-items: center;
    justify-content: center;
    background-color:  #fff;
    /* Цвет фона */
    color:  #111;
    /* Цвет иконки */
    border: none;
    font-size: 24px;
    /* Размер иконки */
    cursor: pointer;
    transition: background-color 0.3s ease;
}


.btn:hover {
    background-color: #FFC600;
    ;
    /* Цвет фона при наведении */
}
.header-img {
    display: flex;
    justify-content: center;
    margin-top: -15em;
}

.header-img img {
    object-fit: cover;
    width: 300px;
    height: 300px;
    max-width: 100%;
    border-radius: 50%;
    padding: 20px; /* Заменяем border на padding */
    background: 
        linear-gradient(to bottom, #00000031, #ffffff28) /* Градиент фона */
        padding-box, /* Применяем градиент только к padding области */
        linear-gradient(to bottom, #000000, #ffffff60) /* Тот же градиент для border */
        border-box;
    background-origin: border-box;
    background-clip: padding-box, border-box;
    border: 20px solid transparent; /* Прозрачная граница для отображения градиента */
}
.img {
    
    border-width: 20px;
    border-color: rgba(255, 255, 255, 0.250);

}

header .header-text {
    color: #fff;
    text-align: center;
    display: block;
    margin: 0;
    height: fit-content;
}



header .header-text h1 {
    font-family: "Dm Serif Display", serif;
    font-size: 6em;
    margin-bottom: -0.8em;
}

header .header-text h2 {
    font-family: "Dancing Script", cursive;
    font-size: 4em;
    color:  #FFC600;
    margin-top: 0px;
}

.container {
    /* font-family: "Afacad Flux", sans-serif; */
    font-family: "Kameron", serif;
    display: flex;
    justify-content: space-between;
    /* align-items: center; */
    text-align: center;
    margin: 0 auto;
    color: #fff;
    position: relative;
    min-height: 100vh;
    background-color:#111;
    max-width: 100%;
    padding: 20px;
  box-sizing: border-box;
  flex-direction: column;

}

.container .user h2 {
    font-size: 2.5em;
    margin: 0;
    padding: 0;
    font-weight: 500;
}

.container .user .position {
    font-size: 1.7em;
    margin: 0;
    padding: 0;
    font-weight: 500;
    color: #FFC600;
}


.custom-list {
    list-style: none;
    font-size: large;
}

.custom-list li {
    display: flex;
    align-items: center;
    margin: 1.2em 0;
}

.custom-list li .special {
    margin-right: 30px;
    font-size: 1.7em;
    color: #fff;
}

footer {
    background-color: #111;
    color: white;
    text-align: center;
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 2.5rem;
    display: block;
    justify-content: center;
    align-items: center;
}

.popup {
    color: #111;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
}

/* Popup content */
.popup-content {
    background-color:  #FFC600;
    padding: 20px;
    border-radius: 10px;
    text-align: center;
    position: relative;
    color: #111;
}

.partneri{
    color: #111;
    background-color: #fff;
    padding: 20px;
}

.share-popup {
    color: black;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
}

/* Popup content */
.share-popup-content {
    background-color:  #FFC600;
    padding: 30px;
    border-radius: 10px;
    text-align: center;
    position: relative;
    width: 30%;
    color: #111;
}

.share-popup-content textarea {
    width: 100%;
    height: 1.8em;
    text-align: center;
    resize: none;
    border: 1px solid #fff;
    background-color: #fff;
    color: #111;
}

/* Close button */
.close {
    position: absolute;
    top: 10px;
    right: 20px;
    font-size: 30px;
    cursor: pointer;
}


.copy {
    background-color: var(--orange);
    color: white;
    border: none;
    padding: 0.5em 1em;
    border-radius: 5px;
    cursor: pointer;
}


.user .textF {
        display: block;
        justify-content: center;
        margin-top: 1.2em;
        background-color: #fff;
        color: #111;
        align-items: center;
    }

.textF p{
    text-align: center;
        max-width: 320;
        word-break: break-word;
        align-items: center;
}

.text{
    background-color: #fff;
    color: #111;
    text-align: center;
    max-width: 320;
    word-break: break-word;
    align-items: center;
    margin-top: 2em;
}

.contact {
    margin-top: 1em; /* Отступ сверху */
    padding: 1rem;
  
    color: white;
    text-align: center;
    flex-basis: auto;
}

.emphasis {
    color:#FFC600;
    font-size: 1.2em;
    text-decoration: none;
}

.emphasis:hover {
    text-decoration: underline;
}


</style>