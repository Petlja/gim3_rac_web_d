Теме и додаци
=============

.. |btn_activate_design|   image:: ../../_images/wordpress/btn_activate_design.png
.. |btn_back|              image:: ../../_images/wordpress/btn_back.png
.. |btn_my_site|           image:: ../../_images/wordpress/btn_my_site.png
.. |btn_customizre_theme|  image:: ../../_images/wordpress/btn_customizre_theme.png
.. |btn_wp_admin|          image:: ../../_images/wordpress/btn_wp_admin.png
.. |btn_add_a_widget|      image:: ../../_images/wordpress/btn_add_a_widget.png
.. |icon_search|           image:: ../../_images/wordpress/icon_search.png


У веб-дизајну се начин приказивања сваког детаља веб-странице задаје помоћу **стилова**. Стиловима се дефинишу боје текста и позадине за сваки елемент стране, коришћени фонтови, изглед оквира, растојања између појединих елемената стране и друго.

Поред тога, битно је дефинисати структуру стране, то јест елементе од којих се страна састоји и њихов распоред. Предефинисана структура стране се назива **темплејт**. Разуме се, комбиновање темплејта и стилова поред времена захтева и известан осећај за естетику.

Теме
----

Да би нам олакшао дефинисање изгледа стране *WordPress* користи концепт тема. Тема је колекција темплејта и стилова помоћу којих се задаје сваки детаљ начина приказивања странице. Професионални веб-дизајнери пажљиво осмишљавају теме тако да се добије складан и допадљив општи изглед. Утисак који сајт оставља је у великој мери одређен управо коришћеном темом.

У систему *WordPress.com* на располагању су нам на стотине тема, од тога велики број у оквиру бесплатног плана. У менију |btn_my_site| потребно је одабрати *Appearance → Themes*.

.. figure:: ../../_images/wordpress/teme_izbor.png
    :align: center
    :width: 780px
    :class: screenshot-shadow

Када кликнете на неку тему, можете је разгледати без обавезе да је активирате. Уколико вам се тема не допада, можете да се вратите на бирање кликом на дугме |btn_back|, а можете и да напустите бирање тема кликом на дугме |btn_my_site|. Када нађете тему која вам одговара, можете да је активирате кликом на дугме |btn_activate_design| (уколико је тема бесплатна). 

.. figure:: ../../_images/wordpress/teme_da_ne.png
    :align: center
    :width: 780px
    :class: screenshot-shadow

Слике на новој теми можете да промените кликом на слику, а затим на дугме *Replace* у сликовном менију, као што је и раније објашњено.

Прилагођавање теме
''''''''''''''''''

.. figure:: ../../_images/wordpress/prilagodjavanje_teme.png
    :align: right
    :width: 300
    :class: screenshot-shadow

Тема може да се промени у било ком тренутку током развоја сајта. Прелазак на нову тему не захтева никакве додатне активности уколико није било напредних прилагођавања теме. У случају да користите сопствени веб-сервер, ради потпуне сигурности се препоручује да направите комплетну резервну копију сајта (*backup*) пре оваквих измена.

Теме се најчешће могу додатно прилагодити. Прилагођавање започињемо кликовима на |btn_my_site|, *Appearance → Customize*. Могућности понуђене у прилагођавању се виде на слици десно и углавном су јасне саме по себи, а често садрже додатна објашњења, упутства и савете.

У оквиру прилагођавања теме можете да промените:

- наслов и поднаслов сајта (*Site identity*),
- преместите постојеће меније, промените им ставке, додате нови мени (*Menus*),
- изаберете која од постојећих страница ће бити почетна и шта ће на њој бити приказано (*Homepage Settings*),
- одаберете комбинацију боја (*Colors*),
- изаберете стил текста (*Fonts*) и
- задате додатно стилизовање ваших страна (*Additional CSS*).

Прикључци
---------

Прикључак (енгл. *plugin*, често се преводи и као додатак) је софтверска компонента која се може додати веб-сајту креираном у систему *WordPress*. Прикључци могу да прошире постојеће или да дају нове функционалности веб-сајтовима.

