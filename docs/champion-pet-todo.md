# 英雄 Pet 进度 TODO

Source patch: `16.9.1`
Champion count: `172`

这份清单回答两个问题：哪些英雄已经做完，哪些还没做；以及每只 pet 是否已经分别体现 Q、W、E、R 四个技能。当前初始化状态是全员 `planned`。

整只 pet 的状态枚举：`planned`、`briefed`、`generated`、`needs-repair`、`accepted`、`regenerate-after-patch`。

Q/W/E/R 状态枚举：`planned`、`briefed`、`generated`、`needs-repair`、`accepted`。四个技能都达到 `accepted`，且整只 pet 通过 QA 后，英雄的 Done 才能勾选。

固定映射：Q = `waving`，W = `waiting`，E = `jumping`，R = `review`。

## 汇总

- accepted pets: 3
- not accepted pets: 169
- total champions: 172

## 英雄清单

| Done | Champion | Pet | Q | W | E | R | Package | Brief | QA |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [x] | Aatrox (Aatrox) | accepted | accepted | accepted | accepted | accepted | `lol-aatrox` | `briefs/Aatrox.md` | `runs/16.9.1/Aatrox/qa/contact-sheet.png` |
| [ ] | Ahri (Ahri) | planned | planned | planned | planned | planned | `lol-ahri` | `briefs/Ahri.md` | `runs/16.9.1/Ahri/qa/contact-sheet.png` |
| [ ] | Akali (Akali) | planned | planned | planned | planned | planned | `lol-akali` | `briefs/Akali.md` | `runs/16.9.1/Akali/qa/contact-sheet.png` |
| [ ] | Akshan (Akshan) | planned | planned | planned | planned | planned | `lol-akshan` | `briefs/Akshan.md` | `runs/16.9.1/Akshan/qa/contact-sheet.png` |
| [ ] | Alistar (Alistar) | planned | planned | planned | planned | planned | `lol-alistar` | `briefs/Alistar.md` | `runs/16.9.1/Alistar/qa/contact-sheet.png` |
| [ ] | Ambessa (Ambessa) | planned | planned | planned | planned | planned | `lol-ambessa` | `briefs/Ambessa.md` | `runs/16.9.1/Ambessa/qa/contact-sheet.png` |
| [ ] | Amumu (Amumu) | planned | planned | planned | planned | planned | `lol-amumu` | `briefs/Amumu.md` | `runs/16.9.1/Amumu/qa/contact-sheet.png` |
| [ ] | Anivia (Anivia) | planned | planned | planned | planned | planned | `lol-anivia` | `briefs/Anivia.md` | `runs/16.9.1/Anivia/qa/contact-sheet.png` |
| [ ] | Annie (Annie) | planned | planned | planned | planned | planned | `lol-annie` | `briefs/Annie.md` | `runs/16.9.1/Annie/qa/contact-sheet.png` |
| [x] | Aphelios (Aphelios) | accepted | accepted | accepted | accepted | accepted | `lol-aphelios` | `briefs/Aphelios.md` | `runs/16.9.1/Aphelios/qa/contact-sheet.png` |
| [ ] | Ashe (Ashe) | planned | planned | planned | planned | planned | `lol-ashe` | `briefs/Ashe.md` | `runs/16.9.1/Ashe/qa/contact-sheet.png` |
| [ ] | Aurelion Sol (AurelionSol) | planned | planned | planned | planned | planned | `lol-aurelionsol` | `briefs/AurelionSol.md` | `runs/16.9.1/AurelionSol/qa/contact-sheet.png` |
| [ ] | Aurora (Aurora) | planned | planned | planned | planned | planned | `lol-aurora` | `briefs/Aurora.md` | `runs/16.9.1/Aurora/qa/contact-sheet.png` |
| [ ] | Azir (Azir) | planned | planned | planned | planned | planned | `lol-azir` | `briefs/Azir.md` | `runs/16.9.1/Azir/qa/contact-sheet.png` |
| [x] | Bard (Bard) | accepted | accepted | accepted | accepted | accepted | `lol-bard-v4` | `briefs/Bard.md` | `runs/16.9.1/Bard-v4/qa/contact-sheet.png` |
| [ ] | Bel'Veth (Belveth) | planned | planned | planned | planned | planned | `lol-belveth` | `briefs/Belveth.md` | `runs/16.9.1/Belveth/qa/contact-sheet.png` |
| [ ] | Blitzcrank (Blitzcrank) | planned | planned | planned | planned | planned | `lol-blitzcrank` | `briefs/Blitzcrank.md` | `runs/16.9.1/Blitzcrank/qa/contact-sheet.png` |
| [ ] | Brand (Brand) | planned | planned | planned | planned | planned | `lol-brand` | `briefs/Brand.md` | `runs/16.9.1/Brand/qa/contact-sheet.png` |
| [ ] | Braum (Braum) | planned | planned | planned | planned | planned | `lol-braum` | `briefs/Braum.md` | `runs/16.9.1/Braum/qa/contact-sheet.png` |
| [ ] | Briar (Briar) | planned | planned | planned | planned | planned | `lol-briar` | `briefs/Briar.md` | `runs/16.9.1/Briar/qa/contact-sheet.png` |
| [ ] | Caitlyn (Caitlyn) | planned | planned | planned | planned | planned | `lol-caitlyn` | `briefs/Caitlyn.md` | `runs/16.9.1/Caitlyn/qa/contact-sheet.png` |
| [ ] | Camille (Camille) | planned | planned | planned | planned | planned | `lol-camille` | `briefs/Camille.md` | `runs/16.9.1/Camille/qa/contact-sheet.png` |
| [ ] | Cassiopeia (Cassiopeia) | planned | planned | planned | planned | planned | `lol-cassiopeia` | `briefs/Cassiopeia.md` | `runs/16.9.1/Cassiopeia/qa/contact-sheet.png` |
| [ ] | Cho'Gath (Chogath) | planned | planned | planned | planned | planned | `lol-chogath` | `briefs/Chogath.md` | `runs/16.9.1/Chogath/qa/contact-sheet.png` |
| [ ] | Corki (Corki) | planned | planned | planned | planned | planned | `lol-corki` | `briefs/Corki.md` | `runs/16.9.1/Corki/qa/contact-sheet.png` |
| [x] | Darius (Darius) | accepted | accepted | accepted | accepted | accepted | `lol-darius` | `briefs/Darius.md` | `runs/16.9.1/Darius/qa/contact-sheet.png` |
| [ ] | Diana (Diana) | planned | planned | planned | planned | planned | `lol-diana` | `briefs/Diana.md` | `runs/16.9.1/Diana/qa/contact-sheet.png` |
| [ ] | Dr. Mundo (DrMundo) | planned | planned | planned | planned | planned | `lol-drmundo` | `briefs/DrMundo.md` | `runs/16.9.1/DrMundo/qa/contact-sheet.png` |
| [ ] | Draven (Draven) | planned | planned | planned | planned | planned | `lol-draven` | `briefs/Draven.md` | `runs/16.9.1/Draven/qa/contact-sheet.png` |
| [ ] | Ekko (Ekko) | planned | planned | planned | planned | planned | `lol-ekko` | `briefs/Ekko.md` | `runs/16.9.1/Ekko/qa/contact-sheet.png` |
| [ ] | Elise (Elise) | planned | planned | planned | planned | planned | `lol-elise` | `briefs/Elise.md` | `runs/16.9.1/Elise/qa/contact-sheet.png` |
| [ ] | Evelynn (Evelynn) | planned | planned | planned | planned | planned | `lol-evelynn` | `briefs/Evelynn.md` | `runs/16.9.1/Evelynn/qa/contact-sheet.png` |
| [ ] | Ezreal (Ezreal) | planned | planned | planned | planned | planned | `lol-ezreal` | `briefs/Ezreal.md` | `runs/16.9.1/Ezreal/qa/contact-sheet.png` |
| [ ] | Fiddlesticks (Fiddlesticks) | planned | planned | planned | planned | planned | `lol-fiddlesticks` | `briefs/Fiddlesticks.md` | `runs/16.9.1/Fiddlesticks/qa/contact-sheet.png` |
| [ ] | Fiora (Fiora) | planned | planned | planned | planned | planned | `lol-fiora` | `briefs/Fiora.md` | `runs/16.9.1/Fiora/qa/contact-sheet.png` |
| [ ] | Fizz (Fizz) | planned | planned | planned | planned | planned | `lol-fizz` | `briefs/Fizz.md` | `runs/16.9.1/Fizz/qa/contact-sheet.png` |
| [ ] | Galio (Galio) | planned | planned | planned | planned | planned | `lol-galio` | `briefs/Galio.md` | `runs/16.9.1/Galio/qa/contact-sheet.png` |
| [ ] | Gangplank (Gangplank) | planned | planned | planned | planned | planned | `lol-gangplank` | `briefs/Gangplank.md` | `runs/16.9.1/Gangplank/qa/contact-sheet.png` |
| [ ] | Garen (Garen) | planned | planned | planned | planned | planned | `lol-garen` | `briefs/Garen.md` | `runs/16.9.1/Garen/qa/contact-sheet.png` |
| [ ] | Gnar (Gnar) | planned | planned | planned | planned | planned | `lol-gnar` | `briefs/Gnar.md` | `runs/16.9.1/Gnar/qa/contact-sheet.png` |
| [x] | Gragas (Gragas) | accepted | accepted | accepted | accepted | accepted | `lol-gragas` | `briefs/Gragas.md` | `runs/16.9.1/Gragas/qa/contact-sheet.png` |
| [ ] | Graves (Graves) | planned | planned | planned | planned | planned | `lol-graves` | `briefs/Graves.md` | `runs/16.9.1/Graves/qa/contact-sheet.png` |
| [ ] | Gwen (Gwen) | planned | planned | planned | planned | planned | `lol-gwen` | `briefs/Gwen.md` | `runs/16.9.1/Gwen/qa/contact-sheet.png` |
| [ ] | Hecarim (Hecarim) | planned | planned | planned | planned | planned | `lol-hecarim` | `briefs/Hecarim.md` | `runs/16.9.1/Hecarim/qa/contact-sheet.png` |
| [ ] | Heimerdinger (Heimerdinger) | planned | planned | planned | planned | planned | `lol-heimerdinger` | `briefs/Heimerdinger.md` | `runs/16.9.1/Heimerdinger/qa/contact-sheet.png` |
| [ ] | Hwei (Hwei) | planned | planned | planned | planned | planned | `lol-hwei` | `briefs/Hwei.md` | `runs/16.9.1/Hwei/qa/contact-sheet.png` |
| [ ] | Illaoi (Illaoi) | planned | planned | planned | planned | planned | `lol-illaoi` | `briefs/Illaoi.md` | `runs/16.9.1/Illaoi/qa/contact-sheet.png` |
| [ ] | Irelia (Irelia) | planned | planned | planned | planned | planned | `lol-irelia` | `briefs/Irelia.md` | `runs/16.9.1/Irelia/qa/contact-sheet.png` |
| [ ] | Ivern (Ivern) | planned | planned | planned | planned | planned | `lol-ivern` | `briefs/Ivern.md` | `runs/16.9.1/Ivern/qa/contact-sheet.png` |
| [ ] | Janna (Janna) | planned | planned | planned | planned | planned | `lol-janna` | `briefs/Janna.md` | `runs/16.9.1/Janna/qa/contact-sheet.png` |
| [ ] | Jarvan IV (JarvanIV) | planned | planned | planned | planned | planned | `lol-jarvaniv` | `briefs/JarvanIV.md` | `runs/16.9.1/JarvanIV/qa/contact-sheet.png` |
| [ ] | Jax (Jax) | planned | planned | planned | planned | planned | `lol-jax` | `briefs/Jax.md` | `runs/16.9.1/Jax/qa/contact-sheet.png` |
| [ ] | Jayce (Jayce) | planned | planned | planned | planned | planned | `lol-jayce` | `briefs/Jayce.md` | `runs/16.9.1/Jayce/qa/contact-sheet.png` |
| [ ] | Jhin (Jhin) | planned | planned | planned | planned | planned | `lol-jhin` | `briefs/Jhin.md` | `runs/16.9.1/Jhin/qa/contact-sheet.png` |
| [ ] | Jinx (Jinx) | planned | planned | planned | planned | planned | `lol-jinx` | `briefs/Jinx.md` | `runs/16.9.1/Jinx/qa/contact-sheet.png` |
| [ ] | K'Sante (KSante) | planned | planned | planned | planned | planned | `lol-ksante` | `briefs/KSante.md` | `runs/16.9.1/KSante/qa/contact-sheet.png` |
| [ ] | Kai'Sa (Kaisa) | planned | planned | planned | planned | planned | `lol-kaisa` | `briefs/Kaisa.md` | `runs/16.9.1/Kaisa/qa/contact-sheet.png` |
| [ ] | Kalista (Kalista) | planned | planned | planned | planned | planned | `lol-kalista` | `briefs/Kalista.md` | `runs/16.9.1/Kalista/qa/contact-sheet.png` |
| [ ] | Karma (Karma) | planned | planned | planned | planned | planned | `lol-karma` | `briefs/Karma.md` | `runs/16.9.1/Karma/qa/contact-sheet.png` |
| [ ] | Karthus (Karthus) | planned | planned | planned | planned | planned | `lol-karthus` | `briefs/Karthus.md` | `runs/16.9.1/Karthus/qa/contact-sheet.png` |
| [ ] | Kassadin (Kassadin) | planned | planned | planned | planned | planned | `lol-kassadin` | `briefs/Kassadin.md` | `runs/16.9.1/Kassadin/qa/contact-sheet.png` |
| [ ] | Katarina (Katarina) | planned | planned | planned | planned | planned | `lol-katarina` | `briefs/Katarina.md` | `runs/16.9.1/Katarina/qa/contact-sheet.png` |
| [ ] | Kayle (Kayle) | planned | planned | planned | planned | planned | `lol-kayle` | `briefs/Kayle.md` | `runs/16.9.1/Kayle/qa/contact-sheet.png` |
| [ ] | Kayn (Kayn) | planned | planned | planned | planned | planned | `lol-kayn` | `briefs/Kayn.md` | `runs/16.9.1/Kayn/qa/contact-sheet.png` |
| [ ] | Kennen (Kennen) | planned | planned | planned | planned | planned | `lol-kennen` | `briefs/Kennen.md` | `runs/16.9.1/Kennen/qa/contact-sheet.png` |
| [ ] | Kha'Zix (Khazix) | planned | planned | planned | planned | planned | `lol-khazix` | `briefs/Khazix.md` | `runs/16.9.1/Khazix/qa/contact-sheet.png` |
| [ ] | Kindred (Kindred) | planned | planned | planned | planned | planned | `lol-kindred` | `briefs/Kindred.md` | `runs/16.9.1/Kindred/qa/contact-sheet.png` |
| [ ] | Kled (Kled) | planned | planned | planned | planned | planned | `lol-kled` | `briefs/Kled.md` | `runs/16.9.1/Kled/qa/contact-sheet.png` |
| [ ] | Kog'Maw (KogMaw) | planned | planned | planned | planned | planned | `lol-kogmaw` | `briefs/KogMaw.md` | `runs/16.9.1/KogMaw/qa/contact-sheet.png` |
| [ ] | LeBlanc (Leblanc) | planned | planned | planned | planned | planned | `lol-leblanc` | `briefs/Leblanc.md` | `runs/16.9.1/Leblanc/qa/contact-sheet.png` |
| [ ] | Lee Sin (LeeSin) | planned | planned | planned | planned | planned | `lol-leesin` | `briefs/LeeSin.md` | `runs/16.9.1/LeeSin/qa/contact-sheet.png` |
| [ ] | Leona (Leona) | planned | planned | planned | planned | planned | `lol-leona` | `briefs/Leona.md` | `runs/16.9.1/Leona/qa/contact-sheet.png` |
| [ ] | Lillia (Lillia) | planned | planned | planned | planned | planned | `lol-lillia` | `briefs/Lillia.md` | `runs/16.9.1/Lillia/qa/contact-sheet.png` |
| [ ] | Lissandra (Lissandra) | planned | planned | planned | planned | planned | `lol-lissandra` | `briefs/Lissandra.md` | `runs/16.9.1/Lissandra/qa/contact-sheet.png` |
| [ ] | Lucian (Lucian) | planned | planned | planned | planned | planned | `lol-lucian` | `briefs/Lucian.md` | `runs/16.9.1/Lucian/qa/contact-sheet.png` |
| [ ] | Lulu (Lulu) | planned | planned | planned | planned | planned | `lol-lulu` | `briefs/Lulu.md` | `runs/16.9.1/Lulu/qa/contact-sheet.png` |
| [ ] | Lux (Lux) | planned | planned | planned | planned | planned | `lol-lux` | `briefs/Lux.md` | `runs/16.9.1/Lux/qa/contact-sheet.png` |
| [ ] | Malphite (Malphite) | planned | planned | planned | planned | planned | `lol-malphite` | `briefs/Malphite.md` | `runs/16.9.1/Malphite/qa/contact-sheet.png` |
| [ ] | Malzahar (Malzahar) | planned | planned | planned | planned | planned | `lol-malzahar` | `briefs/Malzahar.md` | `runs/16.9.1/Malzahar/qa/contact-sheet.png` |
| [ ] | Maokai (Maokai) | planned | planned | planned | planned | planned | `lol-maokai` | `briefs/Maokai.md` | `runs/16.9.1/Maokai/qa/contact-sheet.png` |
| [ ] | Master Yi (MasterYi) | planned | planned | planned | planned | planned | `lol-masteryi` | `briefs/MasterYi.md` | `runs/16.9.1/MasterYi/qa/contact-sheet.png` |
| [ ] | Mel (Mel) | planned | planned | planned | planned | planned | `lol-mel` | `briefs/Mel.md` | `runs/16.9.1/Mel/qa/contact-sheet.png` |
| [ ] | Milio (Milio) | planned | planned | planned | planned | planned | `lol-milio` | `briefs/Milio.md` | `runs/16.9.1/Milio/qa/contact-sheet.png` |
| [ ] | Miss Fortune (MissFortune) | planned | planned | planned | planned | planned | `lol-missfortune` | `briefs/MissFortune.md` | `runs/16.9.1/MissFortune/qa/contact-sheet.png` |
| [ ] | Mordekaiser (Mordekaiser) | planned | planned | planned | planned | planned | `lol-mordekaiser` | `briefs/Mordekaiser.md` | `runs/16.9.1/Mordekaiser/qa/contact-sheet.png` |
| [ ] | Morgana (Morgana) | planned | planned | planned | planned | planned | `lol-morgana` | `briefs/Morgana.md` | `runs/16.9.1/Morgana/qa/contact-sheet.png` |
| [ ] | Naafiri (Naafiri) | planned | planned | planned | planned | planned | `lol-naafiri` | `briefs/Naafiri.md` | `runs/16.9.1/Naafiri/qa/contact-sheet.png` |
| [ ] | Nami (Nami) | planned | planned | planned | planned | planned | `lol-nami` | `briefs/Nami.md` | `runs/16.9.1/Nami/qa/contact-sheet.png` |
| [ ] | Nasus (Nasus) | planned | planned | planned | planned | planned | `lol-nasus` | `briefs/Nasus.md` | `runs/16.9.1/Nasus/qa/contact-sheet.png` |
| [ ] | Nautilus (Nautilus) | planned | planned | planned | planned | planned | `lol-nautilus` | `briefs/Nautilus.md` | `runs/16.9.1/Nautilus/qa/contact-sheet.png` |
| [x] | Neeko (Neeko) | accepted | accepted | accepted | accepted | accepted | `lol-neeko` | `briefs/Neeko.md` | `runs/16.9.1/Neeko/qa/contact-sheet.png` |
| [ ] | Nidalee (Nidalee) | planned | planned | planned | planned | planned | `lol-nidalee` | `briefs/Nidalee.md` | `runs/16.9.1/Nidalee/qa/contact-sheet.png` |
| [ ] | Nilah (Nilah) | planned | planned | planned | planned | planned | `lol-nilah` | `briefs/Nilah.md` | `runs/16.9.1/Nilah/qa/contact-sheet.png` |
| [ ] | Nocturne (Nocturne) | planned | planned | planned | planned | planned | `lol-nocturne` | `briefs/Nocturne.md` | `runs/16.9.1/Nocturne/qa/contact-sheet.png` |
| [ ] | Nunu & Willump (Nunu) | planned | planned | planned | planned | planned | `lol-nunu` | `briefs/Nunu.md` | `runs/16.9.1/Nunu/qa/contact-sheet.png` |
| [ ] | Olaf (Olaf) | planned | planned | planned | planned | planned | `lol-olaf` | `briefs/Olaf.md` | `runs/16.9.1/Olaf/qa/contact-sheet.png` |
| [ ] | Orianna (Orianna) | planned | planned | planned | planned | planned | `lol-orianna` | `briefs/Orianna.md` | `runs/16.9.1/Orianna/qa/contact-sheet.png` |
| [ ] | Ornn (Ornn) | planned | planned | planned | planned | planned | `lol-ornn` | `briefs/Ornn.md` | `runs/16.9.1/Ornn/qa/contact-sheet.png` |
| [ ] | Pantheon (Pantheon) | planned | planned | planned | planned | planned | `lol-pantheon` | `briefs/Pantheon.md` | `runs/16.9.1/Pantheon/qa/contact-sheet.png` |
| [ ] | Poppy (Poppy) | planned | planned | planned | planned | planned | `lol-poppy` | `briefs/Poppy.md` | `runs/16.9.1/Poppy/qa/contact-sheet.png` |
| [ ] | Pyke (Pyke) | planned | planned | planned | planned | planned | `lol-pyke` | `briefs/Pyke.md` | `runs/16.9.1/Pyke/qa/contact-sheet.png` |
| [ ] | Qiyana (Qiyana) | planned | planned | planned | planned | planned | `lol-qiyana` | `briefs/Qiyana.md` | `runs/16.9.1/Qiyana/qa/contact-sheet.png` |
| [ ] | Quinn (Quinn) | planned | planned | planned | planned | planned | `lol-quinn` | `briefs/Quinn.md` | `runs/16.9.1/Quinn/qa/contact-sheet.png` |
| [ ] | Rakan (Rakan) | planned | planned | planned | planned | planned | `lol-rakan` | `briefs/Rakan.md` | `runs/16.9.1/Rakan/qa/contact-sheet.png` |
| [ ] | Rammus (Rammus) | planned | planned | planned | planned | planned | `lol-rammus` | `briefs/Rammus.md` | `runs/16.9.1/Rammus/qa/contact-sheet.png` |
| [x] | Rek'Sai (RekSai) | accepted | accepted | accepted | accepted | accepted | `lol-reksai` | `briefs/RekSai.md` | `runs/16.9.1/RekSai/qa/contact-sheet.png` |
| [ ] | Rell (Rell) | planned | planned | planned | planned | planned | `lol-rell` | `briefs/Rell.md` | `runs/16.9.1/Rell/qa/contact-sheet.png` |
| [ ] | Renata Glasc (Renata) | planned | planned | planned | planned | planned | `lol-renata` | `briefs/Renata.md` | `runs/16.9.1/Renata/qa/contact-sheet.png` |
| [ ] | Renekton (Renekton) | planned | planned | planned | planned | planned | `lol-renekton` | `briefs/Renekton.md` | `runs/16.9.1/Renekton/qa/contact-sheet.png` |
| [ ] | Rengar (Rengar) | planned | planned | planned | planned | planned | `lol-rengar` | `briefs/Rengar.md` | `runs/16.9.1/Rengar/qa/contact-sheet.png` |
| [ ] | Riven (Riven) | planned | planned | planned | planned | planned | `lol-riven` | `briefs/Riven.md` | `runs/16.9.1/Riven/qa/contact-sheet.png` |
| [ ] | Rumble (Rumble) | planned | planned | planned | planned | planned | `lol-rumble` | `briefs/Rumble.md` | `runs/16.9.1/Rumble/qa/contact-sheet.png` |
| [ ] | Ryze (Ryze) | planned | planned | planned | planned | planned | `lol-ryze` | `briefs/Ryze.md` | `runs/16.9.1/Ryze/qa/contact-sheet.png` |
| [ ] | Samira (Samira) | planned | planned | planned | planned | planned | `lol-samira` | `briefs/Samira.md` | `runs/16.9.1/Samira/qa/contact-sheet.png` |
| [ ] | Sejuani (Sejuani) | planned | planned | planned | planned | planned | `lol-sejuani` | `briefs/Sejuani.md` | `runs/16.9.1/Sejuani/qa/contact-sheet.png` |
| [ ] | Senna (Senna) | planned | planned | planned | planned | planned | `lol-senna` | `briefs/Senna.md` | `runs/16.9.1/Senna/qa/contact-sheet.png` |
| [ ] | Seraphine (Seraphine) | planned | planned | planned | planned | planned | `lol-seraphine` | `briefs/Seraphine.md` | `runs/16.9.1/Seraphine/qa/contact-sheet.png` |
| [ ] | Sett (Sett) | planned | planned | planned | planned | planned | `lol-sett` | `briefs/Sett.md` | `runs/16.9.1/Sett/qa/contact-sheet.png` |
| [ ] | Shaco (Shaco) | planned | planned | planned | planned | planned | `lol-shaco` | `briefs/Shaco.md` | `runs/16.9.1/Shaco/qa/contact-sheet.png` |
| [ ] | Shen (Shen) | planned | planned | planned | planned | planned | `lol-shen` | `briefs/Shen.md` | `runs/16.9.1/Shen/qa/contact-sheet.png` |
| [ ] | Shyvana (Shyvana) | planned | planned | planned | planned | planned | `lol-shyvana` | `briefs/Shyvana.md` | `runs/16.9.1/Shyvana/qa/contact-sheet.png` |
| [ ] | Singed (Singed) | planned | planned | planned | planned | planned | `lol-singed` | `briefs/Singed.md` | `runs/16.9.1/Singed/qa/contact-sheet.png` |
| [ ] | Sion (Sion) | planned | planned | planned | planned | planned | `lol-sion` | `briefs/Sion.md` | `runs/16.9.1/Sion/qa/contact-sheet.png` |
| [ ] | Sivir (Sivir) | planned | planned | planned | planned | planned | `lol-sivir` | `briefs/Sivir.md` | `runs/16.9.1/Sivir/qa/contact-sheet.png` |
| [ ] | Skarner (Skarner) | planned | planned | planned | planned | planned | `lol-skarner` | `briefs/Skarner.md` | `runs/16.9.1/Skarner/qa/contact-sheet.png` |
| [ ] | Smolder (Smolder) | planned | planned | planned | planned | planned | `lol-smolder` | `briefs/Smolder.md` | `runs/16.9.1/Smolder/qa/contact-sheet.png` |
| [ ] | Sona (Sona) | planned | planned | planned | planned | planned | `lol-sona` | `briefs/Sona.md` | `runs/16.9.1/Sona/qa/contact-sheet.png` |
| [ ] | Soraka (Soraka) | planned | planned | planned | planned | planned | `lol-soraka` | `briefs/Soraka.md` | `runs/16.9.1/Soraka/qa/contact-sheet.png` |
| [ ] | Swain (Swain) | planned | planned | planned | planned | planned | `lol-swain` | `briefs/Swain.md` | `runs/16.9.1/Swain/qa/contact-sheet.png` |
| [ ] | Sylas (Sylas) | planned | planned | planned | planned | planned | `lol-sylas` | `briefs/Sylas.md` | `runs/16.9.1/Sylas/qa/contact-sheet.png` |
| [ ] | Syndra (Syndra) | planned | planned | planned | planned | planned | `lol-syndra` | `briefs/Syndra.md` | `runs/16.9.1/Syndra/qa/contact-sheet.png` |
| [ ] | Tahm Kench (TahmKench) | planned | planned | planned | planned | planned | `lol-tahmkench` | `briefs/TahmKench.md` | `runs/16.9.1/TahmKench/qa/contact-sheet.png` |
| [ ] | Taliyah (Taliyah) | planned | planned | planned | planned | planned | `lol-taliyah` | `briefs/Taliyah.md` | `runs/16.9.1/Taliyah/qa/contact-sheet.png` |
| [ ] | Talon (Talon) | planned | planned | planned | planned | planned | `lol-talon` | `briefs/Talon.md` | `runs/16.9.1/Talon/qa/contact-sheet.png` |
| [ ] | Taric (Taric) | planned | planned | planned | planned | planned | `lol-taric` | `briefs/Taric.md` | `runs/16.9.1/Taric/qa/contact-sheet.png` |
| [ ] | Teemo (Teemo) | planned | planned | planned | planned | planned | `lol-teemo` | `briefs/Teemo.md` | `runs/16.9.1/Teemo/qa/contact-sheet.png` |
| [ ] | Thresh (Thresh) | planned | planned | planned | planned | planned | `lol-thresh` | `briefs/Thresh.md` | `runs/16.9.1/Thresh/qa/contact-sheet.png` |
| [ ] | Tristana (Tristana) | planned | planned | planned | planned | planned | `lol-tristana` | `briefs/Tristana.md` | `runs/16.9.1/Tristana/qa/contact-sheet.png` |
| [ ] | Trundle (Trundle) | planned | planned | planned | planned | planned | `lol-trundle` | `briefs/Trundle.md` | `runs/16.9.1/Trundle/qa/contact-sheet.png` |
| [ ] | Tryndamere (Tryndamere) | planned | planned | planned | planned | planned | `lol-tryndamere` | `briefs/Tryndamere.md` | `runs/16.9.1/Tryndamere/qa/contact-sheet.png` |
| [ ] | Twisted Fate (TwistedFate) | planned | planned | planned | planned | planned | `lol-twistedfate` | `briefs/TwistedFate.md` | `runs/16.9.1/TwistedFate/qa/contact-sheet.png` |
| [ ] | Twitch (Twitch) | planned | planned | planned | planned | planned | `lol-twitch` | `briefs/Twitch.md` | `runs/16.9.1/Twitch/qa/contact-sheet.png` |
| [ ] | Udyr (Udyr) | planned | planned | planned | planned | planned | `lol-udyr` | `briefs/Udyr.md` | `runs/16.9.1/Udyr/qa/contact-sheet.png` |
| [ ] | Urgot (Urgot) | planned | planned | planned | planned | planned | `lol-urgot` | `briefs/Urgot.md` | `runs/16.9.1/Urgot/qa/contact-sheet.png` |
| [ ] | Varus (Varus) | planned | planned | planned | planned | planned | `lol-varus` | `briefs/Varus.md` | `runs/16.9.1/Varus/qa/contact-sheet.png` |
| [ ] | Vayne (Vayne) | planned | planned | planned | planned | planned | `lol-vayne` | `briefs/Vayne.md` | `runs/16.9.1/Vayne/qa/contact-sheet.png` |
| [ ] | Veigar (Veigar) | planned | planned | planned | planned | planned | `lol-veigar` | `briefs/Veigar.md` | `runs/16.9.1/Veigar/qa/contact-sheet.png` |
| [ ] | Vel'Koz (Velkoz) | planned | planned | planned | planned | planned | `lol-velkoz` | `briefs/Velkoz.md` | `runs/16.9.1/Velkoz/qa/contact-sheet.png` |
| [ ] | Vex (Vex) | planned | planned | planned | planned | planned | `lol-vex` | `briefs/Vex.md` | `runs/16.9.1/Vex/qa/contact-sheet.png` |
| [ ] | Vi (Vi) | planned | planned | planned | planned | planned | `lol-vi` | `briefs/Vi.md` | `runs/16.9.1/Vi/qa/contact-sheet.png` |
| [ ] | Viego (Viego) | planned | planned | planned | planned | planned | `lol-viego` | `briefs/Viego.md` | `runs/16.9.1/Viego/qa/contact-sheet.png` |
| [ ] | Viktor (Viktor) | planned | planned | planned | planned | planned | `lol-viktor` | `briefs/Viktor.md` | `runs/16.9.1/Viktor/qa/contact-sheet.png` |
| [ ] | Vladimir (Vladimir) | planned | planned | planned | planned | planned | `lol-vladimir` | `briefs/Vladimir.md` | `runs/16.9.1/Vladimir/qa/contact-sheet.png` |
| [ ] | Volibear (Volibear) | planned | planned | planned | planned | planned | `lol-volibear` | `briefs/Volibear.md` | `runs/16.9.1/Volibear/qa/contact-sheet.png` |
| [ ] | Warwick (Warwick) | planned | planned | planned | planned | planned | `lol-warwick` | `briefs/Warwick.md` | `runs/16.9.1/Warwick/qa/contact-sheet.png` |
| [ ] | Wukong (MonkeyKing) | planned | planned | planned | planned | planned | `lol-monkeyking` | `briefs/MonkeyKing.md` | `runs/16.9.1/MonkeyKing/qa/contact-sheet.png` |
| [ ] | Xayah (Xayah) | planned | planned | planned | planned | planned | `lol-xayah` | `briefs/Xayah.md` | `runs/16.9.1/Xayah/qa/contact-sheet.png` |
| [ ] | Xerath (Xerath) | planned | planned | planned | planned | planned | `lol-xerath` | `briefs/Xerath.md` | `runs/16.9.1/Xerath/qa/contact-sheet.png` |
| [ ] | Xin Zhao (XinZhao) | planned | planned | planned | planned | planned | `lol-xinzhao` | `briefs/XinZhao.md` | `runs/16.9.1/XinZhao/qa/contact-sheet.png` |
| [ ] | Yasuo (Yasuo) | planned | planned | planned | planned | planned | `lol-yasuo` | `briefs/Yasuo.md` | `runs/16.9.1/Yasuo/qa/contact-sheet.png` |
| [ ] | Yone (Yone) | planned | planned | planned | planned | planned | `lol-yone` | `briefs/Yone.md` | `runs/16.9.1/Yone/qa/contact-sheet.png` |
| [ ] | Yorick (Yorick) | planned | planned | planned | planned | planned | `lol-yorick` | `briefs/Yorick.md` | `runs/16.9.1/Yorick/qa/contact-sheet.png` |
| [ ] | Yunara (Yunara) | planned | planned | planned | planned | planned | `lol-yunara` | `briefs/Yunara.md` | `runs/16.9.1/Yunara/qa/contact-sheet.png` |
| [ ] | Yuumi (Yuumi) | planned | planned | planned | planned | planned | `lol-yuumi` | `briefs/Yuumi.md` | `runs/16.9.1/Yuumi/qa/contact-sheet.png` |
| [ ] | Zaahen (Zaahen) | planned | planned | planned | planned | planned | `lol-zaahen` | `briefs/Zaahen.md` | `runs/16.9.1/Zaahen/qa/contact-sheet.png` |
| [ ] | Zac (Zac) | planned | planned | planned | planned | planned | `lol-zac` | `briefs/Zac.md` | `runs/16.9.1/Zac/qa/contact-sheet.png` |
| [ ] | Zed (Zed) | planned | planned | planned | planned | planned | `lol-zed` | `briefs/Zed.md` | `runs/16.9.1/Zed/qa/contact-sheet.png` |
| [ ] | Zeri (Zeri) | planned | planned | planned | planned | planned | `lol-zeri` | `briefs/Zeri.md` | `runs/16.9.1/Zeri/qa/contact-sheet.png` |
| [ ] | Ziggs (Ziggs) | planned | planned | planned | planned | planned | `lol-ziggs` | `briefs/Ziggs.md` | `runs/16.9.1/Ziggs/qa/contact-sheet.png` |
| [ ] | Zilean (Zilean) | planned | planned | planned | planned | planned | `lol-zilean` | `briefs/Zilean.md` | `runs/16.9.1/Zilean/qa/contact-sheet.png` |
| [ ] | Zoe (Zoe) | planned | planned | planned | planned | planned | `lol-zoe` | `briefs/Zoe.md` | `runs/16.9.1/Zoe/qa/contact-sheet.png` |
| [ ] | Zyra (Zyra) | planned | planned | planned | planned | planned | `lol-zyra` | `briefs/Zyra.md` | `runs/16.9.1/Zyra/qa/contact-sheet.png` |
