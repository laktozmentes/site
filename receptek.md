---
layout: default
title: "Receptek"
---

<section class="py-16 border-b border-slate-100 mb-16 bg-gradient-to-b from-blue-50/50 to-transparent rounded-[3rem]">
    <div class="max-w-3xl mx-auto text-center px-6">
        <span class="text-blue-500 font-bold text-xs uppercase tracking-[0.3em] mb-4 block">Gasztronómia</span>
        <h1 class="text-4xl md:text-5xl font-extrabold text-slate-900 mb-6 tracking-tight">Receptek <span class="text-blue-500 italic font-serif text-3xl md:text-4xl ml-2">& Finomságok</span></h1>
        <p class="text-lg text-slate-500 font-light leading-relaxed">
            Válogatott, tesztelt és 100% laktózmentes receptek a mindennapokra. Mert a diéta nem az élvezetekről való lemondást jelenti.
        </p>
    </div>
</section>

<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
    {% for recipe in site.recipes %}
    <article class="group bg-white rounded-[2rem] border border-slate-100 shadow-sm hover:shadow-2xl hover:shadow-blue-900/5 transition-all duration-500 overflow-hidden flex flex-col">  
        <div class="aspect-[4/3] overflow-hidden relative">
            {% if recipe.image %}
                <img src="{{ recipe.image | relative_url }}" alt="{{ recipe.title }}" class="w-full h-full object-cover group-hover:scale-110 transition duration-700">
            {% else %}
                <div class="w-full h-full bg-gradient-to-br from-blue-50 to-blue-100 flex items-center justify-center">
                    <span class="text-blue-200 font-black text-6xl italic group-hover:scale-110 transition duration-500">R</span>
                </div>
            {% endif %}  
            <div class="absolute top-4 right-4 bg-white/90 backdrop-blur-sm px-3 py-1 rounded-full text-[10px] font-black uppercase tracking-widest text-blue-600 shadow-sm">
                Laktózmentes
            </div>
        </div>
        <div class="p-8 flex flex-grow flex-col">
            <div class="flex items-center space-x-2 text-[10px] font-bold text-slate-400 uppercase tracking-widest mb-3">
                <span>{{ recipe.prep_time | default: "Pár perc" }}</span>
                <span class="w-1 h-1 bg-slate-200 rounded-full"></span>
                <span>Egyszerű</span>
            </div>            
            <h2 class="text-xl font-bold text-slate-900 mb-4 group-hover:text-blue-600 transition leading-tight tracking-tight">
                <a href="{{ recipe.url | relative_url }}">{{ recipe.title }}</a>
            </h2>            
            <div class="mt-auto pt-6 border-t border-slate-50 flex justify-between items-center">
                <a href="{{ recipe.url | relative_url }}" class="text-xs font-black uppercase tracking-widest text-blue-500 hover:text-slate-900 transition">
                    Recept megnyitása &rarr;
                </a>
                <button class="text-slate-300 hover:text-blue-400 transition">
                    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path></svg>
                </button>
            </div>
        </div>
    </article>
    {% endfor %}
</div>

{% if site.recipes.size == 0 %}
<div class="text-center py-20 bg-white rounded-[2rem] border-2 border-dashed border-slate-100">
    <p class="text-slate-400 italic font-serif">Hamarosan érkeznek az első finomságok...</p>
</div>
{% endif %}
