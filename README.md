# Cookies Wochenplaner

Kleine Wochenplaner-App (Deutsch, fürs iPhone gemacht) als installierbare Web-App (PWA): Gerichte der Woche bestätigen oder ablehnen (mit sofortigem Ersatzvorschlag), Rezepte mit Zutaten und Schritten, Einkaufsliste aus den bestätigten Gerichten.

**Enthält keine persönlichen Daten.** In diesem Repo liegen nur App-Code, Icons und allgemeine Rezeptbilder. Wochenpläne, Rezepte, Nährwerte und die Auswahl liegen in einem separaten **privaten** Repository und werden erst geladen, wenn in der App ein eigener GitHub-Schlüssel (fine-grained personal access token, nur dieses private Repo, „Contents: Read and write“) eingetragen ist. Der Schlüssel wird nur im Browser des Geräts (localStorage) gespeichert. Ohne Schlüssel zeigt die App nur die Einrichtung.

App: https://tinofavetto.github.io/cookie-wochenplaner/ – am iPhone in Safari öffnen → Teilen → „Zum Home-Bildschirm“.

## Dateien
- `index.html` – komplette App (HTML/CSS/JS, keine Abhängigkeiten)
- `sw.js` – Service Worker (App-Dateien offline; GitHub-API wird nie zwischengespeichert)
- `manifest.webmanifest`, `icon-*.png`, `apple-touch-icon.png` – App-Icon (selbst erstellt)
- `img/<rezept-id>.webp` – Rezeptbilder

## Bildquellen
Alle Bilder stammen von Wikimedia Commons, wurden auf 480 × 360 px zugeschnitten/verkleinert und als WebP gespeichert. Es sind Beispielfotos – sie zeigen nicht immer exakt das Rezept (z. B. vegetarische Varianten). Bearbeitete Dateien von CC-BY-SA-Vorlagen stehen unter derselben Lizenz wie das Original.

