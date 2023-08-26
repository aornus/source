---
title: Music🎵
mathjax: true
date: 2022-02-03 11:00:32
updated:
type:
aside: false
description: 包含从初高中时代到大学时代喜欢的歌，有很多在导入时候丢失了，歌单没有特别的顺序。
keywords: 歌单, Spotify
top_img: "repeating-linear-gradient(90deg, hsla(285,0%,67%,0.05) 0px, hsla(285,0%,67%,0.05) 1px,transparent 1px, transparent 96px),repeating-linear-gradient(0deg, hsla(285,0%,67%,0.05) 0px, hsla(285,0%,67%,0.05) 1px,transparent 1px, transparent 96px),repeating-linear-gradient(0deg, hsla(285,0%,67%,0.08) 0px, hsla(285,0%,67%,0.08) 1px,transparent 1px, transparent 12px),repeating-linear-gradient(90deg, hsla(285,0%,67%,0.08) 0px, hsla(285,0%,67%,0.08) 1px,transparent 1px, transparent 12px),linear-gradient(90deg, rgb(79, 30, 203),rgb(252,69,69));"
aplayer: true
comments: false
highlight_shrink:
---

{% note success %}
本页从属于秉蕳的**阅读、摄影、音乐、写作统计计划**
<p align="right">✍更新于2023.8.26</p>
{% endnote %}


# 统计
音乐不仅仅是一种消遣，更是一种记忆、情绪的寄托，每每听到曾经听过的歌，彼时的记忆便喷薄而出，今昔对比，回味无穷。

Music serves as a powerful mood enhancer, shielding me from the disheartening sounds of  surroundings. More importantly, it ignites a fiery passion when its style resonates with my thoughts, so its valueable to record the music we listen in order to keep memories longer.

