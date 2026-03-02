---
layout: default
title: "Receptek"
---

<div class="max-w-7xl mx-auto py-20 px-6">
    <div class="text-center mb-20">
        <h1 class="text-5xl md:text-7xl font-[900] text-slate-900 leading-tight tracking-tighter mb-6 font-sans">
            Mentes <span class="text-blue-500">Finomságok</span>
        </h1>
        <p class="text-xl text-slate-500 max-w-2xl mx-auto leading-relaxed">
            Válogass kedvenc laktózmentes receptjeim közül. Egyszerűen elkészíthető, kipróbált ételek a mindennapokra.
        </p>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
        {% for recipe in site.recipes %}
        <article class="group bg-white rounded-[2.5rem] overflow-hidden border border-slate-50 shadow-sm hover:shadow-2xl hover:shadow-blue-900/10 transition-all duration-500 flex flex-col h-full">          
            <div class="aspect-[4/3] overflow-hidden relative">
                {% if recipe.image %}
                    <img src="{{ recipe.image | relative_url }}" alt="{{ recipe.title }}" class="w-full h-full object-cover group-hover:scale-110 transition duration-700">
                {% else %}
                    <div class="w-full h-full bg-blue-50 flex items-center justify-center">
                        <span class="text-blue-200 font-black text-6xl font-sans text-white">R</span>
                    </div>
                {% endif %}                
                <div class="absolute top-6 left-6">
                    <span class="bg-white/90 backdrop-blur-md text-blue-600 px-4 py-1 rounded-full text-[10px] font-black uppercase tracking-widest shadow-sm">
                        Laktózmentes
                    </span>
                </div>
            </div>
            <div class="p-8 flex flex-col flex-grow">
                <h3 class="text-2xl font-black text-slate-900 mb-4 group-hover:text-blue-600 transition tracking-tight leading-tight font-sans">
                    <a href="{{ recipe.url | relative_url }}">{{ recipe.title }}</a>
                </h3>               
                <p class="text-slate-500 leading-relaxed mb-8 line-clamp-3 text-sm flex-grow">
                    {{ recipe.excerpt | strip_html | truncate: 100 }}
                </p>
                <div class="flex items-center justify-between pt-6 border-t border-slate-50">
                    <div class="flex items-center space-x-2 text-slate-400">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                        <span class="text-[11px] font-bold uppercase tracking-wider">{{ recipe.time | default: "30 perc" }}</span>
                    </div>
                    <a href="{{ recipe.url | relative_url }}" class="text-blue-500 text-[11px] font-black uppercase tracking-[0.2em] group-hover:mr-2 transition-all">
                        Megnézem &rarr;
                    </a>
                </div>
            </div>
        </article>
        {% endfor %}
    </div>
</div>
