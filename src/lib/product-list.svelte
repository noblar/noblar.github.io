<script lang="ts">
    import P1 from "../assets/noblar/products/1.jpg";
    import P2 from "../assets/noblar/products/2.jpg";
    import P3 from "../assets/noblar/products/3.jpg";
    import P4 from "../assets/noblar/products/4.jpg";
    import P5 from "../assets/noblar/products/5.jpg";
    import P6 from "../assets/noblar/products/6.jpg";
    import P7 from "../assets/noblar/products/7.jpg";
    import P8 from "../assets/noblar/products/8.jpg";
    import P9 from "../assets/noblar/products/9.jpg";
    import ContactWhatsapp from "./contact-whatsapp.svelte";

    import Product from "./product.svelte";

    setTimeout(() => {
        const lb = new GLightbox({
            touchNavigation: true,
            loop: true,
            moreText: "Vezi toata descrierea",
            moreLength: 64,
            descPosition: "right"
        });

        lb.on('slide_after_load', (data) => {
            console.log(data);
            setTimeout(() => {
                data.slide.querySelector('.contact-wapp').onclick = () => {
                    const phone = '400769194863';
                    const text = `Sunt interesat de produsul: ${data.slideConfig.title}`;

                    const url = `https://wa.me/${phone}?text=${encodeURIComponent(text)}`;
                    window.open(url, '_blank', 'noopener');
                }
            }, 100);
        });
    }, 100);

    const wappLinkText = `
        <a
            class="contact-wapp text-sm text-lime-600"
            href="#"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Contacteaza-ma pe WhatsApp"
        >
            <i class="fa-brands fa-whatsapp"></i>
            Contactează-mă pe WhatsApp
        </a>
    `;
</script>

