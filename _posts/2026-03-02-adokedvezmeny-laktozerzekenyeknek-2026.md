---
layout: post
title: "Adókedvezmény 2026-ban: Így igényeld vissza"
date: 2026-03-02 10:00:00 +0100
categories: tudnivalok penzugyek laktozmentes
image: /assets/images/1-adokedvezmeny-2026.png
---

Magyarországon a laktózintolerancia súlyos fogyatékosságnak minősülő betegségként van nyilvántartva. Ez azzal jár együtt, hogy jogosultak vagyunk adókedvezmény igénybevételére, ami a mindenkori minimálbér 5%-a havonta. 2026-ban ez az összeg már jelentős segítséget jelent a diéta fenntartásához.


## Mennyi az annyi 2026-ban?
2026 januártól a minimálbér bruttó összege **322 800 forintra** emelkedik.  
Ez összegszerűsítve: 322 800 * 0,05 = **16 140 Ft**.
Tehát **havonta 16 140 forint**, éves szinten pedig **193 680 forintnyi** adókedvezményben részesülhetünk. Ne hagyjátok az államnál, nálatok sokkal jobb helyen van!

<div class="my-12 p-8 bg-white rounded-[2.5rem] border border-blue-50 shadow-xl shadow-blue-900/5">
    <h4 class="text-center text-slate-900 font-black mb-8 tracking-tight">Éves adókedvezmény mértéke (2010-2026)</h4>
    <div class="relative h-[350px]">
        <canvas id="taxChart"></canvas>
    </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
document.addEventListener('DOMContentLoaded', function() {
    const ctx = document.getElementById('taxChart').getContext('2d');
    new Chart(ctx, {
        type: 'bar',
        data: {
            labels: ['2010','2011','2012','2013','2014','2015','2016','2017','2018','2019','2020','2021','2022', '2023', '2024', '2025', '2026*'],
            datasets: [{
                label: 'Éves összeg (Ft)',
                data: [44100, 46800, 55800, 58800, 60900, 63000, 66600, 76500, 82800, 89400, 96600, 100440, 120000, 139200, 160080, 174480, 193680],
                backgroundColor: '#3b82f6',
                hoverBackgroundColor: '#2563eb',
                borderRadius: 8,
                borderSkipped: false
            }]
        },
        options: {
            maintainAspectRatio: false,
            plugins: { legend: { display: false } },
            scales: {
                y: {
                    beginAtZero: true,
                    grid: { color: '#f1f5f9' },
                    ticks: { callback: value => value.toLocaleString() + ' Ft' }
                }
            }
        }
    });
});
</script>


## Hogyan tudod te is érvényesíteni az adókedvezményt?
1. **A vizsgálat:** Gasztroenterológiai vizsgálaton, terheléses **H2 kilégzéses teszten** kell kimutatni a laktózérzékenységet. Fontos tudni, hogy a genetikai tesztet egyre kevesebb szak- és háziorvos fogadja el, így érdemes egyből a kilégzéses tesztet választani.
2. **Az igazolás:** A gasztroenterológustól vagy a háziorvostól kell kérned az *"összevont adóalap adóját csökkentő kedvezmény igénybevételére jogosító igazolást"*. 
    * **Tipp:** Figyelj rá, hogy ha az állapotod maradandó, a *"végleges"* minősítés legyen aláhúzva, különben pár évente újra kell járnod a papír után.
3. **Dátumozás:** A kedvezmény az orvosi igazoláson szereplő szakorvosi dokumentáció dátumától (gyakorlatilag a teszt napjától) jár.


## Hol kell leadni?
Két lehetőséged van:
* **HR osztály:** Leadod a munkahelyeden az igazolást, így havonta több lesz a nettó fizetésed.
* **Adóbevallás:** Májusban az adóbevallásodban te magad igényled vissza egyben az egész éves összeget.

## Betegségek, amik után jár a kedvezmény
A pontos listát a [335/2009. (XII. 29.) Korm. rendeletben](https://net.jogtar.hu/jogszabaly?docid=A0900335.KOR) találjátok. A leggyakoribbak:
* **Laktózérzékenység:** E73-mal kezdődő kódok (E730, E731, E738, E739)
* **Fruktóz anyagcsere zavar:** E741.
* **Gluténérzékenység (Coeliakia):** K900.
* Sajnos a tejfehérje allergia jelenleg nem szerepel a kedvezményre jogosító listán.*


## Speciális esetek
* **Nyugdíjasok:** Csak akkor vehetik igénybe, ha a nyugdíj mellett van bejelentett, adózó jövedelmük.
* **KATA vállalkozók:** Mivel a KATA nem képez összevont adóalapot, ők sajnos nem tudnak élni ezzel a lehetőséggel.


A laktózmentes ételek többe kerülnek az átlagosnál, így minden extra bevétel jól jön. Intézzétek el a papírokat, mert ez a pénz jár nektek!



