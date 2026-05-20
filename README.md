<!DOCTYPE html>
<html lang="cs">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Co je to vlastně databáze?</title>
    <!-- Tailwind CSS pro moderní UI -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Lucide ikony -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap');
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: #080c14;
        }
        .glow-violet {
            box-shadow: 0 0 25px rgba(139, 92, 246, 0.15);
        }
    </style>
</head>
<body class="text-slate-200 min-h-screen pb-16">

    <!-- Header -->
    <header class="border-b border-slate-800/80 bg-slate-950/60 backdrop-blur sticky top-0 z-50">
        <div class="max-w-4xl mx-auto px-4 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-3">
                <div class="bg-violet-500/10 p-2 rounded-lg text-violet-400">
                    <i data-lucide="help-circle" class="w-6 h-6"></i>
                </div>
                <span class="font-bold text-lg tracking-tight">Vysvětlení pro lidi 15+</span>
            </div>
            <span class="text-xs bg-slate-800 text-slate-400 px-3 py-1 rounded-full font-medium">Lekce 0: Úvod</span>
        </div>
    </header>

    <main class="max-w-4xl mx-auto px-4 mt-8 space-y-8">

        <!-- Hero sekce -->
        <section class="bg-gradient-to-br from-slate-900 to-slate-950 border border-slate-800/60 rounded-2xl p-6 md:p-8 relative overflow-hidden">
            <div class="absolute top-0 right-0 w-80 h-80 bg-violet-500/5 rounded-full blur-3xl -mr-32 -mt-32"></div>
            <div class="relative z-10 space-y-4">
                <span class="bg-violet-500/10 text-violet-400 text-xs font-semibold px-3 py-1 rounded-full uppercase tracking-wider">Základní otázka</span>
                <h1 class="text-3xl md:text-4xl font-extrabold tracking-tight text-white">
                    Co je to vlastně ta <span class="text-transparent bg-clip-text bg-gradient-to-r from-violet-400 to-fuchsia-400">databáze</span>?
                </h1>
                <p class="text-slate-400 leading-relaxed text-sm md:text-base">
                    Když si otevřeš Instagram, TikTok nebo Brawl Stars, vidíš hromadu fotek, herních skóre a zpráv. Tyhle věci se neobjevují kouzlem. Jsou uložené v databázi. 
                </p>
                <div class="p-4 bg-slate-950/60 rounded-xl border border-slate-800/50 text-sm">
                    💡 <strong>Jednoduchá definice:</strong> Databáze je extrémně bezpečný, chytrý a brutálně rychlý digitální sklad na data. Na rozdíl od tvé paměti v mobilu se z ní nic nesmaže, ani když se vybije baterka nebo spadne aplikace.
                </div>
            </div>
        </section>

        <!-- Proč nestačí Excel? -->
        <section class="space-y-4">
            <h2 class="text-xl md:text-2xl font-bold text-white flex items-center gap-2">
                <i data-lucide="alert-triangle" class="text-amber-400 w-6 h-6"></i>
                Proč vývojáři nepoužívají Excel nebo TXT soubory?
            </h2>
            <p class="text-slate-400 text-sm">
                Napadlo tě někdy, proč prostě všechny uživatele neuložíme do velké tabulky v Excelu nebo do textového souboru? Tady jsou 3 hlavní důvody:
            </p>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                <!-- Karta 1 -->
                <div class="bg-slate-900/50 border border-slate-800 p-5 rounded-xl space-y-3">
                    <div class="text-rose-400 bg-rose-500/10 w-10 h-10 rounded-lg flex items-center justify-center">
                        <i data-lucide="gauge" class="w-5 h-5"></i>
                    </div>
                    <h3 class="font-bold text-white text-base">Rychlost (Rychlost vyhledávání)</h3>
                    <p class="text-slate-400 text-xs leading-relaxed">
                        Kdyby měl Instagram hledat tvůj profil v textovém souboru mezi 1 miliardou lidí, musel by ho číst odshora dolů. Trvalo by to věčnost. Databáze na to má speciální zkratky (tzv. indexy).
                    </p>
                </div>
                <!-- Karta 2 -->
                <div class="bg-slate-900/50 border border-slate-800 p-5 rounded-xl space-y-3">
                    <div class="text-sky-400 bg-sky-500/10 w-10 h-10 rounded-lg flex items-center justify-center">
                        <i data-lucide="users-2" class="w-5 h-5"></i>
                    </div>
                    <h3 class="font-bold text-white text-base">Více lidí najednou</h3>
                    <p class="text-slate-400 text-xs leading-relaxed">
                        Do jednoho Excelu nemůže zapisovat 50 000 lidí naráz, aniž by se soubor poškodil nebo uzamkl. Databáze zvládne miliony zápisů v téže vteřině.
                    </p>
                </div>
                <!-- Karta 3 -->
                <div class="bg-slate-900/50 border border-slate-800 p-5 rounded-xl space-y-3">
                    <div class="text-emerald-400 bg-emerald-500/10 w-10 h-10 rounded-lg flex items-center justify-center">
                        <i data-lucide="shield-check" class="w-5 h-5"></i>
                    </div>
                    <h3 class="font-bold text-white text-base">Bezpečnost a validace</h3>
                    <p class="text-slate-400 text-xs leading-relaxed">
                        Do Excelu může kdokoli napsat cokoli. Databáze tě nepustí. Hlídá, aby věk byl číslo, e-mail obsahoval zavináč a heslo nebylo prázdné.
                    </p>
                </div>
            </div>
        </section>

        <!-- INTERAKTIVNÍ TEST RYCHLOSTI -->
        <section class="bg-slate-900 border border-slate-800 rounded-2xl p-6 space-y-6 glow-violet">
            <div class="space-y-2">
                <span class="bg-violet-500 text-slate-950 text-xs font-bold px-2.5 py-1 rounded-md">INTERAKTIVNÍ EXPERIMENT</span>
                <h2 class="text-xl font-bold text-white">Vyzkoušej si to: Soubor vs. Databáze</h2>
                <p class="text-slate-400 text-sm">
                    Představ si, že hledáme jednu konkrétní písničku v databázi Spotify, která obsahuje <strong>10 000 000 songů</strong>. Klikni na tlačítko a sleduj, jak dlouho to bude komu trvat!
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <!-- Textový soubor (Lineární vyhledávání) -->
                <div class="bg-slate-950 p-4 rounded-xl border border-slate-850 space-y-4">
                    <div class="flex items-center justify-between">
                        <span class="text-xs text-slate-400 uppercase tracking-wider font-semibold">Obyčejný textový soubor / Excel</span>
                        <span class="text-xs text-rose-400 font-mono">Hledání řádek po řádku</span>
                    </div>
                    <div class="h-24 flex flex-col justify-center items-center bg-slate-900/40 rounded-lg border border-slate-800">
                        <div id="file-status" class="text-sm font-semibold text-slate-300">Připraven k hledání</div>
                        <div id="file-progress" class="w-4/5 bg-slate-800 h-2 rounded-full mt-2 overflow-hidden hidden">
                            <div id="file-progress-bar" class="bg-rose-500 h-full w-0 transition-all duration-75"></div>
                        </div>
                    </div>
                    <div class="flex justify-between items-center text-sm">
                        <span class="text-slate-400">Prohledáno záznamů:</span>
                        <span id="file-scanned" class="font-mono font-bold text-rose-400">0</span>
                    </div>
                    <div class="flex justify-between items-center text-sm border-t border-slate-800 pt-2">
                        <span class="text-slate-400">Čas hledání:</span>
                        <span id="file-time" class="font-mono font-bold text-rose-400">0 ms</span>
                    </div>
                </div>

                <!-- Databáze (Indexované vyhledávání) -->
                <div class="bg-slate-950 p-4 rounded-xl border border-slate-850 space-y-4">
                    <div class="flex items-center justify-between">
                        <span class="text-xs text-slate-400 uppercase tracking-wider font-semibold">Moderní Databáze</span>
                        <span class="text-xs text-emerald-400 font-mono">Indexované B-Tree hledání</span>
                    </div>
                    <div class="h-24 flex flex-col justify-center items-center bg-slate-900/40 rounded-lg border border-slate-800">
                        <div id="db-status" class="text-sm font-semibold text-slate-300">Připravena k hledání</div>
                        <div id="db-animation" class="hidden text-emerald-400 animate-bounce">
                            <i data-lucide="check-circle-2" class="w-8 h-8"></i>
                        </div>
                    </div>
                    <div class="flex justify-between items-center text-sm">
                        <span class="text-slate-400">Prohledáno záznamů:</span>
                        <span id="db-scanned" class="font-mono font-bold text-emerald-400">0</span>
                    </div>
                    <div class="flex justify-between items-center text-sm border-t border-slate-800 pt-2">
                        <span class="text-slate-400">Čas hledání:</span>
                        <span id="db-time" class="font-mono font-bold text-emerald-400">0 ms</span>
                    </div>
                </div>
            </div>

            <div class="text-center pt-2">
                <button id="btn-start" onclick="startRace()" class="bg-violet-600 hover:bg-violet-500 text-white font-bold py-3 px-8 rounded-xl transition duration-200 shadow-lg shadow-violet-900/30">
                    Spustit test rychlosti 🏁
                </button>
            </div>
        </section>

        <!-- Jak data putují? (Architektura v praxi) -->
        <section class="space-y-4">
            <h2 class="text-xl md:text-2xl font-bold text-white flex items-center gap-2">
                <i data-lucide="git-commit" class="text-violet-400 w-6 h-6"></i>
                Jak vlastně data cestují?
            </h2>
            <p class="text-slate-400 text-sm">
                Když si v aplikaci (např. v mobilu) lajkneš příspěvek, neukládá se to přímo do databáze na tvém telefonu (to by ostatní tvůj lajk neviděli). Cesta vypadá takto:
            </p>

            <!-- Grafické schéma -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-4 text-center mt-4">
                <div class="bg-slate-900/30 border border-slate-800 p-4 rounded-xl space-y-2">
                    <div class="text-blue-400 mx-auto w-8 h-8 flex items-center justify-center"><i data-lucide="smartphone"></i></div>
                    <h4 class="font-bold text-white text-sm">1. Frontend (Tvůj mobil)</h4>
                    <p class="text-slate-500 text-xs">Klikneš na tlačítko "To se mi líbí". Mobil pošle požadavek přes internet.</p>
                </div>
                <div class="bg-slate-900/30 border border-slate-800 p-4 rounded-xl space-y-2 relative">
                    <div class="hidden md:block absolute top-1/2 -right-3 -translate-y-1/2 text-slate-700 font-mono">&rarr;</div>
                    <div class="text-amber-400 mx-auto w-8 h-8 flex items-center justify-center"><i data-lucide="server"></i></div>
                    <h4 class="font-bold text-white text-sm">2. Backend (Server v cloudu)</h4>
                    <p class="text-slate-500 text-xs">Server (např. v Node.js/Pythonu) zkontroluje, jestli jsi přihlášený a smíš lajkovat.</p>
                </div>
                <div class="bg-slate-900/30 border border-slate-800 p-4 rounded-xl space-y-2">
                    <div class="text-emerald-400 mx-auto w-8 h-8 flex items-center justify-center"><i data-lucide="database"></i></div>
                    <h4 class="font-bold text-white text-sm">3. Databáze (Digitální trezor)</h4>
                    <p class="text-slate-500 text-xs">Server zapíše lajk do databáze. Od této chvíle ho uvidí všichni na celém světě.</p>
                </div>
            </div>
        </section>

        <!-- K zamyšlení na konec hodiny -->
        <section class="bg-slate-950 border border-slate-850 p-6 rounded-xl space-y-3">
            <h3 class="font-bold text-white text-base">Zajímavá otázka na diskuzi se studenty:</h3>
            <p class="text-sm text-slate-400 leading-relaxed">
                "Představte si, že hrajete online hru a na vteřinu vám vypadne internet. Proč se vaše postavička vrátí o kousek zpět? Kde byla ta data uložená a jak se synchronizují s hlavní databází?"
            </p>
        </section>

    </main>

    <!-- Footer -->
    <footer class="max-w-4xl mx-auto px-4 mt-12 pt-6 border-t border-slate-900 text-center text-xs text-slate-500">
        Výuková stránka pro pochopení naprostých základů IT. Otevři si další lekci pro SQL! 🚀
    </footer>

    <!-- JS Simulace pro test rychlosti -->
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            lucide.createIcons();
        });

        function startRace() {
            const btn = document.getElementById('btn-start');
            btn.disabled = true;
            btn.innerText = "Hledám...";

            // Reset prvků souboru
            const fileStatus = document.getElementById('file-status');
            const fileProgress = document.getElementById('file-progress');
            const fileProgressBar = document.getElementById('file-progress-bar');
            const fileScanned = document.getElementById('file-scanned');
            const fileTime = document.getElementById('file-time');

            fileStatus.innerText = "Čtu textový soubor od začátku...";
            fileProgress.classList.remove('hidden');
            fileProgressBar.style.width = '0%';
            fileScanned.innerText = "0";
            fileTime.innerText = "Počítám...";

            // Reset prvků databáze
            const dbStatus = document.getElementById('db-status');
            const dbAnimation = document.getElementById('db-animation');
            const dbScanned = document.getElementById('db-scanned');
            const dbTime = document.getElementById('db-time');

            dbStatus.classList.remove('hidden');
            dbStatus.innerText = "Používám index B-Tree...";
            dbAnimation.classList.add('hidden');
            dbScanned.innerText = "0";
            dbTime.innerText = "Počítám...";

            // 1. Simulace DATABÁZE (je hotová instantně)
            setTimeout(() => {
                dbStatus.classList.add('hidden');
                dbAnimation.classList.remove('hidden');
                // Databáze nepotřebuje projít 10M záznamů, díky stromové struktuře najde záznam cca na 15 až 20 kroků
                dbScanned.innerText = "18 kroků";
                dbTime.innerText = "0.04 ms";
            }, 150);

            // 2. Simulace SOUBORU (trvá déle, animujeme průchod)
            let scannedCount = 0;
            const targetScanned = 10000000; // 10 milionů
            const startTime = performance.now();

            let interval = setInterval(() => {
                scannedCount += Math.floor(Math.random() * 800000) + 400000;
                
                if (scannedCount >= targetScanned) {
                    scannedCount = targetScanned;
                    clearInterval(interval);
                    
                    const endTime = performance.now();
                    const duration = Math.round(endTime - startTime + 1200); // umělé navýšení pro dramatičnost na webu
                    
                    fileProgressBar.style.width = '100%';
                    fileScanned.innerText = scannedCount.toLocaleString('cs-CZ');
                    fileTime.innerText = duration + " ms";
                    fileStatus.innerText = "Hotovo! Písnička nalezena.";
                    
                    btn.disabled = false;
                    btn.innerText = "Spustit test rychlosti znovu 🏁";
                } else {
                    const percent = (scannedCount / targetScanned) * 100;
                    fileProgressBar.style.width = percent + '%';
                    fileScanned.innerText = scannedCount.toLocaleString('cs-CZ');
                    fileTime.innerText = Math.round(performance.now() - startTime) + " ms";
                }
            }, 100);
        }
    </script>
</body>
</html>
