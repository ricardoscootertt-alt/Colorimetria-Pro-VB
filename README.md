<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Espaço Vanessa Braga | Colorimetria AI</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Inter:wght@300;400;600&display=swap');
        
        :root {
            --rose-gold: #e5b3a3;
            --luxury-black: #2d2d2d;
            --soft-cream: #fdfaf9;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--soft-cream);
            color: var(--luxury-black);
        }

        .brand-font {
            font-family: 'Playfair Display', serif;
        }

        .bg-rose-gold { background-color: var(--rose-gold); }
        .text-rose-gold { color: #c28e7e; }
        .border-rose-gold { border-color: var(--rose-gold); }

        .gradient-brand {
            background: linear-gradient(135deg, #2d2d2d 0%, #4a4a4a 100%);
        }

        .glass-card {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(229, 179, 163, 0.3);
            border-radius: 1.5rem;
        }

        .btn-premium {
            background-color: var(--rose-gold);
            color: white;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(229, 179, 163, 0.4);
        }

        .btn-premium:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(229, 179, 163, 0.6);
            background-color: #d8a291;
        }

        .oswald-ring {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            background: conic-gradient(
                #ef4444 0deg 60deg,    /* Vermelho */
                #f97316 60deg 120deg,  /* Laranja */
                #eab308 120deg 180deg, /* Amarelo */
                #22c55e 180deg 240deg, /* Verde */
                #3b82f6 240deg 300deg, /* Azul */
                #a855f7 300deg 360deg  /* Violeta */
            );
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .oswald-inner {
            width: 70%;
            height: 70%;
            background: var(--soft-cream);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            font-size: 0.7rem;
            font-weight: bold;
        }
    </style>
</head>
<body class="p-4 md:p-8">
    <div class="max-w-5xl mx-auto">
        <!-- Logo & Header -->
        <header class="text-center mb-10">
            <h1 class="brand-font text-4xl md:text-5xl mb-2 text-rose-gold">Espaço Vanessa Braga</h1>
            <div class="h-1 w-24 bg-rose-gold mx-auto mb-4"></div>
            <p class="uppercase tracking-widest text-sm text-gray-500 font-light">Consultoria Técnica de Colorimetria Inteligente</p>
        </header>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
            <!-- Coluna de Diagnóstico -->
            <div class="lg:col-span-2 space-y-6">
                <div class="glass-card p-8 shadow-sm">
                    <h2 class="brand-font text-2xl mb-6 flex items-center gap-3">
                        <span class="w-8 h-8 rounded-full bg-rose-gold text-white flex items-center justify-center text-sm">01</span>
                        Análise de Perfil
                    </h2>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div class="space-y-4">
                            <div>
                                <label class="block text-xs font-bold uppercase text-gray-400 mb-2">Nome da Cliente</label>
                                <input type="text" id="client-name" placeholder="Ex: Maria Silva" class="w-full p-3 border-b-2 border-gray-100 focus:border-rose-gold outline-none bg-transparent">
                            </div>
                            <div>
                                <label class="block text-xs font-bold uppercase text-gray-400 mb-2">Altura de Tom Natural</label>
                                <select id="natural-tone" class="w-full p-3 bg-gray-50 rounded-lg outline-none">
                                    <option value="1">1 - Preto</option>
                                    <option value="2">2 - Castanho Escuríssimo</option>
                                    <option value="3">3 - Castanho Escuro</option>
                                    <option value="4">4 - Castanho Médio</option>
                                    <option value="5">5 - Castanho Claro</option>
                                    <option value="6">6 - Louro Escuro</option>
                                    <option value="7">7 - Louro Médio</option>
                                    <option value="8">8 - Louro Claro</option>
                                    <option value="9">9 - Louro Muito Claro</option>
                                    <option value="10">10 - Louro Claríssimo</option>
                                </select>
                            </div>
                        </div>

                        <div class="space-y-4">
                            <div>
                                <label class="block text-xs font-bold uppercase text-gray-400 mb-2">Tom Desejado</label>
                                <select id="target-tone" class="w-full p-3 bg-gray-50 rounded-lg outline-none">
                                    <option value="1">1 - Preto</option>
                                    <option value="3">3 - Castanho Escuro</option>
                                    <option value="4">4 - Castanho Médio</option>
                                    <option value="5">5 - Castanho Claro</option>
                                    <option value="6">6 - Louro Escuro</option>
                                    <option value="7">7 - Louro Médio</option>
                                    <option value="8">8 - Louro Claro</option>
                                    <option value="9">9 - Louro Muito Claro</option>
                                    <option value="10">10 - Louro Claríssimo</option>
                                </select>
                            </div>
                            <div>
                                <label class="block text-xs font-bold uppercase text-gray-400 mb-2">Cabelos Brancos (%)</label>
                                <input type="range" id="gray-hair" min="0" max="100" value="0" class="w-full h-2 bg-gray-200 rounded-lg appearance-none cursor-pointer accent-rose-gold">
                                <div class="flex justify-between text-[10px] mt-1 text-gray-400">
                                    <span>0%</span>
                                    <span id="gray-label" class="font-bold text-rose-gold">0%</span>
                                    <span>100%</span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <button onclick="generateProtocol()" class="w-full mt-8 btn-premium py-4 rounded-xl font-bold uppercase tracking-widest text-sm">
                        Gerar Protocolo Vanessa Braga
                    </button>
                </div>

                <!-- Painel de Resultados (Oculto Inicialmente) -->
                <div id="protocol-result" class="hidden glass-card p-8 border-l-8 border-l-rose-gold shadow-xl">
                    <div class="flex justify-between items-start mb-6">
                        <h3 class="brand-font text-2xl text-rose-gold">Resultado do Diagnóstico</h3>
                        <span id="date-stamp" class="text-[10px] text-gray-400"></span>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-8">
                        <div class="p-4 border border-rose-gold border-opacity-20 rounded-xl">
                            <span class="text-[10px] uppercase text-gray-400 block mb-1">Mistura</span>
                            <p id="res-formula" class="font-bold text-lg">--</p>
                        </div>
                        <div class="p-4 border border-rose-gold border-opacity-20 rounded-xl">
                            <span class="text-[10px] uppercase text-gray-400 block mb-1">Oxidante (OX)</span>
                            <p id="res-ox" class="font-bold text-lg">--</p>
                        </div>
                        <div class="p-4 border border-rose-gold border-opacity-20 rounded-xl">
                            <span class="text-[10px] uppercase text-gray-400 block mb-1">Fundo Exposto</span>
                            <p id="res-fundo" class="font-bold text-lg">--</p>
                        </div>
                    </div>

                    <div class="bg-gray-50 p-6 rounded-2xl relative overflow-hidden">
                        <div class="absolute right-[-10px] top-[-10px] opacity-10">
                            <svg width="100" height="100" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/></svg>
                        </div>
                        <h4 class="text-xs font-bold uppercase tracking-tighter text-rose-gold mb-2">Dica Técnica Vanessa Braga:</h4>
                        <p id="res-insight" class="text-sm leading-relaxed text-gray-700 italic">--</p>
                    </div>
                </div>
            </div>

            <!-- Coluna Lateral -->
            <div class="space-y-6">
                <!-- Estrela de Oswald Custom -->
                <div class="glass-card p-6 flex flex-col items-center">
                    <h3 class="brand-font text-lg mb-4 text-center">Círculo Cromático</h3>
                    <div class="oswald-ring">
                        <div class="oswald-inner">
                            Neutralização<br>Espaço VB
                        </div>
                    </div>
                    <div class="mt-6 w-full text-[11px] space-y-2">
                        <div class="flex justify-between"><span>Vermelho</span> <span class="text-blue-500 font-bold">← Mate / Cinza</span></div>
                        <div class="flex justify-between"><span>Laranja</span> <span class="text-blue-400 font-bold">← Azul / Íris</span></div>
                        <div class="flex justify-between"><span>Amarelo</span> <span class="text-purple-500 font-bold">← Violeta</span></div>
                    </div>
                </div>

                <!-- Histórico Rápido -->
                <div class="glass-card p-6">
                    <h3 class="brand-font text-lg mb-4">Últimos Atendimentos</h3>
                    <div id="history-list" class="space-y-3 max-h-60 overflow-y-auto pr-2">
                        <p class="text-xs text-gray-400 text-center py-4 italic">Nenhum registro recente.</p>
                    </div>
                </div>
            </div>
        </div>

        <footer class="mt-16 text-center border-t border-rose-gold border-opacity-10 pt-8">
            <p class="brand-font text-rose-gold text-xl mb-2">Espaço Vanessa Braga</p>
            <p class="text-[10px] text-gray-400 uppercase tracking-widest">Excelência em Cor & Saúde Capilar</p>
        </footer>
    </div>

    <script>
        const fundoClareamento = {
            1: "Vermelho Escuríssimo",
            3: "Vermelho Intenso",
            4: "Vermelho Alaranjado",
            5: "Laranja Vermelho",
            6: "Laranja",
            7: "Laranja Amarelo",
            8: "Amarelo",
            9: "Amarelo Muito Claro",
            10: "Amarelo Pálido"
        };

        document.getElementById('gray-hair').addEventListener('input', (e) => {
            document.getElementById('gray-label').innerText = e.target.value + '%';
        });

        const history = [];

        function generateProtocol() {
            const client = document.getElementById('client-name').value || "Cliente s/ Nome";
            const natural = parseInt(document.getElementById('natural-tone').value);
            const target = parseInt(document.getElementById('target-tone').value);
            const gray = parseInt(document.getElementById('gray-hair').value);
            
            const diff = target - natural;
            let ox = "";
            let insight = "";
            let formula = "";

            // Definição de OX para Vanessa Braga
            if (diff <= 0) ox = "10 Vol (Deposição)";
            else if (diff === 1) ox = "20 Vol";
            else if (diff === 2) ox = "30 Vol";
            else ox = "40 Vol (Cuidado com a fibra!)";

            // Lógica de Cobertura de Brancos VB
            if (gray >= 40) {
                formula = `${target}.0 + ${target}.X`;
                insight = `Vanessa, como temos ${gray}% de brancos, use a técnica de pré-pigmentação ou misture 50% de base natural profunda (.0) para garantir a cobertura perfeita sem transparência.`;
            } else if (gray > 0) {
                formula = `${target}.X + 1/4 de ${target}.0`;
                insight = `Leve incidência de brancos. Adicione apenas um toque de base para controle de fidelidade da cor.`;
            } else {
                formula = `${target}.X (Desejada)`;
                insight = `Base sem brancos. Foco total na revelação do reflexo. O fundo de clareamento revelado será ${fundoClareamento[target]}.`;
            }

            // Neutralização Inteligente
            if (target >= 7) {
                insight += ` Para um resultado mais elegante, adicione 1cm de corretor violeta para neutralizar o fundo ${fundoClareamento[target]} típico de loiros.`;
            }

            // Exibir Resultado
            const resultDiv = document.getElementById('protocol-result');
            resultDiv.classList.remove('hidden');
            document.getElementById('res-formula').innerText = formula;
            document.getElementById('res-ox').innerText = ox;
            document.getElementById('res-fundo').innerText = fundoClareamento[target];
            document.getElementById('res-insight').innerText = insight;
            document.getElementById('date-stamp').innerText = new Date().toLocaleDateString('pt-BR');

            // Adicionar ao Histórico
            addToHistory(client, formula);

            // Efeito de Scroll
            resultDiv.scrollIntoView({ behavior: 'smooth' });
        }

        function addToHistory(name, formula) {
            const list = document.getElementById('history-list');
            const item = document.createElement('div');
            item.className = "p-3 bg-white rounded-lg border-l-2 border-rose-gold text-[11px] shadow-sm animate-fade-in";
            item.innerHTML = `<strong>${name}</strong><br><span class="text-gray-400">Fórmula: ${formula}</span>`;
            
            if (list.querySelector('p')) list.innerHTML = '';
            list.prepend(item);
        }
    </script>
</body>
</html>