На пример, постоје прикључци који омогућавају управљање контактима, креирање онлајн продавнице, прикључци који помажу да се веб-стране уреде тако да постигну боље рангирање на претраживачима (*Search Engine Optimization*, скр. *SEO*), прикључци који смањују време учитавања сајта и многи други.

Организовањем додатних функционалности у мале компоненте, *WordPress* је корисницима веома поједноставио процес додавања тих функционалности својим сајтовима. Захваљујући модуларности, корисник може да дода жељену функционалност свом сајту "као са полице", а да не мора ни мало да разуме програмски кôд. Корисницима сервера *WordPress.com* са комерцијалним планом на располагању је више десетина хиљада прикључака за *WordPress* (који се не наплаћују додатно).

Избор доступних прикључака се отвара кликом на *Plugins* у менију |btn_my_site|.

Виџити
------

Виџит (енгл. *widget*, справица) је софтверски додатак веб-страни, који се на њој најчешће види као икона или дугме. Ако сте икада кликнули на дугме за дељење (*share button*) на врху стране да бисте разгласили неку вест на друштвеним мрежама, користили сте виџит.

Прикључци и виџити су слични по томе што и једни и други доносе нове функционалности веб-страници. Прикључке треба посматрати као програме који се инсталирају и нешто раде са нашим сајтом (или нама омогућавају да урадимо нешто), а виџите као садржај, тј. као делове сајта који се убацују директно у неку од веб-страна. Прикључак најчешће није видљив на страници и нема интерфејс за интеракцију са корисником (ради у позадини), док је виџит видљив и обично на неки начин комуницира са корисником.

Систем *WordPress* омогућава једноставно стављање виџита само у посебне области на страни, као што су заглавље, подножје или бочна трака (*header, footer, sidebar*). Зато у овом контексту наведене области једним именом зовемо области виџита (*widget areas*). Многе теме имају само једну од поменутих области (нпр. подножје), али у оквиру комерцијалног корисничког плана може да се на страницу постави неки од прикључака, помоћу којих се у тему или на поједине стране могу додавати нпр. бочне траке (*custom sidebars*), а касније у њих и виџити.

Виџитима управљамо у секцији *Appearance → Widgets* менија |btn_my_site|. Овде можемо да изаберемо област виџита коју уређујемо. Када постоји само једна област, она је аутоматски изабрана (на слици доле, то је област *Footer*, тј. подножје). Кликом на дугме |btn_add_a_widget| отвара се листа доступних виџита које можемо да додамо у задату област. Да бисмо додали виџит, довољно је кликнути на њега и он је већ видљив у прегледу (*preview*) са десне стране.

.. figure:: ../../_images/wordpress/widgets.png
    :align: center
    :width: 300
    :class: screenshot-shadow

Виџитима које смо раније додали, можемо да мењамо редослед у листи (а тиме и на страни) кликом на опцију *Reorder*. На пример, на претходној слици се види да смо додали два виџита:

- Виџит *Milestone*, који у страницу додаје тајмер за одбројавање преосталог времена до задатог тренутка - догађаја
- Виџит *Search*, помоћу кога посетиоци нашег сајта могу да пронађу неку вест или други садржај

Кликом на виџит отвара се подешавање специфично за тај виџит. У подешавању виџита *Milestone* можемо да задамо наслов, датум и време догађаја и друге детаље, док за виџит *Search* можемо да подесимо назив поља за претрагу. Када смо задовољни подешавањима, треба да кликнемо *Done* да бисмо их сачували. Кликом на *Remove* уклонићемо виџит из задате области.

Тема може да садржи већ додате и укључене виџите, које добијамо самим избором теме. Неки од популарних виџита који су често унапред додати у теме су већ помињана претрага (*Search*), недавне објаве на блогу (*Recent posts*), архива објава и страна (*Archives*), листа категорија (*Categories*) са везама ка објавама у оквиру сваке категорије и сл.

Након уређивања виџита треба још кликнути *Save Changes* у врху, да би стање које видимо у прегледу десно (избор, редослед и подешавања виџита у области) било објављено.
