---
layout: default
title: "Blog"
---

<section class="max-w-6xl mx-auto py-16 px-6">
    <header class="text-center mb-20">
        <span class="text-blue-500 font-bold text-xs uppercase tracking-[0.3em] mb-4 block">Minden, ami mentes</span>
        <h1 class="text-4xl md:text-6xl font-black text-slate-900 tracking-tighter mb-6">
            Friss <span class="text-blue-500 italic font-serif">Bejegyzések</span>
        </h1>
        <div class="w-24 h-1.5 bg-gradient-to-r from-blue-600 to-sky-400 mx-auto rounded-full"></div>
    </header>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
        {% for post in site.posts %}
        <article class="group flex flex-col bg-white rounded-[2.5rem] border border-slate-100 overflow-hidden hover:shadow-2xl transition-all duration-500">
            <div class="aspect-[16/10] overflow-hidden relative">
                {% if post.image %}
                    <img src="{{ post.image }}" alt="{{ post.title }}" class="w-full h-full object-cover group-hover:scale-105 transition duration-700">
                {% else %}
                    <div class="w-full h-full bg-gradient-to-br from-blue-50 to-blue-100"></div>
                {% endif %}
                <div class="absolute top-6 left-6">
                    <span class="bg-white/90 backdrop-blur-md px-4 py-1.5 rounded-full text-[10px] font-black uppercase tracking-widest text-blue-600 shadow-sm">
                        {{ post.categories | first | default: 'Cikk' }}
                    </span>
                </div>
            </div>
            <div class="p-10 flex flex-col flex-grow">
                <span class="text-slate-400 font-bold text-[10px] uppercase tracking-widest mb-3">
                    {{ post.date | date: "%Y. %m. %d." }}
                </span>
                <h2 class="text-2xl font-bold text-slate-900 mb-4 group-hover:text-blue-600 transition leading-snug">
                    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
                </h2>
                <p class="text-slate-500 leading-relaxed mb-8 line-clamp-3 italic">
                    {{ post.excerpt | strip_html | truncate: 160 }}
                </p>
                <div class="mt-auto">
                    <a href="{{ post.url | relative_url }}" class="text-xs font-black uppercase tracking-widest border-b-2 border-blue-100 hover:border-blue-500 transition-all pb-1">
                        Elolvasom a cikket &rarr;
                    </a>
                </div>
            </div>
        </article>
        {% endfor %}
    </div>
    <div class="mt-24 p-12 bg-slate-900 rounded-[3rem] text-center text-white relative overflow-hidden shadow-2xl">
        <div class="absolute top-0 right-0 w-32 h-32 bg-blue-500/20 blur-3xl rounded-full -mr-16 -mt-16"></div>
        <h3 class="text-2xl font-bold mb-4 relative z-10 font-serif italic">Inspirációt keresel a konyhában?</h3>
        <p class="text-slate-400 mb-8 max-w-md mx-auto relative z-10 text-sm">Nézd meg a legújabb laktózmentes receptjeinket is!</p>
        <a href="{{ '/receptek/' | relative_url }}" class="inline-block bg-blue-500 text-white px-10 py-4 rounded-full font-black text-xs uppercase tracking-widest hover:bg-blue-600 transition shadow-lg shadow-blue-900/20">Irány a receptek</a>
    </div>
</section>