<div class="grid gap-6 grid-cols-1 md:grid-cols-3 mt-6 md:mt-8 mx-8 md:mx-32">
    <Product image={P4} title="Măsuță din piatră naturală de travertin" description={`
        <p>
            O piesă de mobilier sculpturală ce îmbină eleganța atemporală cu minimalismul contemporan.
        </p>
        <p>
            Fiecare detaliu este realizat manual, păstrând textura unică și nuanțele autentice ale travertinului.
        </p>
        <p>
            Designul geometric, perfect echilibrat, transformă această măsuță într-un element statement al oricărei incăperi de lux - o expresie pură a rafinamentului natural și a măiestriei artizanale.
        </p>

        ${wappLinkText}
    `} />

    <Product image={P5} title="Suport pentru plantă din lemn masiv" description={`
        <p>
            Eleganță sculpturală pentru interioare rafinate.
        </p>
        <p>
            Realizat din lemn masiv, acest suport pentru plantă impresionează prin silueta sa sculpturală și finisajele impecabile.
        </p>
        <p>
            Liniile fluide și proporțiile perfecte îl transformă într-o piesă de design contemporan, ideală pentru apartamente cu stil.
        </p>
        <p>
            Combinând funcționalitatea cu estetica minimalistă, suportul adaugă un accent cald și sofisticat oricărui colț de living, dining sau birou.
        </p>
        <p>
            Fiecare detaliu este atent lucrat, rezultând o piesă care emană rafinament și naturalețe.
        </p>
        <p>
            Disponibil la comandă, cu posibilitatea personalizării esenței de lemn și a finisajului.
        </p>

        ${wappLinkText}
    `} />

    <Product image={P6} title="Masă laterală din stejar masiv" description={`
        <p>
            Un design sculptural ce îmbină eleganța naturală a lemnului cu rafinamentul formelor contemporane.
        </p>
        <p>
            Liniile fluide ale bazei creează o prezență artistică, transformând această piesă într-un accent exclusivist pentru orice interior sofisticat.
        </p>
        <p>
            Finisajul cald, cu luciu satinat, pune în valoare textura nobilă a stejarului, oferind o notă de lux discret.
        </p>
        <p>
            Ideală pentru spații premium - de la apartamente elegante la lounge-uri rafinate - această masă aduce un echilibru perfect între artă, funcționalitate și măiestrie în execuție.
        </p>

        ${wappLinkText}
    `} />

    <Product image={P7} title="Măsuță" description={`
        <p>
            Design elegant și finisaj premium. Realizată din lemn masiv de stejar, cu îmbinări tăiate la 45° pentru un aspect rafinat și modern.
        </p>
        <p>
            Ideală ca noptieră sau măsuță de accent în spații sofisticate.
        </p>

        ${wappLinkText}
    `} />

    <Product image={P8} title="Suport carte din lemn masiv de stejar personalizabil" description={`
        <p>
            Elegant și practic, acest suport pentru carte este realizat din lemn masiv de stejar, cu un design modern și finisaj premium.
        </p>
        <p>
            Poate fi personalizat cu orice text (nume, citat, mesaj) și adaptat în dimensiuni la comandă.
        </p>
        <p>
            Perfect pentru dormitor, birou sau bibliotecă - o piesă decorativă ce adaugă stil și rafinament oricărui spațiu.
        </p>
        <p>
            📚 Material: stejar natural <br/>
            ✨ Personalizare: gravură text la alegere <br/>
            📏 Dimensiuni: standard sau personalizate <br/>
            🎁 Ideal ca decor sau cadou pentru iubitorii de lectură
        </p>

        ${wappLinkText}
    `} />

    <Product image={P9} title="Suport elegant pentru papuci" description={`
        <p>
            Realizat manual din lemn masiv de nuc, cu finisaj natural și linii curate.
        </p>
        <p>
            Designul minimalist se îmbină perfect cu rafinamentul unui interior modern sau clasic, adăugând o notă de căldură și lux în orice locuință.
        </p>
        <p>
            Ideal pentru holuri, dormitoare sau spații de relaxare, acest suport nu este doar practic, ci și o piesă decorativă deosebită, ce reflectă atenția la detalii și gustul pentru calitate autentică.
        </p>

        ${wappLinkText}
    `} />

    <!-- <Product image={P3} title="Birou din stejar masiv" description={`
        <p>
            Birou realizat din stejar masiv, cu un design minimalist și linii naturale, ideal pentru spații moderne sau amenajări cu accente boeme. Blatul din lemn solid, finisat manual, evidențiază textura autentică a stejarului și oferă un farmec cald și rafinat. Picioarele metalice subțiri conferă stabilitate și un aspect contemporan, punând în valoare eleganța materialului natural.
        </p>
        <p>
            Acest model poate fi realizat pe comandă, în dimensiunile, finisajele și esențele de lemn dorite, pentru a se integra perfect în orice interior. Perfect pentru birou, colțul de lucru de acasă sau spațiile creative.
        </p>

        ${wappLinkText}
    `} />

    <Product image={P2} title="Masă din stejar masiv" description={`
        <p>
            Transformăm lemnul de stejar masiv într-o piesă centrală pentru casa ta. Fiecare masă este lucrată cu grijă, respectând fibra, culoarea și caracterul unic al lemnului. Realizăm la comandă, pentru ca tu să ai exact masa pe care o visezi.
        </p>

        ${wappLinkText}
    `} />

    <Product image={P1} title="Personalizare gravată pe stejar masiv" description={`
        <p>
            Realizată prin gravură laser de înaltă precizie, această personalizare pe stejar masiv evidențiază eleganța naturală a lemnului și finețea detaliilor.
        </p>
        <p>
            Poate fi personalizată cu orice nume, logo sau text dorit, devenind un obiect unic și rafinat — perfect pentru cadouri, decoruri sau branding premium.
        </p>
        <p>
            ✅ Material: stejar masiv <br/>
            ✅ Gravură laser permanentă <br/>
            ✅ Design personalizat la cerere
        </p>

        ${wappLinkText}
    `} /> -->

</div>
