Функције
========

У програмима који решавају сложеније проблеме, групу наредби које решавају неки подзадатак можемо да издвојимо у целину која се зове функција. Функција има своје име и позивом функције по имену се извршавају наредбе у тој функцији.


У језику *JavaScript* се функције креирају тако што се иза имена функције у облим задградама наведе листа параметара, а затим у витичастим заградама скуп наредби које треба извршити када се та функција позове. 

.. figure:: ../../_images/js/funkcija_sintaksa.png
    :width: 500px
    :align: center

Параметри су вредности које можемо да пошаљемо функцији када је позовемо. Функција на основу параметара може (а не мора) да врати неки резултат помоћу наредбе *return*. У следећих пар примера ћемо видети како се пишу и позивају функције које враћају резултат:

.. questionnote::

    **Пример - сложено кретање 1**
    
    Позната је брзина тела у појединим тренуцима:

    - у тренутку :math:`t_0 = 0 s`, брзина је била :math:`V_0 = 2 {m \over s}`
    - у тренутку :math:`t_1 = 4 s`, брзина је била :math:`V_1 = 11 {m \over s}`
    - у тренутку :math:`t_2 = 11 s`, брзина је била :math:`V_2 = 13 {m \over s}`
    - у тренутку :math:`t_3 = 14 s`, брзина је била :math:`V_3 = 5 {m \over s}`

    Написати програм који израчунава дужину пута коју је ово тело прешло, претпостављајући да се брзина између контролних тачака мењала равномерно.

Уз нешто знања физике не би требало да буде тешко да се разуме дато решење:

.. activecode:: slozeno_kretanje_1_js
    :language: javascript
    :nocodelens:

    function put(tPoc, tZav, vPoc, vZav) {
        let t = tZav - tPoc;
        let vsr = (vPoc + vZav) / 2;
        let predjeniPut = vsr * t;
        return predjeniPut;
    }

    // дати подаци
    let t0 = 0, t1 = 4, t2 = 11, t3 = 14;
    let v0 = 2, v1 = 11, v2 = 13, v3 = 5;

    let s1 = put(t0, t1, v0, v1);
    let s2 = put(t1, t2, v1, v2);
    let s3 = put(t2, t3, v2, v3);
    alert(`Укупан пређени пут је ${(s1+s2+s3).toFixed(2)}.`);

Када је потребно да функција врати више од једног резултата, те резултате можемо да наведемо у угластим заградама (као низ). Променљиве које примају враћене вредности на месту позива функције такође наводимо у угластим заградама.

.. questionnote::

    **Пример - сложено кретање 2**
    
    Тело које је на почетку у мировању, креће се све време у истом смеру на следећи начин:

    - најпре 3 секунде равномерно убрзава убрзањем од :math:`2 {m \over s^2}`;
    - затим се креће сталном брзином током наредних 10 секунди;
    - на крају равномерно успорава убрзањем од :math:`-6 {m \over s^2}` до заустављања.
    
    Написати програм који израчунава дужину пута коју је ово тело прешло.

.. activecode:: slozeno_kretanje_2_js
    :language: javascript
    :nocodelens:

    function putIZavrsnaBrzina(t, vpoc, a) {
        let vzav = vpoc + a*t;        // брзина после t секунди (завршна)
        let vsr = (vpoc + vzav) / 2;  // средња брзина
        put = vsr * t;                // пређени пут
        return [put, vzav];
    }

    // дати подаци
    let a01 = 2, a12 = 0, a23 = -6;
    let t01 = 3, t12 = 10;
    let v0 = 0;

    let [s1, v1] = putIZavrsnaBrzina(t01, v0, a01);
    let [s2, v2] = putIZavrsnaBrzina(t12, v1, a12);
    let t23 = v2 / Math.abs(a23);
    let [s3, v3] = putIZavrsnaBrzina(t23, v2, a23);
    alert(`Укупан пређени пут је ${(s1+s2+s3).toFixed(2)}.`);

|
    
Функције у претходним примерима на основу датих параметара израчунавају неки резултат и враћају га на место позива:

.. figure:: ../../_images/js/funkcija_ulaz_izlaz.png
    :width: 400px
    :align: center

Функција, међутим, може да буде и без параметара, а у том случају се после имена функције пишу само обле заграде. Такође, функција не мора ни да врати резултат. У следећем примеру се појављује функција која нема параметре и не враћа резултат (функције које не враћају резултат се понекад називају процедуре).

.. questionnote::

    **Пример - време отварања веб странице**
    
    Направити веб страницу, која по отварању јавља у колико сати је отворена.

Једно могуће решење је:

.. activecode:: tacno_vreme_js
    :language: html
    :nocodelens:
    
    <!DOCTYPE html>
    <html>
    <head>
      <script>

      function prikaziTacnoVreme() {
        let sada = new Date();
        alert(`Страница је отворена у ${sada.toLocaleTimeString()} сати.`);
      }

      prikaziTacnoVreme();

      </script>
      <title>Време</title>
    </head>
    <body>
        <p>Садржај стране.</p>
    </body>
    </html>


У случају да функција нема у себи наредбу ``return``, или ако би у њој писало само ``return;`` без вредности која се враћа, позив функције пишемо као наредбу

.. code-block:: javascript

    prikaziTacnoVreme();

Ако бисмо "вредност" такве функције грешком доделили некој променљивој

.. code-block:: javascript

    let x = prikaziTacnoVreme();

променљива ``x`` би добила вредност ``undefined``. 