| Datei | Original | Urheber | Lizenz |
|---|---|---|---|
| `img/blumenkohl-curry.webp` | [Curried cauliflower and chickpea stew.jpg](https://commons.wikimedia.org/wiki/File:Curried_cauliflower_and_chickpea_stew.jpg) | Jim Reynolds from Cleveland, USA | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0) |
| `img/butternut-gefuellt.webp` | [Butternut squash stuffed shells with toasted pecan and sage brown butter (3869054302).jpg](https://commons.wikimedia.org/wiki/File:Butternut_squash_stuffed_shells_with_toasted_pecan_and_sage_brown_butter_(3869054302).jpg) | Karen and Brad Emerson | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0) |
| `img/chili-sin-carne.webp` | [ChiliSinCarne.jpg](https://commons.wikimedia.org/wiki/File:ChiliSinCarne.jpg) | Charles Brooking | Public domain |
| `img/chinakohl-erdnuss-tofu.webp` | [Horka Litinova Panev Tofu Zlaty Klas 2025.jpg](https://commons.wikimedia.org/wiki/File:Horka_Litinova_Panev_Tofu_Zlaty_Klas_2025.jpg) | Mojmir Churavy | [CC0](http://creativecommons.org/publicdomain/zero/1.0/deed.en) |
| `img/fenchel-ofenblech.webp` | [Roasted Fennel, Burrata, and orange (9024095627).jpg](https://commons.wikimedia.org/wiki/File:Roasted_Fennel,_Burrata,_and_orange_(9024095627).jpg) | Charles Haynes | [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0) |
| `img/frittata.webp` | [Frittata di patate.jpg](https://commons.wikimedia.org/wiki/File:Frittata_di_patate.jpg) | Ensahequ | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) |
| `img/gefuellte-paprika.webp` | [Vegan Stuffed Roasted Red Peppers (5908287385).jpg](https://commons.wikimedia.org/wiki/File:Vegan_Stuffed_Roasted_Red_Peppers_(5908287385).jpg) | Lablascovegmenu from London | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0) |
| `img/gruenkohl-wuerstchen.webp` | [Boerenkool met worst.jpg](https://commons.wikimedia.org/wiki/File:Boerenkool_met_worst.jpg) | Amin | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) |
| `img/huel.webp` | [Huel powder black edition shaker.jpg](https://commons.wikimedia.org/wiki/File:Huel_powder_black_edition_shaker.jpg) | Ethanmackenzie1 | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) |
| `img/kartoffel-pilz-gratin.webp` | [Gratin 4.jpg](https://commons.wikimedia.org/wiki/File:Gratin_4.jpg) | Wxao Zexw | [CC0](http://creativecommons.org/publicdomain/zero/1.0/deed.en) |
| `img/kichererbsen-bratlinge.webp` | [Curry chickpea burgers (4900258232).jpg](https://commons.wikimedia.org/wiki/File:Curry_chickpea_burgers_(4900258232).jpg) | Abi Porter | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0) |
| `img/kuerbis-gnocchi-blech.webp` | [Gnocchi di zucca.jpg](https://commons.wikimedia.org/wiki/File:Gnocchi_di_zucca.jpg) | Ricettario di Mamidoli | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) |
| `img/kuerbis-kichererbsen-eintopf.webp` | [Chickpea stew.jpg](https://commons.wikimedia.org/wiki/File:Chickpea_stew.jpg) | E4024 | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) |
| `img/kuerbis-linsen-curry.webp` | [Curried Lentils with Potatoes on Rice (3899524434).jpg](https://commons.wikimedia.org/wiki/File:Curried_Lentils_with_Potatoes_on_Rice_(3899524434).jpg) | Mack Male from Edmonton, AB, Canada | [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0) |
| `img/kuerbis-risotto.webp` | [Risotto with pumpkin, pecorino and pine nuts (30897108636).jpg](https://commons.wikimedia.org/wiki/File:Risotto_with_pumpkin,_pecorino_and_pine_nuts_(30897108636).jpg) | Luca Nebuloni | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0) |
| `img/kuerbis-suppe.webp` | [Autumn Soup (Unsplash) cropped.jpg](https://commons.wikimedia.org/wiki/File:Autumn_Soup_(Unsplash)_cropped.jpg) | Cala cala_maffia | [CC0](http://creativecommons.org/publicdomain/zero/1.0/deed.en) |
| `img/linsen-bolognese.webp` | [Spaghetti Bolognese - Figaros, Brighton 2023-10-06.jpg](https://commons.wikimedia.org/wiki/File:Spaghetti_Bolognese_-_Figaros,_Brighton_2023-10-06.jpg) | Andy Li | [CC0](http://creativecommons.org/publicdomain/zero/1.0/deed.en) |
| `img/linsen-eintopf.webp` | [Catalan lentil soup.JPG](https://commons.wikimedia.org/wiki/File:Catalan_lentil_soup.JPG) | Xufanc | [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0) |
| `img/mandel-kuerbis-pasta.webp` | [Pasta with pumpkin, aubergine and chili pepper (30506843925).jpg](https://commons.wikimedia.org/wiki/File:Pasta_with_pumpkin,_aubergine_and_chili_pepper_(30506843925).jpg) | Luca Nebuloni | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0) |
| `img/ofengemuese-bowl.webp` | [BuddhaBowlLot.jpg](https://commons.wikimedia.org/wiki/File:BuddhaBowlLot.jpg) | PizzaMan | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) |
| `img/ofenkartoffeln-brokkoli.webp` | [Roasted potatoes in bowl.jpg](https://commons.wikimedia.org/wiki/File:Roasted_potatoes_in_bowl.jpg) | Punker1999 | [CC0](http://creativecommons.org/publicdomain/zero/1.0/deed.en) |
| `img/pasta-pfeffermedaillons.webp` | [Mushroom and tomato sauce pasta (4261192837).jpg](https://commons.wikimedia.org/wiki/File:Mushroom_and_tomato_sauce_pasta_(4261192837).jpg) | pelican from Tokyo, Japan | [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0) |
| `img/pesto-bohnen-pasta.webp` | [Basil pesto pasta.jpg](https://commons.wikimedia.org/wiki/File:Basil_pesto_pasta.jpg) | Shreya13jain | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) |
| `img/pilz-gulasch.webp` | [Pilzragout-mit-Reis.jpg](https://commons.wikimedia.org/wiki/File:Pilzragout-mit-Reis.jpg) | MartinThoma | [CC0](http://creativecommons.org/publicdomain/zero/1.0/deed.en) |
| `img/pilz-stroganoff.webp` | [Baked Mushroom Stroganoff Spud with Squash (3612329429).jpg](https://commons.wikimedia.org/wiki/File:Baked_Mushroom_Stroganoff_Spud_with_Squash_(3612329429).jpg) | Vegan Feast Catering | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0) |
| `img/quesadillas.webp` | [Quesadilla with cheese, black beans, and beef brisket - Cambridge, MA.jpg](https://commons.wikimedia.org/wiki/File:Quesadilla_with_cheese,_black_beans,_and_beef_brisket_-_Cambridge,_MA.jpg) | Daderot | [CC0](http://creativecommons.org/publicdomain/zero/1.0/deed.en) |
| `img/rosenkohl-gnocchi.webp` | [Gnocchi mit Maronen, Schlüchtern.jpg](https://commons.wikimedia.org/wiki/File:Gnocchi_mit_Maronen,_Schl%C3%BCchtern.jpg) | Gerda Arendt | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) |
| `img/rosenkohl-ofen.webp` | [Roasted Brussels Sprouts with Kumquats.jpg](https://commons.wikimedia.org/wiki/File:Roasted_Brussels_Sprouts_with_Kumquats.jpg) | Kelly Sue | [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0) |
| `img/rosenkohl-pasta.webp` | [Hot pasta with brussels sprouts (22334866755).jpg](https://commons.wikimedia.org/wiki/File:Hot_pasta_with_brussels_sprouts_(22334866755).jpg) | sunny mama | [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0) |
| `img/rote-bete-linsen.webp` | [Beetroot Salad (3862315693).jpg](https://commons.wikimedia.org/wiki/File:Beetroot_Salad_(3862315693).jpg) | Suzette - www.suzette.nu from Arnhem, Netherlands | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0) |
| `img/rote-bete-ofen.webp` | [Roasted beetroot.jpg](https://commons.wikimedia.org/wiki/File:Roasted_beetroot.jpg) | Jacknstock | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) |
| `img/rotkohl-tempeh.webp` | [Modra kapusta po poznansku.jpg](https://commons.wikimedia.org/wiki/File:Modra_kapusta_po_poznansku.jpg) | MOs810 | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) |
| `img/ruehrei.webp` | [Liat Portal for Foodie Disorder - Breakfast in Israel scrambled eggs with herbs and vegetables.jpg](https://commons.wikimedia.org/wiki/File:Liat_Portal_for_Foodie_Disorder_-_Breakfast_in_Israel_scrambled_eggs_with_herbs_and_vegetables.jpg) | HaJunkiyada | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) |
| `img/spitzkohl-pfanne.webp` | [Bratkartoffeln 1024 768.jpg](https://commons.wikimedia.org/wiki/File:Bratkartoffeln_1024_768.jpg) | Eckhard Polesny ( ? Metzecki at de.wikipedia) | Public domain |
| `img/spitzkohl-schupfnudeln.webp` | [Schupfnudeln mit Sauerkraut.jpg](https://commons.wikimedia.org/wiki/File:Schupfnudeln_mit_Sauerkraut.jpg) | MarkusHagenlocher | [CC BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/) |
| `img/tempeh-gruenkohl.webp` | [Boerenkool stamppot with turkey ham instead of bacon 2.jpg](https://commons.wikimedia.org/wiki/File:Boerenkool_stamppot_with_turkey_ham_instead_of_bacon_2.jpg) | GrammarFascist | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) |
| `img/teriyaki-tofu.webp` | [Baked Tofu with Broccoli and Rice.jpg](https://commons.wikimedia.org/wiki/File:Baked_Tofu_with_Broccoli_and_Rice.jpg) | Miscellaneous contributor | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) |
| `img/udon-tofu.webp` | [Black pepper tofu fried udon - Stir Fry by CK.jpg](https://commons.wikimedia.org/wiki/File:Black_pepper_tofu_fried_udon_-_Stir_Fry_by_CK.jpg) | Andy Li | [CC0](http://creativecommons.org/publicdomain/zero/1.0/deed.en) |
| `img/weisse-bohnen-eintopf.webp` | [Tuscan kale and white bean soup in personalized bowls with spoons on a decorative tree cross cut (16085794138).jpg](https://commons.wikimedia.org/wiki/File:Tuscan_kale_and_white_bean_soup_in_personalized_bowls_with_spoons_on_a_decorative_tree_cross_cut_(16085794138).jpg) | Personal Creations | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0) |
| `img/zucchini-gefuellt.webp` | [Stuffed squash 2025 JORDAN (2).jpg](https://commons.wikimedia.org/wiki/File:Stuffed_squash_2025_JORDAN_(2).jpg) | Justwiki | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0) |
