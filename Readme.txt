Descrição:

A Calculadora EcoTrip é uma aplicação web interativa que calcula o impacto ambiental (emissões de CO₂) de viagens entre cidades brasileiras, comparando diferentes modos de transporte: bicicleta, carro, ônibus e caminhão.

Desenvolvida no Bootcamp GitHub Copilot - Código na Prática da DIO, simula cenários reais de mobilidade sustentável, incentivando escolhas ecológicas e calculando créditos de carbono necessários para neutralização.


Funcionalidades:
Autocomplete de cidades brasileiras com distâncias pré-cadastradas.

Cálculo automático de emissões de CO₂ (kg/km).

Comparação visual com barras coloridas para todos os transportes.

Créditos de carbono e custo estimado de compensação (R$/kg).

Inserção manual de distância para rotas customizadas.

Design responsivo - funciona em desktop, tablet e mobile.

Sem dependências externas - HTML, CSS e JS puro.

 
Exemplo de Uso:
Selecione São Paulo → Rio de Janeiro (430 km).

Escolha Carro → 107.5 kg CO₂.

Compare: Bicicleta (0 kg), Ônibus (43 kg), Caminhão (64.5 kg).

Créditos necessários: 107.5 kg (~R$ 5.38)


Tecnologias Utilizadas:
| Tecnologia | Uso                                     |
| ---------- | --------------------------------------- |
| HTML5      | Estrutura semântica e formulários dio​  |
| CSS3       | Estilos responsivos, Flexbox, animações |
| Vanilla JS | Lógica de cálculo, DOM manipulation     |
| Datalist   | Autocomplete nativo                     |


Estrutura do Projeto:

ecotrip-calculator/
├── index.html     # Interface principal
├── style.css      # Estilos e responsividade
├── script.js      # Lógica de negócio e cálculos
└── README.md      # Esta documentação


Como Executar:
Clone ou baixe os arquivos.

Abra index.html em qualquer navegador moderno (Chrome, Firefox, Safari).

Sem instalação necessária - funciona offline!


Configuração e Customização
Fatores de Emissão (kg CO₂/km) [Aproximações reais]

const EMISSION_FACTORS = {
    bike: 0,      // Zero emissão
    car: 0.25,    // Gasolina média
    bus: 0.1,     // Transporte coletivo
    truck: 0.15   // Carga pesada
};


Distâncias Pré-Cadastradas
Adicione rotas em CONFIG.DISTANCES:

'São Paulo': { 
    'Rio de Janeiro': 430,
    'Salvador': 1500
}


Preço Créditos Carbono:

pricePerKg: 0.05  // R$ 0,05/kg CO₂ (mercado voluntário 2026)



Fórmulas Utilizadas:

Emissão total:

Emissão = Distância (km) x Fator (kg/km)

Custo Compensação:

Custo = Emissão x Preço/kg



 Melhorias Futuras:

Integração Google Maps API para distâncias reais.

API de preços reais de créditos carbono.

Histórico de cálculos (LocalStorage).

Export PDF dos resultados.

Mais transportes: Avião, Trem, Moto.

Gráficos interativos (Chart.js).


Sustentabilidade:
Zero emissões no servidor - Static hosting.

Dados leves (~10KB total).

Hospede grátis em GitHub Pages ou Netlify.



