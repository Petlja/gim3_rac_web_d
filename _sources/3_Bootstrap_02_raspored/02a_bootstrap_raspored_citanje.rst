*Bootstrap* и распоређивање елемената
=====================================

*Bootstrap* за распоређивање елемената користи систем мреже (engl. *grid system*).

Хијерархија елемената у оваквом систему захтева да имамо контејнер елемент, у њему елементе који представљају редове, и у сваком реду елементе колона.

*Bootstrap* може да распореди елементе по контејнерима, који заузимају најмање дванаестину ширине стране (*col-1*) а највише целу ширину (*col-12*):

.. figure:: ../../_images/bootstrap/kontejneri.png
    :width: 780px
    :align: center
    
Контејнери ``col-1`` су најужи и може се ставити 12 блокова ове ширине у један ред. Блокови различитих ширина се могу комбиновати у једном реду (на пример ``col-4`` и ``col-8`` у трећем реду), под условом да не пређу укупну ширину 12.

.. petlja-editor:: bootstrap_grid_demo

    style.css
    .container-fluid {
        padding: 20px;
    }
    .col-1, .col-4, .col-6, .col-8, .col-12 {
        background-color: #efefef;
        text-align: center;
        border: 1px solid white;
    }
    ~~~
    index.html
    <!doctype html>
    <html>
    <head>
        <title>Bootstrap</title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css" rel="stylesheet" crossorigin="anonymous">
        <link rel="stylesheet" href="style.css"/>
    </head>
    <body>
        <div class="container-fluid">
            <div class="row">
                <div class="col-1">col-1</div>
                <div class="col-1">col-1</div>
                <div class="col-1">col-1</div>
                <div class="col-1">col-1</div>
                <div class="col-1">col-1</div>
                <div class="col-1">col-1</div>
                <div class="col-1">col-1</div>
                <div class="col-1">col-1</div>
                <div class="col-1">col-1</div>
                <div class="col-1">col-1</div>
                <div class="col-1">col-1</div>
                <div class="col-1">col-1</div>
            </div>
            <div class="row">
                <div class="col-4">col-4</div>
                <div class="col-8">col-8</div>
            </div>
            <div class="row">
                <div class="col-4">col-4</div>
                <div class="col-4">col-4</div>
                <div class="col-4">col-4</div>
            </div>
            <div class="row">
                <div class="col-6">col-6</div>
                <div class="col-6">col-6</div>
            </div>
            <div class="row">
                <div class="col-12">col-12</div>
            </div>
        </div>
    </body>
    </html>


У следећем примеру је приказан кôд реда који у себи има 3 ``<div>`` блока исте ширине:

.. petlja-editor:: bootstrap_grid_1

    style.css
    .crvena {
        background-color: red;
    }
    .plava {
        background-color: blue;
        color: white;
    }
    .zelena {
        background-color: green;
    }
    ~~~
    index.html
    <!doctype html>
    <html>
    <head>
        <title>Bootstrap</title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css" rel="stylesheet" crossorigin="anonymous">
        <link rel="stylesheet" href="style.css"/>
    </head>
    <body>
        <div class="container">
            <div class="row">
                <div class="col crvena">
                    Ред 1 Колона 1
                </div>
                <div class="col plava">
                    Ред 1 Колона 2
                </div>
                <div class="col zelena">
                    Ред 1 Колона 3
                </div>
            </div>
        </div>
    </body>
    </html>

У овом примеру, ``<div>`` блокови ће заузети по трећину ширине стране (као ``col-4`` са горње слике), пошто ширине нису експлицитно наведене у *CSS* класама.

.. questionnote::

    **Вежба**

    Измените претходни пример тако да колоне буду распоређене:

    - прва колона ширине 2 блока,
    - друга колона ширине 6 блокова,
    - трећа колона ширине 4 блока.

    Након тога, пробајте да другој колони додате ширину 7 блокова. Тада збир прелази 12 (2 + 7 + 4 = 13). Који је резултат?

*Bootstrap* има и посебне класе са префиксима ``col-sm-``, ``col-lg-`` и слично. Више информација о овим класама се може наћи на сајту `Bootstrap <https://getbootstrap.com/docs/5.2/layout/grid/#responsive-classes/>`_.