记录音乐的方法有很多，最简单方便的就是歌单了，但如果想要更个性化的记录就不得不付诸所谓的Scrobbler服务了。
第一次接触音乐统计是2020年第一次收到的Spotify年度报告[^1]，后来又断断续续用Last.fm来记录听歌历史，但是免费版的限制实在太多，但好在能跟声田联动，自己记录也不用管它。
直到前两天（2023年5月8日晚），在Fdroid转悠，发现了[MusicBrainz](https://musicbrainz.org/)开发的[ListenBrainz](https://listenbrainz.org/)1.4.0版本的app发布了，便摸索了一番。ListenBrainz使用开源的数据来记录，完全开源，对于用户非常友好（开源的力量），不仅支持last.fm的导入，也支持与spotify的联动，还支持数据的导出。这好东西，怎能不用，当晚立时就转移到上面了。
>安卓端上可以用[Pano Scrobbler ](https://sspai.com/post/66715#!)来辅助记录，(甚至可以记录radio-browser上的部分电台，比如：ASIA FM等)
<iframe style="border-radius:12px" src="https://listenbrainz.org/user/siontin/" width="100%" height="719.8" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>


# FM📻
{% aplayer "传统音乐" "中华音乐世界"  "http://radio.chinesemusicworld.com/chinesemusic.ogg" "https://chinesemusicworld.com/wp-content/uploads/2012/03/logo.png" "width:400" "autoplay" %}

{% aplayer "雨声" "纯音乐"  "https://stream.zeno.fm/689zc32y4x8uv" "/images/20221012/Sion_6.svg" "width:400" %}

{% aplayer "天籁古典" "河南网络广播"  "http://lhttp.qingting.fm/live/20210756/64k.mp3" "https://cmsres.dianzhenkeji.com/anonymous/2020/4/24/1253511691526868992.jpg" "width:400"  %}

{% aplayer "动听音乐" "蜻蜓"  "http://lhttp.qingting.fm/live/5022107/64k.mp3" "/images/ava.svg" "width:400" %}

<!-- {% aplayerlist %}
{
    "narrow": false,   
    "autoplay": true,                    
    "mode": "order",                      
    "mutex": true,                 
    "theme": "#e6d0b2",	                
    "preload": "none",                    
    "listmaxheight": "513px", 
    "music": [           
        {
            "title": "传统音乐",
            "author": "中华音乐世界",
            "url": "http://radio.chinesemusicworld.com/chinesemusic.ogg",
            "pic": "https://chinesemusicworld.com/wp-content/uploads/2012/03/logo.png",
        },
        {
            "title": "雨声",
            "author": "纯音乐",
            "url": "https://stream.zeno.fm/689zc32y4x8uv",
        }
        {
            "title": "天籁古典",
            "author": "河南网络广播",
            "url": "http://lhttp.qingting.fm/live/20210756/64k.mp3",
            "pic": "https://cmsres.dianzhenkeji.com/anonymous/2020/4/24/1253511691526868992.jpg",
        },  
    ]     
}
{% endaplayerlist %} -->
{% folding red,  收藏的电台流媒体地址 %}


``` yml
#EXTM3U
#RADIOBROWSERUUID:951b325b-5b78-45ef-bebf-88f9a0f6c250
#EXTINF:-1,华语金曲500首
http://ls.qingting.fm/live/3412131.m3u8?bitrate=64

#RADIOBROWSERUUID:3d11b752-4868-40e0-b792-16bbf2c91e07
#EXTINF:-1,CNR 阅读之声
http://ngcdn014.cnr.cn/live/ylgb/index.m3u8

#RADIOBROWSERUUID:d5acb94f-3374-47ba-9e6b-1c0130feea11
#EXTINF:-1,动听音乐网络电台
http://lhttp.qingting.fm/live/5022107/64k.mp3

#RADIOBROWSERUUID:2bf82625-6e78-445d-afff-e51e53c369a9
#EXTINF:-1,CCTV-13新闻伴音
https://piccpndali.v.myalicdn.com/audio/cctv13_2.m3u8

#RADIOBROWSERUUID:e4599290-f353-478d-b920-7e057d049dd5
#EXTINF:-1,AsiaFM高清音乐台
http://asiafm.hk:8000/asiahd

#RADIOBROWSERUUID:72fa86ec-a990-43d6-98f8-ecc6236ea61e
#EXTINF:-1,雨声轻音乐
https://stream.zeno.fm/689zc32y4x8uv

#RADIOBROWSERUUID:94b627b7-7b61-4478-b797-bcb21973c4bf
#EXTINF:-1,AsiaFM亚洲经典台
http://goldfm.cn:8000/goldfm

#RADIOBROWSERUUID:d2654fee-d6cc-42f1-a4a9-a48ff3fbbb5f
#EXTINF:-1,AsiaFM亞洲熱歌台【192k】
http://asiafm.net:8000/asiafmhot

#RADIOBROWSERUUID:ea5e18e6-8897-417f-bf9c-d696c9d8f887
#EXTINF:-1,AsiaFM HD音樂臺
http://asiafm.hk:8000/asiahd

#RADIOBROWSERUUID:f8d2182f-c84f-11e8-a54a-52543be04c81
#EXTINF:-1,CRI轻松调频
http://sk.cri.cn/915.m3u8

#RADIOBROWSERUUID:701e4c8c-b2c2-42db-a535-65ac13de0e0f
#EXTINF:-1,CNR-1 中国之声
https://piccpndali.v.myalicdn.com/audio/cctv2_2.m3u8?

#RADIOBROWSERUUID:a5bffcf2-3924-40a7-998a-221011fb0a20
#EXTINF:-1,雨声
https://stream.zeno.fm/ckptaagp6x8uv

#RADIOBROWSERUUID:90812afa-6fd4-11e8-83fa-52543be04c81
#EXTINF:-1,CRI Voice of South China Sea
http://sk.cri.cn/nhzs.m3u8

#RADIOBROWSERUUID:4d0b4981-7a88-4f3b-a838-966d1bd7263b
#EXTINF:-1,Chinese Music World
http://radio.chinesemusicworld.com/chinesemusic.ogg

#RADIOBROWSERUUID:3af6f3d6-0fbd-4565-98c0-5488285f2bb9
#EXTINF:-1,AsiaFM亞洲熱歌台【192k】
http://asiafm.net:8000/asiafmhot

#RADIOBROWSERUUID:46c79dfa-1a99-4139-a052-81c434f259dd
#EXTINF:-1,Fred Film Radio(中文)
https://s10.webradio-hosting.com/proxy/fredradiocn/stream

#RADIOBROWSERUUID:4610edcd-9987-4b55-b0f5-87bea6f94377
#EXTINF:-1,民谣·蓝调
http://play-radio-stream3.hndt.com/now/XWfN89gh/chunklist.m3u8

#RADIOBROWSERUUID:177a078b-b787-436e-b641-19f16b6708ef
#EXTINF:-1,河南网络广播·天籁古典
http://lhttp.qingting.fm/live/20210756/64k.mp3

```
{% endfolding %}

# 音乐之旅
{% timeline 音乐之旅 %}
<!-- timeline 2013~2016 小学、初中时代-->
| 📱OS |        塞班         |
|:------:|:------------------------:|
| 🎵软件 |         多米音乐         |
|  🥰喜好  | 七八十年代的华语经典老歌 |
<!-- endtimeline -->
<!-- timeline 2016~2019 高中时代-->
| 📱OS |        塞班        |
|:------:|:------------------------:|
| 🎵软件 |      虾米音乐、QQ音乐         |
|  🥰喜好  | 交响乐、轻音乐、节奏感  |
<!-- endtimeline -->
<!-- timeline 2019~2023 大学时代-->
| 📱OS |        多平台        |
|:------:|:------------------------:|
| 🎵软件 |      Spotify、~~豆瓣FM~~         |
|  🥰喜好  | 流行音乐、节奏感、影视原声  |
<!-- endtimeline -->
{% endtimeline %}

## 实体设备选择
1. ~~黑胶唱片机~~(太贵了)
2. ~~CD唱片播放器(Thinkya Ja-310)~~(刻录与搜寻太麻烦)
3. ~~USB播放器~~(日后再买)
4. 手机

## 歌单

{% folding purple, 耒耨·诺基亚时代歌单回听 %}


1. 初雪 班得瑞
2. 后会无期 邓紫棋
3. 平凡之路 朴树
4. 太阳照常升起 久石让
5. Journey Capozio
6. Secrets AMFB Onerepublic
7. 奥特曼 舞指如歌
8. 奔跑进行曲 
9. 夜斗
10. tetrix(Dirty Saw Mix)
11. Spontaneous Me(Inst.) Lindsey strling
12. With an Orchid 雅尼
13. Reunion Gray Burton
14. 山丹丹开花红艳艳 陈东宝
15. 贝多芬 C小调第七小提琴奏鸣曲

{% endfolding %}

{% folding blue, 歌单：秉蕳♥的歌（2016-2022.8） %}



|                             歌名                             |                             歌手                             |                             专辑                             |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|                        Tell The Truth                        |                      The Avett Brothers                      |                     Closer Than Together                     |
|                   Better When You're Gone                    |                         David Guetta                         |                   Better When You're Gone                    |
|                           Popcorn                            |                         The Muppets                          |                           Popcorn                            |
|                     No Fear In My Heart                      |                            Pu Shu                            |                     朴树 猎户星座 · 专场                     |
|                 bad guy (with Justin Bieber)                 |                        Billie Eilish                         |                 bad guy (with Justin Bieber)                 |
|       Driftveil City (From "Pokemon Black and White")        |                         Chippy Bits                          |              Pokemon Black and White Chiptunes               |
|                     Everytime You Leave                      |                       Sonya Belousova                        |     The Witcher (Music from the Netflix Original Series)     |
|                       Over the Rainbow                       |                    Israel Kamakawiwo'ole                     |                      Alone In Iz World                       |
|                          Rather Be                           |                       Beloved Melodies                       |                       Beloved Melodies                       |
|                           Lifeline                           |                       Geir Gudmundson                        |                           Lifeline                           |
|                          Blue Bird                           |                          Edward Ong                          |                          Blue Bird                           |
|                        In the Clouds                         |                            Astron                            |                        In the Clouds                         |
|     Always With Me (Spirited Away) - Guitar Instrumental     |                          Edward Ong                          |     Always With Me (Spirited Away) [Guitar Instrumental]     |
|                   Butterfly (Anniversary)                    |                           SMiLE.dk                           |                   Butterfly (Anniversary)                    |
|                           Run Free                           |                         Deep Chills                          |                   "Tropical House, Vol. 2"                   |
|                           Backfire                           |                         Deep Chills                          |                           Backfire                           |
|                      Seve - Radio Edit                       |                          Tez Cadey                           |                      Seve (Radio Edit)                       |
|                        Echoes Of Love                        |                         Jesse & Joy                          |                        Echoes Of Love                        |
|                             Baby                             |                        Justin Bieber                         |                         My World 2.0                         |
|                     Mischievous Alchemy                      |                          Amos Roddy                          |           Kingdom Two Crowns (Original Soundtrack)           |
|                        coquelicot 14                         |                        Satoshi Takebe                        |              From Up on Poppy Hill Image Album               |
|                      I Want It That Way                      |                        Tyler and Mark                        |                       Beautiful Dreams                       |
|                          Raindrops                           |                             Giné                             |                          Raindrops                           |
|                             Home                             |                        Rui Fujishiro                         |                       Sentimental Days                       |
|                      You Spin Me Round                       |                          Auralnauts                          |           How to Make a Blockbuster Movie Trailer            |
|              You Spin Me Round (Like a Record)               |                        Dead Or Alive                         |                          Youthquake                          |
| "Piano Sonata No. 11 in A Major, K. 331: III. Rondo alla turca: Allegretto" |                   Wolfgang Amadeus Mozart                    | "Mozart: Piano Sonatas, Vol. 4 (Piano Sonatas Nos. 3, 7, 11 and 18)" |
|                 "Serenade No. 13 in G Major                  | K. 525 ""Eine kleine Nachtmusik"": I. Allegro (Featured in ""Nikita"")" |                   Wolfgang Amadeus Mozart                    |
|                          Night Out                           |                            LiQWYD                            |                          Night Out                           |
|         Ashitaka and San (From "Princess Mononoke")          |                           Lofi Lia                           |         Ashitaka and San (From "Princess Mononoke")          |
|                        coquelicot 13                         |                        Satoshi Takebe                        |              From Up on Poppy Hill Image Album               |
|     One Summer's Day (From "Spirited Away") - Lofi Beat      |                     Celestial Alignment                      |     One Summer's Day (From "Spirited Away") [Lofi Beat]      |
|     One Summer's Day (From "Spirited Away") [Lofi Beat]      |                     Celestial Alignment                      |                   Studio Ghibli Reimagined                   |
|         Bygone Days (From "Porco Rosso") - Lofi Beat         |                     Celestial Alignment                      |              Anime & Chill Lofi Beats for Study              |
|          "Take Me Home, Country Roads - Rerecorded"          |                         John Denver                          | "The John Denver Collection, Vol. 1: Take Me Home Country Roads" |
|                   Daydreamer - Radio Edit                    |                            KARLK                             |                          Crossroads                          |
|                          Astronomia                          |                           Tony Igy                           |                          Astronomia                          |
| Battle Versus Legendary Pokemon (From "Pokemon Black and White") |                         Chippy Bits                          |              Pokemon Black and White Chiptunes               |
|                      Duel of the Fates                       |                        John Williams                         | Star Wars: The Phantom Menace (Original Motion Picture Soundtrack) |
|           The Imperial March (Darth Vader's Theme)           |                        John Williams                         | Star Wars: The Empire Strikes Back (Original Motion Picture Soundtrack) |
|                          英雄也有淚                          |                       中國國家交響樂團                       |                           新水滸傳                           |
|                        Someone To You                        |                           BANNERS                            |                    Where The Shadow Ends                     |
|                           Matsuri                            |                            Kitaro                            |                            Kojiki                            |
|                         Caravansary                          |                            Kitaro                            |                  The Definitive Collection                   |
|                          Die Young                           |                            Kesha                             |                  Warrior (Expanded Edition)                  |
|                            Summer                            |                        Calvin Harris                         |                            Motion                            |
|                       A Thousand Years                       |                       Christina Perri                        |                       A Thousand Years                       |
|                        Phantom Racer                         |                             TWRP                             |                    Together Through Time                     |
|                      Starlight Brigade                       |                             TWRP                             |                    Together Through Time                     |
| Symphonic Suite “Kiki’s Delivery Service” : On a Clear Day 〜 A Town with an Ocean View - Live In Japan / 2019 |                         Joe Hisaishi                         |          Symphonic Suite “Kiki’s Delivery Service”           |
|                             勇者                             |                           矢野立美                           |                           神秘失踪                           |
|                       Angels Will Rise                       |                       Twisted Jukebox                        |                       Angels Will Rise                       |
|                      Last Of The Wilds                       |                          Nightwish                           |                      Dark Passion Play                       |
|               I Will Survive - Single Version                |                        Gloria Gaynor                         |                      Colour Collection                       |
|                       Four Wild Horses                       |                         David Munyon                         |                          Live 2014                           |
|                         Lighthearted                         |                         Deep Chills                          |                         Lighthearted                         |
|                             Home                             |                           Steerner                           |                             Home                             |
|                 Astronomia - Medieval Style                  |                        Cornelius Link                        |                 Astronomia (Medieval Style)                  |
|                    What a Wonderful World                    |                            Raffi                             |                          Let's Play                          |
|                          Only Time                           |                             Enya                             |                      A Day Without Rain                      |
|                     Conquest of Paradise                     |                           Vangelis                           |                  1492: Conquest of Paradise                  |
|                           曾经的你                           |                            Xu Wei                            |                       每一刻都是崭新的                       |
|                             初雪                             |                      Chiharu Matsuyama                       |                         起承転結 14                          |
|                           Refrain                            |                          Anan Ryoko                          |                        Eternal Light                         |
|                         99 Problems                          |                             Hugo                             |                      Old Tyme Religion                       |
|                        With an Orchid                        |                            Yanni                             |                     If I Could Tell You                      |
|                           Children                           |                         Robert Miles                         |                 Children (Dance Vault Mixes)                 |
|                      Bring It All Back                       |                           S Club 7                           |                            S Club                            |
|                  我的身旁是一扇亮了又暗的窗                  |                          理想後花園                          |         街声大登陆合辑Vol.1:这个世界让你紧张害怕吗?          |
|                    Recursive Iteration II                    |                         Ryan Teague                          |                     Recursive Iterations                     |
|                          Tetramery                           |                         Ryan Teague                          |                        Field Drawings                        |
|  "21 Hungarian Dances in F-Sharp Minor, WoO 1: V. Allegro"   |                       Johannes Brahms                        |                   Classic Piano Collection                   |
|                        Driftveil City                        |                             VGR                              |                        Driftveil City                        |
|                           Popcorn                            |                        Edward Simoni                         |                 Die Zauberwelt der Panflöte                  |
|                        A Time For Us                         |                 Frank Chacksfield Orchestra                  |                        A Time for Us                         |
|                   Children of Planet Earth                   |                         Melodysheep                          |                      The Music of Sound                      |
|                          Emergence                           |                        Epic Mountain                         |  "Kurzgesagt, Vol. 4 (Original Motion Picture Soundtrack)"   |
|                         野子 - Live                          |                             Sue                              |               第二季中國好歌曲導師原創: 心宇宙               |
|                             Neo                              |                         Ryan Teague                          |                        Field Drawings                        |
|                          The Shire                           |                         Howard Shore                         | The Lord of the Rings: The Fellowship of the Ring - the Complete Recordings |
|                         Anywhere Is                          |                             Enya                             |                            Oceans                            |
|               How to Train Your Dragon Medley                |                       Taryn Harbridge                        |               How to Train Your Dragon Medley                |
|                    Ballad of the Goddess                     |                            ROZEN                             |                        Sins of Hyrule                        |
|                       Pneumatic Tokyo                        |                             Env                              |                       Pneumatic Tokyo                        |
|                     Crab Rave Orchestral                     |                     TheDancingFishstick                      |                     Crab Rave Orchestral                     |
|             Opening Theme (From "Gravity Falls")             |                       Pontus Hultgren                        |             Opening Theme (From "Gravity Falls")             |
|                           真心英雄                           |                         Jackie Chan                          |                    成龍超級精裝大戲主題曲                    |
|                     時の流れに身をまかせ                     |                         Teresa Teng                          |                      鄧麗君東洋金曲賞03                      |
|                           The Baby                           |                       Ludwig Goransson                       |         The Mandalorian: Chapter 8 (Original Score)          |
|                        Therefore I Am                        |                        Billie Eilish                         |                        Therefore I Am                        |
|                        Echoes in Rain                        |                             Enya                             |                       Dark Sky Island                        |
|                           Señorita                           |                         Simply Three                         |                           Señorita                           |
|                  The King of the Highlands                   |                      Antti Martikainen                       |                      The Last Chronicle                      |
|                           Señorita                           |                         Shawn Mendes                         |                           Señorita                           |
|                            Faded                             |                      Karolina Protsenko                      |                          Sunflower                           |
|                       Blinding Lights                        |                          The Weeknd                          |                         After Hours                          |
|                       Wait Another Day                       |                        Mike Williams                         |                       Wait Another Day                       |
|               "Taking Me High, Taking Me Low"                |                          Gold Flow                           |                           Pioneer                            |
|               Crab Rave - Crazy Piano Version                |                          NPT Music                           |               Crab Rave (Crazy Piano Version)                |
|                         Ievan Polkka                         |                         Middle Ages                          |           Ice and Fire (Medieval Folk Collection)            |
|                      Moves Like Jagger                       |                         TwoPlusFour                          |                      Moves Like Jagger                       |
|               For the Dancing and the Dreaming               |                            Erutan                            |               For the Dancing and the Dreaming               |
|                         Senbonzakura                         |                         Osamuraisan                          |              Shoubu Zenya Gengetsu -Hikite Ban-              |
|                       Moonlight Sonata                       |                            Marcin                            |                       Moonlight Sonata                       |
|                           The Mass                           |                             ERA                              |                           The Mass                           |
|                           Ricochet                           |                       Caitlin De Ville                       |                           Ricochet                           |
|                  Astronomia (Electro Swing)                  |                        Wolfgang Lohr                         |                  Astronomia (Electro Swing)                  |
|                     Leaves From The Vine                     |                      Lofi Fruits Music                       |                     Leaves From The Vine                     |
|                     Take Back The Power                      |                       The Interrupters                       |              The Interrupters (Deluxe Edition)               |
|      Somewhere Over The Rainbow_What A Wonderful World       |                    Israel Kamakawiwo'ole                     |                        Facing Future                         |
|                 Blackbird - Remastered 2009                  |                         The Beatles                          |                   The Beatles (Remastered)                   |
|           King Dedede & Meta Knight Medley (Live)            |                 Tokyo Philharmonic Orchestra                 |           Kirby 25th Anniversary Orchestra Concert           |
|                           Bad Guy                            |                         Kezia Amelia                         |                        All About You                         |
|                       The Mandalorian                        |                       Ludwig Goransson                       |         The Mandalorian: Chapter 1 (Original Score)          |
|        "Take Me Home, Country Roads - Violin Version"        |                          Yuji Nomi                           |               Whisper of the Heart Soundtrack                |
|                          Off Shore                           |                            Geike                             |                         Lost in Time                         |
|                      A-Bit of Star Wars                      |                         Joe Jeremiah                         |                    A-Bit of 8-Bit: Vol. 3                    |
|                  A-Bit of the Mountain King                  |                         Joe Jeremiah                         |                    A-Bit of 8-Bit: Vol. 1                    |
|              A-Bit of Pirates of the Caribbean               |                         Joe Jeremiah                         |                    A-Bit of 8-Bit: Vol. 1                    |
|               Blinding Lights (8 Bit Version)                |                        8 Bit Universe                        |                       Droppin' Boppers                       |
|                          Mr. Roboto                          |                       Super Power Club                       |                          8-Bit 80's                          |
|         Sweet Dreams Are Made of This Medieval Ver.          |                            Alvei                             |         Sweet Dreams Are Made of This Medieval Ver.          |
|     Pokémon Theme (TheFatRat Remix) [feat. Jason Paige]      |                       Video Games Live                       |     Pokémon Theme (TheFatRat Remix) [feat. Jason Paige]      |
|                       We Will Rock You                       |                        8-Bit Misfits                         |                   8-Bit Versions of Queen                    |
|                 The Force (Star Wars Theme)                  |                       Fallen Superhero                       |                 The Force (Star Wars Theme)                  |
|                           奇迹再现                           |                            毛华锋                            |                         永远的奥特曼                         |
|           A Tale of Six Trillion Years and a Night           |                         Shane Rogers                         |                            Change                            |
|                       Blinding Lights                        |                      Invadable Harmony                       |                       The Dream Weaver                       |
|               When Johnny Comes Marching Home                |                           浜口史郎                           |   『ガールズ&パンツァー 劇場版』オリジナルサウンドトラック   |
|                   HandClap (8 Bit Version)                   |                        8 Bit Universe                        |                   "8 Bit Invasion, Vol.2"                    |
|                           HandClap                           |                    Fitz and The Tantrums                     |            Fitz and The Tantrums (Deluxe Edition)            |
|                 Tetris Theme (From "Tetris")                 |                            Mykah                             |                    Video Game Music 2019                     |
|                       桂河大橋 - 口哨                        |                          口琴與口哨                          |                      輕古典/口琴與口哨                       |
|                        Touch the Sky                         |                    Malinda Kathleen Reese                    |                        Touch the Sky                         |
|                         Cereal Killa                         |                        Blue Wednesday                        |                         Beat Tape 1                          |
|                     Gravity Falls Theme                      |                         Cement City                          |               Cement City Vol. 1: Housetrapped               |
|           Go. K.K. Rider! (From "Animal Crossing")           |                             Qumu                             |                            Year 5                            |
|                        Avatar's Love                         |                           Leaflet                            |                        Avatar's Love                         |
|                        Secret Tunnel                         |                           Leaflet                            |                        Secret Tunnel                         |
|                          Torimichi                           |                           Coddneck                           |                          Torimichi                           |
|                cantina band ~ star wars lofi                 |                       Closed on Sunday                       |                cantina band ~ star wars lofi                 |
|                         Cantina Band                         |                        John Williams                         |  Star Wars: A New Hope (Original Motion Picture Soundtrack)  |
|                       Knight's Templar                       |                         Adriel Fair                          |                       Arms of the Wind                       |
|                         Rey's Theme                          |                          Samuel Kim                          |        Star Wars: The Rise of Skywalker Epic Tribute         |
|   Rosalina in the Observatory (From "Super Mario Galaxy")    |                      The 8-Bit Big Band                      |                    Choose Your Character!                    |
|                          Tidal Rush                          |                            Kamex                             |                          Tidal Rush                          |
|                       Over The Rainbow                       |                         Judy Garland                         |          Greatest Performances Original Recordings           |
|                 Battle Call (Album Version)                  |                           Emma Re                            |                           Emma Re                            |
|                  Dance Of The Little Swans                   |                            Flawx                             |                  Dance Of The Little Swans                   |
|                          If I Fail                           |                          Mono Inc.                           |                        Voices of Doom                        |
|            Battle! Gym Leader (Sword and Shield)             |                            Vetrom                            |            Battle! Gym Leader (Sword and Shield)             |
|                         A Part of Us                         |                          Yael Naim                           |        Mon Bébé (Original Motion Picture Soundtrack)         |
|                          My Dreams                           |                          Yael Naim                           |                        She Was a Boy                         |
|                             大海                             |                        Zhang Yu Sheng                        |                             大海                             |
|                            追夢人                            |                            羅大佑                            |                       追夢 (演奏專輯)                        |
|                         Senbonzakura                         |                         Random Piano                         |                         Senbonzakura                         |
|                       Oriental Journey                       |                   Aun J-Classic Orchestra                    |                       Sound Collection                       |
|                         Dragon Tales                         |                        Butterfly Tea                         |                        Celtic Legends                        |
|                         Rainy Days 2                         |                         Mflex Sounds                         |            Electric Time (Kidnap My Soul Edition)            |
|                       Legend of Zelda                        |                            Mikel                             |                        Zelda & Chill                         |
|                          我只在乎你                          |                         Teresa Teng                          |                    BTB 鄧麗君-我只在乎你                     |
|                          Uninvited                           |                      Alfie-Jay Winters                       |                         Autumn Ends                          |
|             Swallowtail Jig (The Dancing Master)             |                         Katy Adelson                         |                       Tune Collection                        |
|                       The Great Speech                       |                     Jonas B. Ingebretsen                     |                     The Musical Journey                      |
|               "Better by You, Better Than Me"                |                         Judas Priest                         |                        Stained Class                         |
|  Medley: Designer Music / I Love Rock'n Roll / Stupid Cupid  |                         Teresa Teng                          |                     君之千言萬語 - 英語1                     |
|                           千千闋歌                           |                        Priscilla Chan                        |                        永遠是你的朋友                        |
|                         Breathtaking                         |                       The Chalkeaters                        |                         Breathtaking                         |
|                           Secrets                            |                        Bryson Andres                         |                           Secrets                            |
|                        Glad You Came                         |                      Faux Alexanderson                       |                    "Time Machine, Pt. 2"                     |
|                           Memories                           |                      Invadable Harmony                       |                       The Dream Weaver                       |
|              Magic Night In The Slaughterhouse               |                           Jelonek                            |                           Revenge                            |
|                          Astronomia                          |                         Dylan Locke                          |                          Astronomia                          |
|                           I Lived                            |                         OneRepublic                          |                            Native                            |
|                      Hell Shall Perish                       |                         Efisio Cross                         |                   The Vanquisher of Death                    |
|                           The Maze                           |                       Twisted Jukebox                        |                        Life In Motion                        |
|                             Numb                             |                         Linkin Park                          |                   Meteora (Bonus Edition)                    |
|                       One Man's Dream                        |                            Yanni                             |                     The Essential Yanni                      |
|                         Senbonzakura                         |                        Lizz Robinett                         |                         Senbonzakura                         |
|                      The New Beginning                       |                           Matt Key                           |                      The New Beginning                       |
|                      T'as D'beaux Cieux                      |                       Camping Sauvach                        |                         Petit Monde                          |
|                    Canon Waltz 卡农华尔兹                    |                       Keyshawn Binean                        |                        Forever Canon                         |
|                        Young Forever                         |                            JAY-Z                             |                       The Blueprint 3                        |
|                     If I Ruled The World                     |                          Mike Perry                          |                     If I Ruled The World                     |
|                           不会改变                           |                            謝天笑                            |                             幻觉                             |
|             青い果実/ウルトラマンネクサス(8bit)              |                        Studio Megaane                        |                   ウルトラマン8bit vol.03                    |
|        ザ☆ウルトラマン/ザ☆ウルトラマン(アニメ)(8bit)         |                        Studio Megaane                        |                   ウルトラマン8bit vol.01                    |
|                          最好的安排                          |                            謝天笑                            |                           哈哈大笑                           |
|                       向阳花(2020年版)                       |                            謝天笑                            |                      《再次来临》自选辑                      |
|                           Bluebird                           |                        Alexis Ffrench                        |                          Evolution                           |
|                      Dream It Possible                       |                          Jane Zhang                          |                            我的夢                            |
|                            我相信                            |                            楊培安                            |                        午夜兩點半的我                        |
|           Wellerman vs Ievan Polkka! PIANO BATTLE            |                            PACIL                             |           Wellerman vs Ievan Polkka! PIANO BATTLE            |
|                      Carol of the Fates                      |                          AtinPiano                           |                      Carol of the Fates                      |
|              Still D.R.E. - MusicalBasics Remix              |                        Musicalbasics                         |              Still D.R.E. (MusicalBasics Remix)              |
|                     Farm Village Scenery                     |                        Fumio Hayasaka                        | Akira Kurosawa's Seven Samurai (七人の侍) [Shichinin no Samurai] [Complete Original Soundtrack] |
|          Gershwin / Arr. Harris: Fascinatin' Rhythm          |                       George Gershwin                        |                 Icon: Menuhin and Grappelli                  |
|                             Nine                             |                       Sleeping At Last                       |                       Atlas: Enneagram                       |
|                          Wake Me Up                          |                            Avicii                            |                             TRUE                             |
|                         Misere Mani                          |                             ERA                              |                            Era II                            |
|                    紅の豚: Madness - Live                    |                         Joe Hisaishi                         |           Dream Songs: The Essential Joe Hisaishi            |
|                       Future Brownies!                       |                          Dein0mite                           |                       Lucid Daydreams                        |
|                       Swing That Horn                        |                         Mary Riddle                          |                    Play Loud March Proud                     |
|                          Rescue Me                           |                         OneRepublic                          |                          Rescue Me                           |
|            Departure but is it okay if it's lofi?            |                            Kijugo                            |            Departure but is it okay if it's lofi?            |
|                      Seven Nation Army                       |                      The White Stripes                       |                           Elephant                           |
|                       The Cursed Path                        |                          Lionel Yu                           |                       The Cursed Path                        |
|                      Yurukyan no theme                       |                       Akiyuki Tateyama                       |           TV anime “Yurukyan△”original sound track           |
|                           Valient                            |                     Shades of the Abyss                      |         Shades of the Abyss (Official Trailer Music)         |
|                        The Wellerman                         |                         Caleb Hyles                          |                        The Wellerman                         |
|                   Terraria Day Theme Remix                   |                      Scott Lloyd Shelly                      |           "Terraria, Vol. 4 (Original Soundtrack)"           |
|                           Secrets                            |                         OneRepublic                          |                          Waking Up                           |
|               Overworld Day (From "Terraria")                |                             Qumu                             |               Overworld Day (From "Terraria")                |
|                         Shape of You                         |                          Ed Sheeran                          |                          ÷ (Deluxe)                          |
|                          Let It Go                           |                        The Piano Guys                        |                              10                              |
|                        The High Seas                         |                             Env                              |                        The High Seas                         |
|              Another Day of Sun - Instrumental               |                            May J.                            |              Cinema Song Covers (Instrumental)               |
|                       Blinding Lights                        |                    Vitamin String Quartet                    |                VSQ Performs the Hits of 2020                 |
|                        Hiragana Song                         |                         Cyber Bunny                          |                        Hiragana Song                         |
|                         Kokoronotizu                         |                      HIRAGANA KAMIYADO                       |                             HRGN                             |
|                       赛马 - 二胡独奏                        |                           华夏乐团                           |                    "国乐贺年金曲, Vol. 1"                    |
|                     猴哥 (西游记动画片)                      |                            张伟进                            |                     猴哥 (西游记动画片)                      |
|                     You Were My Lantern                      |                        Plastic Patina                        |                       Lustrous Lights                        |
|                 Detroit Become Human Hopeful                 |                            Keyson                            |                 Detroit Become Human Hopeful                 |
|                          Luv Letter                          |                         TSUKINOSORA                          |              Tsukinosora 10th Anniversary Best               |
|                           Creative                           |                            Button                            |                           Creative                           |
| In the Hall of the Mountain King (Piano Version) [Edvard Grieg] |                             Myuu                             | In the Hall of the Mountain King (Piano Version) [Edvard Grieg] |
| 打上花火(「打上花火、下から見るか?横から見るか?」より)harp version |                     Kyoto Harp Ensemble                      | 打上花火(「打上花火、下から見るか?横から見るか?」より)harp version |
|                            Busan                             |                         Adam Burgess                         |                Overwatch: Cities & Countries                 |
|                         Dear Calypso                         |                             CG5                              |                         Dear Calypso                         |
|        새벽 별과 소년의 노래 Dawn Star And Boy’S Song        |                       세레노 (Sereno)                        |                         The Serenade                         |
|                            とんぼ                            |                      Tsuyoshi Nagabuchi                      |                        長渕剛 LIVE'89                        |
|                        Discombobulate                        |                         Hans Zimmer                          |     Sherlock Holmes (Original Motion Picture Soundtrack)     |
|                           打上花火                           |                            Daoko                             |                        THANK YOU BLUE                        |
|                            春天裡                            |                          Wang Feng                           |                        信仰在空中飄揚                        |
|                            Scabs                             |                        Bryson Andres                         |                    "Time Machine, Pt. 1"                     |
|                     We All Lift Together                     |                       Freya Catherine                        |                       "Freya, Vol. 3"                        |
|                 Song for Denise - Lofi Remix                 |                          Peng Lexer                          |                 Song for Denise (Lofi Remix)                 |
|               The Spectre - Piano Instrumental               |                           Alan Ng                            |               The Spectre (Piano Instrumental)               |
|                            Faded                             |                         Alan Walker                          |                       Different World                        |
|                          "Primrose                           |           the Dancer (From ""Octopath Traveler"")"           |                        Patti Rudisill                        |
|                      The Last Prophecy                       |                            Synthr                            |                        Horizon Chaser                        |
|                             Nero                             |                          The Speed                           |                             Nero                             |
|                         The Spectre                          |                         Alan Walker                          |                         The Spectre                          |
|                            Winter                            |                           Cydemind                           |                            Winter                            |
|    The Journey Starts Today (Theme from Pokémon Journeys)    |                      Walk Off the Earth                      |    The Journey Starts Today (Theme from Pokémon Journeys)    |
|                      Little Bit of Love                      |                         Tom Grennan                          |                      Little Bit of Love                      |
|            The Periodic Table Song (2018 Update)             |                         AsapSCIENCE                          |            The Periodic Table Song (2018 Update)             |
| Dark Star Core (From: "Mario & Luigi: Bowser's Inside Story") |                       Dinnick the 3rd                        |                   "Electro Covers, Vol. 1"                   |
|       Fire Emblem Theme (from "Fire Emblem: Warriors")       |                       Samantha Ballard                       |       Fire Emblem Theme (from "Fire Emblem: Warriors")       |
|                     Melody of My Dreams                      |                          Whitesand                           |                           Monsters                           |
|                         Spider Dance                         |                       Sheet Music Boss                       |                  Undertale Piano Favourites                  |
|            Can-Can From Orpheus In The Underworld            |                      Jacques Offenbach                       |                   Last Night of the Proms                    |
|               The Path of Wind (Piano & Cello)               |                       Victor Butzelaar                       |               The Path of Wind (Piano & Cello)               |
|                      平凡之路 (钢琴版)                       |                           Jesse T                            |                      平凡之路 (钢琴版)                       |
|                  Skyrim Theme (Dragonborn)                   |                         Celtic Woman                         |                           Destiny                            |
|                          Canon in D                          |                         Jason Piano                          |                         Jason Piano                          |
|                   Canon in D Major - Piano                   |                    Canon in D Variations                     | Variations and Re-inventions on Pachelbel's Canon in D Major |
|                           Bubbles                            |                        Yosi Horikawa                         |                          Wandering                           |
|                           Katyusha                           |                      Mikhail Isakovsky                       |                        Russian Things                        |
|                             国家                             |                           降央卓玛                           |                  中国之声 降央卓玛 3 (翻唱)                  |
|                            黃種人                            |                         Nicholas Tse                         |                    黃 ‧ 鋒 (新曲 + 精選)                     |
|                        陽光總在風雨後                        |                          Mavis Hee                           |                          都是夜歸人                          |
|                           東方之珠                           |                            羅大佑                            |              東方之珠(I) 來自你・來自我・來自他              |
|                         九妹 - Dj版                          |                            唐小力                            |                         九妹 (Dj版)                          |
|                          城裡的月光                          |                          Mavis Hee                           |                             遺憾                             |
|                     Timber (feat. Ke$ha)                     |                           Pitbull                            |          Global Warming: Meltdown (Deluxe Version)           |
|                            青花瓷                            |                           Jay Chou                           |                            我很忙                            |
|                           快樂崇拜                           |                           Will Pan                           |                            Wu Ha                             |
|                          淋雨一直走                          |                         Angela Chang                         |                          有形的翅膀                          |
|                           英雄の詩                           |                          THE ALFEE                           |                           三位一体                           |
|                          summertime                          |                          cinnamons                           |                          summertime                          |
|                 Meditation: Soft Mindfulness                 |                        Jupiter Grains                        |                      Deeper Meditation                       |
|                Next to You (From "Parasyte")                 |                           Ken Arai                           |                Next to You (From "Parasyte")                 |
|                            Demons                            |                           2CELLOS                            |                            Demons                            |
|                      The Awesome Piano                       |                         Peter Bence                          |                Peter Bence: The Awesome Piano                |
|                       Mysterious Paths                       |                        Marco Belloni                         |                       Mysterious Paths                       |
|         One Winged Angel (From "Final Fantasy VII")          |                       Pontus Hultgren                        |         One Winged Angel (From "Final Fantasy VII")          |
|                Demon Slayer Opening "Gurenge"                |                      Friedrich Habetler                      |                Demon Slayer Opening "Gurenge"                |
|                             英雄                             |                             doa                              |                             英雄                             |
|                     Theme from ULTRAMAN                      |                           松本孝弘                           |                       House Of Strings                       |
|                          Crab Wave                           |                           DjUpbeat                           |                          Crab Wave                           |
|  Take to the Sky (A How to Train Your Dragon Orchestration)  |                         Rush Garcia                          |                  "Everything I Have, Vol.3"                  |
|                       Flourishing Age                        |                         Kirara Magic                         |                       Flourishing Age                        |
|            A cruel angel's thesis - Instrumental             |                        Yoko Takahashi                        |            A cruel angel's thesis (Instrumental)             |
|                        夜空中最亮的星                        |                         Escape Plan                          |                             世界                             |
|                       Raise Your Glass                       |                             P!nk                             |                       Raise Your Glass                       |
|                           SAMURAI                            |                             doa                              |                             CAMP                             |
|                     大家一起喜羊羊 - 国                      |                          Bibi Zhou                           |             喜羊羊与灰太狼之虎虎生威电影原声大碟             |
|                             Numb                             |                         Linkin Park                          |                           Meteora                            |
|                      Undercover Martyn                       |                     Two Door Cinema Club                     |                       Tourist History                        |
|                           Horizon                            |                            Janji                             |                           Horizon                            |
|                           Ready to                           |                  影森みちる(CV:諸星すみれ)                   |         アニメ『BNA ビー・エヌ・エー』Complete album         |
|                   Ready to - Instrumental                    |                  影森みちる(CV:諸星すみれ)                   |         アニメ『BNA ビー・エヌ・エー』Complete album         |
|                        Zen Zen Zense                         |                         Sungha Jung                          |               Sungha Jung Cover Compilation 5                |
|              情熱大陸2018 ~Full Orchestra Ver.               |                         Taro Hakase                          |                        ALL TIME BEST                         |
|                       Hot Air Balloon                        |                          Don Diablo                          |                       Hot Air Balloon                        |
|                  Time to Fly (Feerty Remix)                  |                            Astra                             |                  Time to Fly (The Remixes)                   |
|                           7 Years                            |                         Lukas Graham                         |                         Lukas Graham                         |
|                        Cheap Thrills                         |                             Sia                              |                        This Is Acting                        |
|                           煙袋斜街                           |                        接個吻，開一槍                        |                           煙袋斜街                           |
|                              不                              |                           痛仰樂隊                           |                              不                              |
|                            红蜻蜓                            |                             叶蓓                             |                        流浪途中爱上你                        |
|                          明天更漫長                          |                           Dou Wei                            |                             黑夢                             |
|                      Sign of the Times                       |                         Harry Styles                         |                      Sign of the Times                       |
|                      Lord of the Rings                       |                        The Piano Guys                        |                       The Piano Guys 2                       |
|                        Counting Stars                        |                         Simply Three                         |                        Counting Stars                        |
|                            Pepas                             |                           Farruko                            |                            Pepas                             |
|                           Señorita                           |                         Simply Three                         |                           Volume 5                           |
| He's a Pirate (From "Pirates of the Caribbean) - Folk Version |                         Taylor Davis                         | He's a Pirate (From "Pirates of the Caribbean) [Folk Version] |
|        Scheherazade: The Tale of the Kalendar Prince         |                   Nikolai Rimsky-Korsakov                    |                Rimsky-Korsakov: Scheherezade                 |
|               Blinding Lights - Medieval Style               |                        Cornelius Link                        |                       Blinding Lights                        |
|                 Wake Me Up - Medieval Style                  |                        Cornelius Link                        |                 Wake Me Up (Medieval Style)                  |
|                            老男孩                            |                           筷子兄弟                           |                             父親                             |
|                       起风了 ヤキモチ                        |                           Lennerd                            |                       起风了 ヤキモチ                        |
|                          otherside                           |                          Lena Raine                          |     Minecraft: Caves & Cliffs (Original Game Soundtrack)     |
|         Face My Fears - Kaleidoscope Orchestra Remix         |                    Kaleidoscope Orchestra                    |         Face My Fears (Kaleidoscope Orchestra Remix)         |
|                         The Spectre                          |                        David Starsky                         |           Piano and Violin Covers of Popular Songs           |
|                   Through the Woods We Ran                   |                          Vindsvept                           |                  Vindsvept Collection 2016                   |
|                  River Flows In You (Remix)                  |                           Olivund                            |                  River Flows In You (Remix)                  |
|                      Kids Return - Live                      |                         Joe Hisaishi                         |       Songs of Hope: The Essential Joe Hisaishi Vol. 2       |
|                            SEVEN                             |                         Nobuko Toda                          |            Ultraman (Original Series Soundtrack)             |
|                           ULTRAMAN                           |                         Nobuko Toda                          |   Ultraman (Music from the Netflix Original Anime Series)    |
|                           Believer                           |                            Atlys                             |                           Believer                           |
|                         The Spectre                          |                          Peter Buka                          |                         The Spectre                          |
|                      An Endless Desert                       |                          Todd Baker                          |          Alto's Odyssey (Original Game Soundtrack)           |
|                        Lose Somebody                         |                             Kygo                             |                        Lose Somebody                         |
|                     Skilled In The Arts                      |                          Yi Nantiro                          |                        A True Master                         |
|                      Meme Music Medley                       |                            Algal                             |                   This Is Bardcore (Vol.1)                   |
|                      Dragostea Din Tei                       |                            O-Zone                            |                          DiscO-Zone                          |
|                           不怕不怕                           |                          Jocie Guo                           |                           不怕不怕                           |
|           となりのトトロ - ぐっすり眠れる木琴 ver.           |                      Jukebox ☆☆☆ MAGIC                       |           となりのトトロ (ぐっすり眠れる木琴 ver.)           |
| Dumbo Theme Song (優しい木琴バージョン♪) [ディズニー『ダンボ』より] |                      Jukebox ☆☆☆ MAGIC                       | ベストヒット♪ ディズニー セレクション Vol.2 (優しい木琴 versions) |
|                Xylophone Beats - Original Mix                |                          Lov Smith                           |          Summer Splash - Music For Beach Chill Out           |
|                          Baby Steps                          |                         Rhythm Scott                         |                      Music for Mallets                       |
|                 Kaptein Sabeltann (Overture)                 |                     Jonas B. Ingebretsen                     |                     The Musical Journey                      |
| Under The Sea [From Disney "Little Mermaid"] - Nice & Smooth Marimba Version |                      Jukebox ☆☆☆ MAGIC                       | Best Hits Selection of Disney Song Vol.2 (Nice & Smooth Marimba Versions) |
|                         Viva La Vida                         |                           Coldplay                           |          Viva La Vida or Death and All His Friends           |
|                         SENBONZAKURA                         |                            Ayasa                             |                  ANISONG COVER NIGHT Vol.1                   |
|               In the Hall of the Mountain King               |                           Deficio                            |               In the Hall of the Mountain King               |
|                     Lacrimosa (8d Audio)                     |                           Deficio                            |                         Lacrimosa EP                         |
|                          My Own Way                          |                           8D Audio                           |                          My Own Way                          |
|               Sky (feat. Martell) - Radio Edit               |                           Steerner                           |               Sky (feat. Martell) [Radio Edit]               |
|                          Tokyo Rain                          |                        Marcus Warner                         |                          39 Seconds                          |
|                      Impossible Worlds                       |                          Todd Baker                          |         Monument Valley 2 (Original Game Soundtrack)         |
|                           Popcorn                            |                            Helion                            |                           Popcorn                            |
|                            Moskau                            |                           DOPEDROP                           |                            Moskau                            |
|                       Popcorn - Remix                        |                      Daniele Vitale Sax                      |                      Daniele Vitale Sax                      |
|                           Popcorn                            |                       Florence Nevada                        |                           Popcorn                            |
|                         Rebel Rouser                         |                          Duane Eddy                          |            Popcorn And Other Great Instrumentals             |
|                  River Flows In You - Remix                  |                      Daniele Vitale Sax                      |                  River Flows In You (Remix)                  |
|                            心要野                            |                          后海大鲨鱼                          |                            心要野                            |
|                            Rush E                            |                       Sheet Music Boss                       |                       Rush Collection                        |
|                       SWINGIN' VIVALDI                       |                              PD                              |    HATS MUSIC COLLECTION ~ Taro Hakase Collaborated Works    |
|                           Shivers                            |                          Ed Sheeran                          |                           Shivers                            |
|                        Call Me Maybe                         |                       Carly Rae Jepsen                       |                             Kiss                             |
|                           遠走高飛                           |                            金志文                            |                           Hello 1                            |
|                         España Cañi                          |                          Pasodobles                          |                          Pasodobles                          |
|                     Lunar Beasts - 2021                      |                      League of Legends                       |                     Lunar Beasts - 2021                      |
|                           I'm Blue                           |                             Alef                             |                           I'm Blue                           |
|                         Cats on Mars                         |                          SEATBELTS                           |                   COWBOY BEBOP Vitaminless                   |
|                          Juggernaut                          |                             Env                              |                          Juggernaut                          |
|                      Mexican Hat Dance                       |                  Mariachi Nuevo Tecalitlan                   |               16 de Septiembre (Con Mariachi)                |
|                       This Is Our Land                       |                          Epic Score                          |            Epic Action & Adventure Vol. 5 - ES012            |
|                       Blue - Da Ba Dee                       |                      Daniele Vitale Sax                      |                       Blue (Da Ba Dee)                       |
|                         Shalala Lala                         |                          Vengaboys                           |                         Shalala Lala                         |
|                         和煦的糖果风                         |                          Candy_Wind                          |                         和煦的糖果风                         |
|                          Despacito                           |                        Calvin Devito                         |                        Battle Pianos                         |
|                             奔跑                             |                           Yu Quan                            |                             拾伍                             |
|       Mario & Luigi Bowser's Inside Story - Final Boss       |                         Game & Sound                         |              "Game & Sound: VGM Covers, Vol. 3"              |
|                         Mr. Blue Sky                         |                   Electric Light Orchestra                   |                       Out of the Blue                        |
|                        幻昼 - 钢琴版                         |                            文武贝                            |                        幻昼 (钢琴版)                         |
|                 "Bubba, the Wandering Gypsy"                 |                         Buddy Greene                         |                     Harmonica Anthology                      |
|                         Stadium Rave                         |                    Spongebob Squarepants                     |                  SpongeBob's Greatest Hits                   |
|               Pumped Up Kicks - Medieval Style               |                        Cornelius Link                        |               Pumped Up Kicks (Medieval Style)               |
|                             Omen                             |                         Guilhem Desq                         |                           Visions                            |
|               Under Pressure - Remastered 2011               |                            Queen                             |            Hot Space (Deluxe Remastered Version)             |
|             Bohemian Rhapsody - Remastered 2011              |                            Queen                             |       A Night At The Opera (Deluxe Remastered Version)       |
|                       現在是什麼時辰了                       |                          Hebe Tien                           |                       現在是什麼時辰了                       |
|                    Walk Like an Egyptian                     |                         The Bangles                          |                       Different Light                        |
|                         How It Began                         |                              Na                              |                         Venice Beach                         |
|                             Rain                             |                         Steve Conte                          |      COWBOY BEBOP (Original Motion Picture Soundtrack)       |
|                       Live in Baghdad                        |                           遠藤正明                           | COWBOY BEBOP (Original Motion Picture Soundtrack 2 - No Disc) |
|                 Somebody That I Used To Know                 |                            Gotye                             |                        Making Mirrors                        |
|                        Hold The Line                         |                          后海大鲨鱼                          |          Look Directly Into The Sun: China Pop 2007          |
|                        Nuke the Moon                         |                        Epic Mountain                         |  "Kurzgesagt, Vol. 7 (Original Motion Picture Soundtrack)"   |
|               Penguin's Game - English Version               |                            Gelato                            |                "That's Bubble Dance, Vol. 2"                 |
|           Launchpad vs. Launchkey - Dubstep Remix            |                           Kaskobi                            |           Launchpad vs. Launchkey (Dubstep Remix)            |
|               Can't Hold Us (feat. Ray Dalton)               |                   Macklemore & Ryan Lewis                    |                          The Heist                           |
|                 Navigate The Seas Of The Sun                 |                       Bruce Dickinson                        |                       Tyranny Of Souls                       |
|                      Touhou Bad Apple!!                      |                   Stringanza Erhu Quartet                    |                      Touhou Bad Apple!!                      |
|                   Tom's Diner - 7" Version                   |                             DNA                              |          The Best Of Suzanne Vega - Tried And True           |
|                   Tom's Diner - 7" Version                   |                             DNA                              |           RetroSpective: The Best Of Suzanne Vega            |
|           時の中を走りぬけて/ウルトラマンUSA(8bit)           |                        Studio Megaane                        |                   ウルトラマン8bit vol.01                    |
|                           Positive                           |                       AShamaluevMusic                        |                        Positive Music                        |
|                     Spaceships for Earth                     |                      Everyday Astronaut                      |                 Maximum Aerodynamic Pressure                 |
|                   DEJA VU - Extended ver.                    |                         dave rodgers                         | SUPER EUROBEAT presents DAVE RODGERS Special COLLECTION (Vol.2) |
|                   Welcome to the Internet                    |                          Bo Burnham                          |                      Inside (The Songs)                      |
|                      Daybreak Confusion                      |                            Prism                             |                          blue・・・                          |
|                           Whistle                            |                           Flo Rida                           |                          Wild Ones                           |
|  "Piano Concerto No.1 In E Minor, Op.11: 3. Rondo (Vivace)"  |                       Frédéric Chopin                        |              Chopin: Piano Concertos Nos.1 & 2               |
|                   Humoresque - Radio Edit                    |                        Scott Hamilton                        |                          Humoresque                          |
|                 maybe as his skies are wide                  |                         Brad Mehldau                         |                        Jacob's Ladder                        |
|                            River                             |                         Tom Gregory                          |                            River                             |
|                          Heartbeat                           |                           Xillions                           |                          Heartbeat                           |
|                              愛                              |                            小虎隊                            |                              愛                              |
|                        Gurdy's Green                         |                         Patty Gurdy                          |                      Shapes & Patterns                       |
|              Main Theme (From "Twisted Nerve")               |          The City of Prague Philharmonic Orchestra           |                   100 Greatest Film Themes                   |
|              Crazy La Paint (Ultimate Edition)               |                         Minimusicman                         |              Crazy La Paint (Ultimate Edition)               |
|                        Counting Stars                        |                    Piano Tribute Players                     |                      Dinner Party Piano                      |
|                            Summer                            |                         Joe Hisaishi                         |                       メロディフォニー                       |
|                            Summer                            |                         Joe Hisaishi                         |          菊次郎の夏 (オリジナル・サウンドトラック)           |
|                         Viva la Vida                         |                         Louie Ashley                         |                 "The Epic Orchestra, Vol. 1"                 |
|                          森林狂想曲                          |                       Wu Judy Chin-tai                       |                          森林狂想曲                          |
|      Lightning Flame Dragon Roaring - From "Fairy Tail"      |                           Melôdyne                           |      Lightning Flame Dragon Roaring (From "Fairy Tail")      |
|                           雪の進軍                           |                        あんこうチーム                        | TVアニメ『ガールズ&パンツァー』ファンディスクCD 「ディープパンツァーCDです!」 |
|            First Level (From "Adventure Island")             |                           Melôdyne                           |            First Level (From "Adventure Island")             |
|                          Levitation                          |                            Mabeha                            |                          Levitation                          |
|                     Live Is Life - Live                      |                             Opus                             |               Die Grössten Hits Aus 15 Jahren                |
|                     Souvenirs D' Enfance                     |                             佚名                             |                          想戀甜檸檬                          |
|                       Marriage D'amour                       |                         Maan Hamadeh                         |                          Inception                           |
|                      River Flows In You                      |                            Yiruma                            | Yiruma 2nd Album 'First Love' (The Original & the Very First Recording) |
|         Take Me to Church - Acoustic Guitar Version          |                      Unplugged Machine                       |           "Pop Goes Acoustic Guitar 2014, Vol. 2"            |
|                     不会成真的梦 - Live                      |                            何亮辰                            |                声入人心·第二季 (第一期 Live)                 |
|                       Slumbering Weald                       |                          TeraCMusic                          |                       Slumbering Weald                       |
|                      The Latin Quarter                       |                        Satoshi Takebe                        |               From Up On Poppy Hill Soundtrack               |
|         "Beethoven: Piano Trio No. 7 in B-Flat Major         |                            Op. 97                            |             ""Archduke"": II. Scherzo. Allegro"              |
|            "Sonata For Violin And Piano No.5 In F            |               Op.24 - ""Spring"": 1. Allegro"                |                     Ludwig van Beethoven                     |
|                          Legendary                           |                           MyoMouse                           |                          Legendary                           |
|                          China-Rain                          |                             YUAN                             |                         China Series                         |
|                   Flight Of The Silverbird                   |               Massed Bands of HM Royal Marines               |              Mountbatten Festival of Music 2017              |
| My Best Friends in the World (What Am I to You?) [From "Adventure Time"] |                         Phil Larson                          | My Best Friends in the World (What Am I to You?) [From "Adventure Time"] |
|                          Shackleton                          |                          Adam Young                          |                        The Endurance                         |
|                        Anyone Got Mic                        |                      Lofi Fruits Music                       |                         3 AM. Gaming                         |
|                          Wake Me Up                          |                       Sébastien Hogge                        |                        Guitar Covers                         |
|                         Tarrey Town                          |                          Juke Remix                          |         "Relaxing and Beautiful Zelda Music, Vol. 1"         |
|               In the Hall of the Mountain King               |               In The Hall Of The Mountain King               |               In the Hall of the Mountain King               |
|                   "Einzug der Gladiatoren                    |                  Op. 68 ""Triumph March"""                   |                         Julius Fučík                         |
|                   SAXOSUELTA - Sax Version                   |                      Daniele Vitale Sax                      |                      Daniele Vitale Sax                      |
|                          Let Her Go                          |                          Passenger                           |            All the Little Lights (Deluxe Version)            |
|                           Bus Stop                           |                        Infinity Train                        |         Infinity Train: Book 1 (Original Soundtrack)         |
|                      Popcorn (8D Audio)                      |                           8D Tunes                           |                      Popcorn (8D Audio)                      |
|                    多瑙河之波 - 口哨吹奏                     |                            李迩泰                            |                    百年经典-口哨吹奏(一)                     |
|                     斯卡布罗 - 口哨吹奏                      |                            李迩泰                            |                    百年经典-口哨吹奏(一)                     |
|                    匈牙利舞曲 - 口哨吹奏                     |                            李迩泰                            |                    百年经典-口哨吹奏(四)                     |
|                       Moonlight Shadow                       |                        Mike Oldfield                         |                 The Mike Oldfield Collection                 |
|                      Green Green Grass                       |                         George Ezra                          |                        Gold Rush Kid                         |
|                     Rolling in the Deep                      |                           92 Keys                            |                        Spring of Fire                        |
|                           CHINA-2                            |                             Sand                             |                      CHINA(中国风电音)                       |
|                         Soviet March                         |                          Megaraptor                          |                         Soviet March                         |
|                        火ノ鳥のように                        |                             doa                              |                            open_d                            |
|                  Journey of a Soul Symphony                  |                           Valkyra                            |                  Journey of a Soul Symphony                  |
|                            Sugar                             |                           92 Keys                            |                           92 Keys                            |
| "Offenbach: Die schöne Helena (Gesamt) 1. Akt (1994 Digital Remaster): Nr. 7b: Ich bin Ajax, Held im Kriege" |                      Jacques Offenbach                       |          Best Of Offenbach [International Version]           |
|     "Tchaikovsky: 1812 Overture in E-Flat Major, Op. 49"     |                   Pyotr Ilyich Tchaikovsky                   |         Tchaikovsky : Symphony No.5 & 1812 Overture          |
| Orphée aux enfers: Overture (Arr. C. Binder & J.G. Busch for Orchestra) |                      Jacques Offenbach                       |                     Offenbach: Overtures                     |
|                            Africa                            |                         Simply Three                         |                           Volume 5                           |
|             A Thousand Miles - Piano Arrangement             |                        Niko Kotoulas                         |                     Piano Covers Vol. 1                      |
|          DETECTIVE CONAN MAIN THEME DEEP AZURE ver.          |                         Katsuo Ohno                          |    「名探偵コナン 紺碧の棺」オリジナル・サウンドトラック     |
|                     Stay - Instrumental                      |                             INST                             |                     Stay (Instrumental)                      |
|          The Curse of Monkey Island & Grim Fandango          |                       Legacy Sessions                        |                      GAME Generation 5                       |
|                            來不及                            |                            Pu Shu                            |                           生如夏花                           |
|                        想把我唱給你聽                        |                           Lao Lang                           |                          北京的冬天                          |
|                       Top Of The World                       |                          Carpenters                          |                        A Song For You                        |
|                       Cheri Cheri Lady                       |                        Modern Talking                        |     The First & Second Album (30th Anniversary Edition)      |
|                          LEMON TREE                          |                            蘇慧倫                            |                          LEMON TREE                          |
|                           Vincent                            |                          Don McLean                          |                         American Pie                         |
|                           Victory                            |                     Two Steps from Hell                      |                          Battlecry                           |
|                   It Is You (I Have Loved)                   |                         Dana Glover                          |                            Shrek                             |
|                       A Thousand Years                       |                       Christina Perri                        |                       Autumn Acoustic                        |
|                         I Got A Name                         |                          Jim Croce                           |                         I Got A Name                         |
|                      A Man Without Love                      |                    Engelbert Humperdinck                     |                      A Man Without Love                      |
|                (They Long To Be) Close To You                |                          Carpenters                          |                         Close To You                         |
|      Brinstar - The Jungle Floor (From "Super Metroid")      |                          Ludopatas                           |              La Leyenda de las Siete Estrellas               |
|                       Oriental Breeze                        |                          Collioure                           | "Chill in Paradise, Vol. 11 - 25 Lounge & Chill-Out Tracks"  |
|                      Ain't No Sunshine                       |                         Boney James                          |                          Seduction                           |
|                        Brother Louie                         |                        Modern Talking                        |                        Back for Gold                         |
|                            とんぼ                            |                      Tsuyoshi Nagabuchi                      |                        長渕剛 LIVE'89                        |
|                          Lemon Tree                          |                         Fools Garden                         |                       Dish Of The Day                        |
|                      刀剑如梦 - Live版                       |                          Wakin Chau                          |                      周华健 侠客行·专场                      |
|                     Yesterday Once More                      |                          Carpenters                          |                     Now & Then (Reissue)                     |
|                       秋去秋來 - Live                        |                          Sally Yeh                           |                   葉蒨文完全是你演唱會2012                   |
|                Before the Next Teardrop Falls                |                        Freddy Fender                         |                 The Freddy Fender Collection                 |
|                    The Girl From Ipanema                     |                        Vince Guaraldi                        |                     Essential Standards                      |
|                      Going Home - Edit                       |                           Kenny G                            |                        Greatest Hits                         |
|                       Uncle Al - Live                        |                           Kenny G                            |                         Kenny G Live                         |
|         Let It Go - From "Frozen"/Soundtrack Version         |                         Idina Menzel                         | Frozen (Original Motion Picture Soundtrack / Deluxe Edition) |
|                            Tikal                             |                        E.S. Posthumus                        |                          Unearthed                           |
|                       A Hero Will Rise                       |                      Future World Music                      |                       A Hero Will Rise                       |
|                       Close Your Eyes                        |                        Bernward Koch                         |                    Walking through Clouds                    |
|                             歡沁                             |                           Lin Hai                            | 慶新年添好運!必聽新世紀中國風賀歲組曲 – 春節氣氛營造 純音樂  |
|                       Johnny B. Goode                        |                         Chuck Berry                          |                       Berry Is On Top                        |
|                 Auf und auf voll lebenslust                  |                         Franzl Lang                          |                 Auf und auf voll lebenslust                  |
|                          Magic Fly                           |                            Space                             |                          Magic Fly                           |
|                          Just Blue                           |                            Space                             |                          Just Blue                           |
|                   Graze the Roof (In-Game)                   |                       Laura Shigihara                        |     Plants Vs. Zombies (Original Video Game Soundtrack)      |
|                   Crazy Dave (Intro Theme)                   |                       Laura Shigihara                        |     Plants Vs. Zombies (Original Video Game Soundtrack)      |
|                       Brainiac Maniac                        |                       Laura Shigihara                        |     Plants Vs. Zombies (Original Video Game Soundtrack)      |
|                   Star Sky - Instrumental                    |                     Two Steps from Hell                      |                          Battlecry                           |
|                 Thank God I'm a Country Boy                  |                     Hampton The Hampster                     |                  Hampster Dance - The Album                  |
|                    The HampsterDance Song                    |                     Hampton The Hampster                     |                  Hampster Dance - The Album                  |
|                         Cantina Band                         |                        John Williams                         |  Star Wars: A New Hope (Original Motion Picture Soundtrack)  |
|                    Uraniwa Ni Zombies Ga!                    |                       Laura Shigihara                        |     Plants Vs. Zombies (Original Video Game Soundtrack)      |
| "Peer Gynt Suite No. 1, Op. 46: IV. In the Hall of the Mountain King" |                         Edvard Grieg                         |          The 50 Greatest Pieces of Classical Music           |
|                     Who Let The Dogs Out                     |                           Baha Men                           |                     Who Let The Dogs Out                     |
|                       The Party Troll                        |                         D1ofAquavibe                         |                       The Party Troll                        |
|                      U Can't Touch This                      |                          MC Hammer                           |                 Please Hammer Don't Hurt 'Em                 |
|             She Is My Sin - Live at Wacken 2013              |                          Nightwish                           |                 "Showtime, Storytime (Live)"                 |
|                        Where Are You                         |                         Don Williams                         |                    You're My Best Friend                     |
|                            江湖笑                            |                          Wakin Chau                          |                             雨人                             |
|                          其實不想走                          |                          Wakin Chau                          |                 滾石香港黃金十年-周華健精選                  |
|                           戀曲1990                           |                            羅大佑                            |                           愛人同志                           |
|                      Last Of The Wilds                       |                          Nightwish                           |                      Dark Passion Play                       |
|                         逆战 - Live                          |                         Jason Zhang                          |                乘风破浪的姐姐 (成团之夜 Live)                |
|                            我相信                            |                            楊培安                            |                        午夜兩點半的我                        |
|                          漫步人生路                          |                         Teresa Teng                          |                      鄧麗君-傳奇的誕生                       |
|               Stronger (What Doesn't Kill You)               |                        Kelly Clarkson                        |                  Stronger (Deluxe Version)                   |
|                         Fundamentum                          |                            Lesiem                            |                     Mystic Spirit Voices                     |
|                            丁香花                            |                             唐磊                             |                            丁香花                            |
|                  If I Fail - Symphonic Live                  |                          Mono Inc.                           |                  If I Fail (Symphonic Live)                  |
|                      おどるポンポコリン                      |                        GOLDEN BOMBER                         |                      おどるポンポコリン                      |
|                           Frisbee                            |                           Ahxello                            |                           Frisbee                            |
|                        He's a Pirate                         |                         Klaus Badelt                         | Pirates of the Caribbean: The Curse of the Black Pearl (Original Motion Picture Soundtrack) |
|                    Csardas - Gypsy Dance                     |                        David Garrett                         |                           Virtuoso                           |
|                        He's A Pirate                         |                        David Garrett                         |          Unlimited - Greatest Hits (Deluxe Version)          |
|                        Spontaneous Me                        |                       Lindsey Stirling                       |                       Lindsey Stirling                       |
|                       We Will Rock You                       |                        David Garrett                         |                            Music                             |
| "Rock Around The Clock / See You Later, Alligator / Hound Dog - Medley" |                          James Last                          |                     Rock Around With Me!                     |
|                    William Tell: Overture                    |                      Gioachino Rossini                       |                       Viral Classical                        |
|                            Scabs                             |                        Bryson Andres                         |                    "Time Machine, Pt. 1"                     |
|                         Contradanza                          |                          Mike Batt                           |                   The Best Of Vanessa-Mae                    |
|                              画                              |                           Zhao Lei                           |                            赵小雷                            |
|                           WolfRed                            |                           Jelonek                            |                           Revenge                            |
|              The River Kwai March - Remastered               |                         Mitch Miller                         | The River Kwai March & The Yellow Rose of Texas (Remastered) |
|                           The Mass                           |                             ERA                              |                           The Mass                           |
|                             醉拳                             |                         Jackie Chan                          |                    成龍超級精裝大戲主題曲                    |
|                         Mr. Blue Sky                         |                   Electric Light Orchestra                   |                       Out of the Blue                        |
|                           天煞孤星                           |                          Ekin Cheng                          |                       Friends For Life                       |
|                       It's Raining Men                       |                        Geri Halliwell                        |                Scream If You Wanna Go Faster                 |
|                        Discombobulate                        |                         Hans Zimmer                          |     Sherlock Holmes (Original Motion Picture Soundtrack)     |
|            壯誌在我胸2020 (電影《急先鋒》主題曲)             |                         Jackie Chan                          |            壮志在我胸2020 (电影《急先锋》主题曲)             |
|                           星星點燈                           |                            鄭智化                            |                           星星點燈                           |
|                           平凡之路                           |                            Pu Shu                            |                     朴树 猎户星座 · 专场                     |
|                  Let The Music Take Control                  |                             W&W                              |                  Let The Music Take Control                  |
|                   Popcorn - GATTÜSO Remix                    |                          Steve Aoki                          |                   Popcorn (GATTÜSO Remix)                    |
|                           Memories                           |                           Maroon 5                           |                           Memories                           |
|                          追梦赤子心                          |                             GALA                             |                          追梦痴子心                          |
|                      Only For A Moment                       |                          Lola Marsh                          |                      Only For A Moment                       |
|                         Dance Monkey                         |                         Tones And I                          |         Dance Monkey (Stripped Back) / Dance Monkey          |
|                          Love Story                          |                         Taylor Swift                         |                           Fearless                           |
|                          Hot N Cold                          |                          Katy Perry                          |                       One Of The Boys                        |
|                      Pretty White Lies                       |                         Jason Zhang                          |                         FUTURE·LIVE                          |
|                        Make You Mine                         |                            PUBLIC                            |                        Make You Mine                         |
|                    Mood (feat. iann dior)                    |                           24kGoldn                           |                    Mood (feat. iann dior)                    |
|                         Breaking Me                          |                            Topic                             |                         Breaking Me                          |
|                             Salt                             |                           Ava Max                            |                             Salt                             |
|                            鐘鼓樓                            |                             何勇                             |                            垃圾場                            |
|                        She Is My Sin                         |                          Nightwish                           |                          Wishmaster                          |
|                       Nausicaä Requiem                       |                         Joe Hisaishi                         | Nausicaä of the Valley of the Wind Soundtrack: Towards the Faraway Land |
|                         野子 - Live                          |                             Sue                              |               第二季中國好歌曲導師原創: 心宇宙               |
|                             成都                             |                           Zhao Lei                           |                           無法長大                           |
|                         M O N I C A                          |                        Leslie Cheung                         |                            Leslie                            |
|                             YES                              |                          BEN & TAN                           |                             YES                              |
|                            Brave                             |                          Hanna Ferm                          |                            Brave                             |
|                           Sunshine                           |                        Lance & Linton                        |                           Sunshine                           |
|                  風になる(Acoustic Version)                  |                         Tsuji Ayano                          |                          恋する眼鏡                          |
|                      Good Enough (Live)                      |                      Annaleigh Ashford                       |             Lost in the Stars: Live at 54 Below              |
|  Rocket to the Moon (From the Netflix Film "Over the Moon")  |                          Cathy Ang                           |  Rocket to the Moon (From the Netflix Film "Over the Moon")  |
|                            Faith                             |                        Calvin Harris                         |                            Motion                            |
|                          "Honey, I"                          |                          Wes Reeve                           |                          "Honey, I"                          |
|                           平凡之路                           |                            Pu Shu                            |                     朴树 猎户星座 · 专场                     |
|     夜空中最亮的星 (The Brightest Star in the Night Sky)     |                         Calculasian                          |                      待整理 To Be Done                       |
|                            Leyla                             |                            Mesto                             |                            Leyla                             |
|                             Baby                             |                        Justin Bieber                         |                         My World 2.0                         |
|                   Butterfly (Anniversary)                    |                           SMiLE.dk                           |                   Butterfly (Anniversary)                    |
|                             荒島                             |                            謝春花                            |                            算雲煙                            |
|                         Bad Romance                          |                          Lady Gaga                           |                         Bad Romance                          |
|                         Viva La Vida                         |                           Coldplay                           |          Viva La Vida or Death and All His Friends           |
|                        小さな恋のうた                        |                          MONGOL800                           |                           MESSAGE                            |
|                      Island in the Sun                       |                       GAMPER & DADONI                        |                      Island in the Sun                       |
|                 Delacey - Dream It Possible                  |                       Sufian Bouhrara                        |                 Delacey - Dream It Possible                  |
|                      Dream It Possible                       |                       The Brick Slayer                       |                      Dream It Possible                       |
|                          淋雨一直走                          |                         Angela Chang                         |                          有形的翅膀                          |
|                           Lifeline                           |                           Zeraphym                           |                           Lifeline                           |
|                        Stick Together                        |                           Elijah N                           |                       Forgetting This                        |
|                           All Star                           |                          Mike Perry                          |                           All Star                           |
|                        Someone To You                        |                           BANNERS                            |                    Where The Shadow Ends                     |
|                          明天會更好                          |                          Tsai Chin                           |                          明天會更好                          |
|                        Indian Summer                         |                        Stereophonics                         |                    Graffiti on The Train                     |
|                           Crystals                           |                           Steerner                           |                            Sun EP                            |
|                      驕傲的少年 - Live                       |                           南征北戰                           |                 第三季中國好歌曲導師: 陶喆組                 |
|                            熱血燃                            |                          Wowkie Da                           |                           人間精品                           |
|                            B.East                            |                           Jelonek                            |                           Jelonek                            |
|                           bad guy                            |                        Billie Eilish                         |          "WHEN WE ALL FALL ASLEEP, WHERE DO WE GO?"          |
|                      Cockroaches Empire                      |                           Jelonek                            |                           Revenge                            |
|                          MachineHat                          |                           Jelonek                            |                           Jelonek                            |
|                             Baby                             |                        Justin Bieber                         |                     Birthday party 2020                      |
|                           Matsuri                            |                            Kitaro                            |                            Kojiki                            |
|                     Yesterday Once More                      |                          Carpenters                          |                     Now & Then (Reissue)                     |
|                        There for You                         |                        Martin Garrix                         |                        There for You                         |
|              Magic Night In The Slaughterhouse               |                           Jelonek                            |                           Revenge                            |
|                           Oneself                            |                        Jincheng Zhang                        |                            Absorb                            |
|   Ma Ya Hi (Dragostea Din Tei) - Original Romanian Version   |                            O-Zone                            |         Ma Ya Hi (Dragostea Din Tei) [English Mixes]         |
|                (They Long To Be) Close To You                |                          Carpenters                          |                         Close To You                         |
|                      Glitz and Glamour                       |                        Jason Farnham                         |             "Pop City Electronic Music, Vol. 3"              |
|                     No Fear In My Heart                      |                             朴树                             |                           猎户星座                           |
|                   Car Wash - Long Version                    |                          Rose Royce                          |                           Car Wash                           |
|                        小さな恋のうた                        |                          MONGOL800                           |                           MESSAGE                            |
|                         Like A Boss                          |                             Kura                             |                         Like A Boss                          |
|               Sky (feat. Martell) - Radio Edit               |                           Steerner                           |               Sky (feat. Martell) [Radio Edit]               |
|                        HAPPY BIRTHDAY                        |                          MONGOL800                           |                       GO ON AS YOU ARE                       |
|          We Gave up Too Soon (feat. Vanessa Jamie)           |                         Speedometer                          |                     Our Kind of Movement                     |
|                        陽光總在風雨後                        |                          Mavis Hee                           |                          都是夜歸人                          |
|                     Friends - Radio Edit                     |                           Steerner                           |                     Friends (Radio Edit)                     |
|     "Main Title / [Ghidorah, The Three-Headed Monster]"      |                        Akira Ifukube                         |      Shin Godzilla (Original Motion Picture Soundtrack)      |
|        贝多芬第五小提琴奏鸣曲“春天” : 第四乐章 - Live        |                     Ludwig van Beethoven                     |                       一半天平一半巨蟹                       |
|                            黃種人                            |                         Nicholas Tse                         |                    黃 ‧ 鋒 (新曲 + 精選)                     |
|                       Butterfly Effect                       |                      Christian Telford                       |              Inspirations (Original Soundtrack)              |
|                           雾里看花                           |                             那英                             |                    "名人名歌荟萃, Vol. 5"                    |
|                     DON'T WORRY BE HAPPY                     |                          MONGOL800                           |                       GO ON AS YOU ARE                       |
|                            Alive                             |                           Steerner                           |                            Alive                             |
|                             July                             |                          Noah Cyrus                          |                    THE END OF EVERYTHING                     |
|                       Four Wild Horses                       |                         David Munyon                         |                          Live 2014                           |
|                           WolfRed                            |                           Jelonek                            |                           Revenge                            |
|                          HAPPY LIFE                          |                          MONGOL800                           |                       GO ON AS YOU ARE                       |
|                           花好月圆                           |                             刁寒                             |                            爱情装                            |
|                          長路有多遠                          |                            蔣志光                            |                          皇后大道東                          |
|                      Life - Radio Edit                       |                           Steerner                           |                      Life (Radio Edit)                       |
|                       Close Your Eyes                        |                        Bernward Koch                         |                    Walking through Clouds                    |
|                           Popcorn                            |                        Edward Simoni                         |                 Die Zauberwelt der Panflöte                  |
|                          平凡的一天                          |                           Mao Buyi                           |                          平凡的一天                          |
|              A Funeral Of A Provincial Vampire               |                           Jelonek                            |                           Jelonek                            |
|             Jambalaya (on the Bayou) - Live 1974             |                          Carpenters                          |              The Road to Yesterday (Live 1974)               |
|                         野子 - Live                          |                             Sue                              |               第二季中國好歌曲導師原創: 心宇宙               |
|                        You're My Star                        |                        Stereophonics                         |  Decade In The Sun - Best of Stereophonics (Deluxe Version)  |
|                             CRY                              |                  SawanoHiroyuki[nZk]:mizuki                  |                             CRY                              |
|                       A Hero's Return                        |                      Christopher Drake                       | Superman Batman: Public Enemies (Soundtrack From The DC Universe Animated Original Movie) |
|                    I Walk A Little Faster                    |                        BLOSSOM DEARIE                        |                       Whisper For You                        |
|                           New Soul                           |                          Yael Naim                           |                          Yael Naïm                           |
|                          Koko Soko                           |                           SMiLE.dk                           |                    Party Around The World                    |
|                      Concerning Hobbits                      |                         Howard Shore                         | The Lord of the Rings: The Fellowship of the Ring (Original Motion Picture Soundtrack) |
|      Love Story - Live From Clear Channel Stripped 2008      |                         Taylor Swift                         |                      Big Machine Live!                       |
|                        Sorry Suzanne                         |                         The Hollies                          |                       20 Golden Greats                       |
|                     Across the Universe                      |                     Across The Universe                      |                      Boom Hits (Vol. 2)                      |
|                       We Are The World                       |                      U.S.A. For Africa                       |                       We Are The World                       |
|                   Something Just Like This                   |                       The Chainsmokers                       |                   Something Just Like This                   |

{% endfolding %}

{% folding red, 网易云Alpyer测试歌单 %}

{% meting "7304688535" "netease" "playlist" "order:random" "listmaxheight:340px" "preload:none" "theme:#ad7a86"%}


{% meting "7304737427" "netease" "playlist" "order:random" "listmaxheight:340px" "preload:none" "theme:#ad7a86"%}

{% endfolding %}


[^1]: 现在看看，这似乎就是资本家的“奶头乐”，让用户觉得被关注，被重视，以回避更深层次的矛盾。