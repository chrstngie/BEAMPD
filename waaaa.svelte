<div class="p-6">
  <header class="mb-6 mt-4">
    <h1 class="text-3xl font-black text-[#002266] tracking-tighter">Archive</h1>
    <p class="text-xs font-bold text-slate-400 uppercase tracking-widest">Local Bioacoustic Logs Explorer</p>
  </header>

  <div class="relative mb-6">
    <span class="material-symbols-outlined absolute left-4 top-1/2 -translate-y-1/2 text-slate-400">search</span>
    <input type="text" placeholder="Search Node ID or Pest Type..." class="w-full p-4 pl-12 bg-slate-100 rounded-2xl border-none outline-none focus:ring-2 focus:ring-[#002266] font-medium text-sm" />
  </div>

  <div class="flex gap-2 mb-8 overflow-x-auto pb-2">
    <button class="px-4 py-2 bg-[#fccc00] text-[#002266] rounded-full text-[10px] font-black uppercase tracking-widest whitespace-nowrap">All Logs</button>
    <button class="px-4 py-2 bg-slate-100 text-slate-500 rounded-full text-[10px] font-black uppercase tracking-widest whitespace-nowrap">Critical Nodes</button>
    <button class="px-4 py-2 bg-slate-100 text-slate-500 rounded-full text-[10px] font-black uppercase tracking-widest whitespace-nowrap">High Confidence</button>
  </div>

  <div class="bg-white rounded-[32px] p-6 border border-slate-100 shadow-sm mb-8">
     <div class="flex justify-between items-start mb-4">
        <div>
            <p class="text-[10px] font-black text-red-600 flex items-center gap-1 uppercase tracking-widest">
                <span class="w-2 h-2 rounded-full bg-red-600 animate-pulse"></span> Selected Audio Stream
            </p>
            <h2 class="text-xl font-black text-[#002266] mt-1">Node-142B_Sector7</h2>
        </div>
        <div class="flex gap-2">
            <button class="w-10 h-10 bg-slate-100 rounded-full flex items-center justify-center"><span class="material-symbols-outlined text-sm">play_arrow</span></button>
            <button class="w-10 h-10 bg-slate-100 rounded-full flex items-center justify-center"><span class="material-symbols-outlined text-sm">share</span></button>
        </div>
     </div>

     <div class="flex items-end justify-between h-24 gap-1 mb-6 px-4">
        {#each [40, 70, 50, 90, 60, 100, 80, 45, 75, 55, 95, 65, 30] as height}
            <div class="flex-grow bg-[#002266] rounded-full" style="height: {height}%"></div>
            <div class="flex-grow bg-slate-200 rounded-full" style="height: {height/2}%"></div>
        {/each}
     </div>

     <div class="flex justify-between border-t border-slate-50 pt-4">
        <div>
            <p class="text-[10px] font-bold text-slate-400 uppercase">Timestamp</p>
            <p class="text-xs font-black text-[#002266]">Oct 24, 2026 - 14:22</p>
        </div>
        <div class="text-right">
            <p class="text-[10px] font-bold text-slate-400 uppercase">Confidence Score</p>
            <p class="text-xs font-black text-blue-600">98.2% Accuracy</p>
        </div>
     </div>
  </div>

  <h3 class="text-xs font-black text-slate-400 uppercase tracking-widest mb-4 px-2">Archived Logs (42)</h3>
  <div class="space-y-3 mb-10">
    {#each ['Termite', 'Weevil', 'Background'] as pest}
      <div class="bg-slate-50 p-4 rounded-2xl flex items-center justify-between group active:scale-[0.98] transition-all">
        <div class="flex items-center gap-4">
            <div class="w-12 h-12 bg-white rounded-xl flex items-center justify-center shadow-sm">
                <span class="material-symbols-outlined text-[#002266]">{pest === 'Background' ? 'eco' : 'pest_control'}</span>
            </div>
            <div>
                <p class="text-sm font-black text-[#002266]">{pest === 'Background' ? 'Spodoptera frugiperda' : pest + ' Activity'}</p>
                <p class="text-[10px] font-bold text-slate-400 uppercase tracking-widest">Node-092A • 12:45 • Sector 3</p>
            </div>
        </div>
        <span class="material-symbols-outlined text-slate-300">chevron_right</span>
      </div>
    {/each}
  </div>
</div>