Распоред – Пример 1
-------------------

Потребно је направити *Bootstrap* распоред за следећи дизајн  (занемарићемо садржај):

.. figure:: ../../_images/bootstrap/raspored2.png
    :width: 500px
    :align: center
    :class: screenshot-shadow

Елемент ``div`` са класом ``hello-world`` заузима целу ширину и има позадинску боју, као на слици. Користећи класу ``.container-sm`` постижемо да се ширина садржаја ограничи и садржај центрира.

.. petlja-editor:: bootstrap_grid_2

    style.css
    .row {
        border: 1px dashed #ccc;
    }

    .col, .col-4, .col-6, .col-8 {
        border: 1px dotted red;
    }

    .hello-world {
        background-color: skyblue;
    }
    ~~~
    index.html
    <!doctype html>
    <html>
    <head>
        <title>Bootstrap</title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css" rel="stylesheet" crossorigin="anonymous">
        <link rel="stylesheet" href="style.css"/>
    </head>
    <body>
        <div class="row">
            <div class="col">Navbar…</div>
        </div>
        <div class="hello-world">
            <div class="container-sm">
                <div class="row">
                    <div class="col">
                        <h1>Hello World</h1>
                        <p>...</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="container-sm">
            <!-- Ред са 3 колоне -->
            <div class="row">
                <div class="col-4">
                    <h2>Heading</h2>
                    <p>...</p>
                </div>
                <div class="col-4">
                    <h2>Heading</h2>
                    <p>...</p>
                </div>
                <div class="col-4">
                    <h2>Heading</h2>
                    <p>...</p>
                </div>
            </div>
            <div class="row">
                <div class="col">&copy; Company 2017</div>
            </div>
        </div>
    </body>
    </html>

Распоред – Пример 2
-------------------

Потребно је направити распоред ``<div>`` блокова који одговара следећој страни (занемарићемо садржај):

.. figure:: ../../_images/bootstrap/raspored1.png
    :width: 780px
    :align: center
    :class: screenshot-shadow
    
Прва три реда (лого, навигација и велики наслов) заузимају пуну ширину стране и зато имају по један ``<div>`` у реду.

Потом следи ред са две колоне једнаких ширина које садрже два главна чланка. За две колоне једнаких ширине користимо ``col-6`` да би добили збир од 12 колона.

На крају се налази ред у коме је лева колона (чланак) два пута шира од десне (секција *About*). Одговарајуће колоне би биле ``col-8`` и ``col-4``.

*Bootstrap* распоред који одговара овој страни је:

.. petlja-editor:: bootstrap_grid_3

    style.css
    .row {
        border: 1px dashed #ccc;
    }

    .col, .col-4, .col-6, .col-8 {
        border: 1px dotted red;
    }
    ~~~
    index.html
    <!doctype html>
    <html>
    <head>
        <title>Bootstrap</title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css" rel="stylesheet" crossorigin="anonymous">
        <link rel="stylesheet" href="style.css"/>
    </head>
    <body>
        <!-- Лого -->
        <div class="row">
          <div class="col text-center">
            <h1>Large</h1>
          </div>
        </div>
        <!-- Навигациона трака -->
        <div class="row">
          <div class="col">
            World | U.S. | Technology | ...
          </div>
        </div>
        <!-- Издвојен чланак -->
        <div class="row">
          <div class="col p-5">
            <h1>
                Title of a longer<br/>
                featured blog post
            </h1>
          </div>
        </div>
        <!-- Два издвојена чланка -->
        <div class="row">
          <div class="col-6">
            <h2>Featured post</h2>
            <p>...</p>
          </div>
          <div class="col-6">
            <h2>Post title</h2>
            <p>...</p>
          </div>
        </div>
        <div class="row">
          <!-- Главни садржај стране -->
          <div class="col-8">
            <h1>Sample blog post</h1>
            <p>...</p>
          </div>
          <!-- Споредна секција -->
          <div class="col-4">
            <h2>About</h2>
            <p>...</p>
          </div>
        </div>
    </body>
    </html>
