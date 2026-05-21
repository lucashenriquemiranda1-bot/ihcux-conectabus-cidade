# ihcux-conectabus-cidade

## 👥 Integrantes
* **Cauã Mendes** - RA: 326141078
* **Fábio Henrique Zanini Ferreira** - RA: 326113387
* **Gabriel Ferreira de Souza** - RA:325140970
* **Lucas Henrique Miranda** - RA: 325131396
* **Curso:** Análise e Desenvolvimento de Sistemas (ADS)
* **Instituição:** Centro Universitário UNA – Belo Horizonte
* **Matéria:** Interação Humano Computador e UX
* **Professor:** Daniel Henrique Matos de Paiva

---

## 🏃 Contexto de Uso
O aplicativo "ConectaBus" foi projetado para cenários urbanos de alta pressão, estresse e dinamismo. O usuário padrão encontra-se em ambiente externo, muitas vezes correndo para não perder o metrô ou o ônibus, carregando mochilas ou sacolas em uma das mãos, o que limita sua capacidade de interação com o dispositivo móvel. 

Nesse contexto de alta carga cognitiva e distração ambiental, o aplicativo atua minimizando fricções e entregando as cinco principais necessidades de forma imediata: busca de rotas, tempo estimado de percurso, mapa de navegação ativa, pagamento digital via QR Code e verificação de detalhes de ocupação/acessibilidade do veículo.

---

## 🧠 Decisões de UX & Engenharia de IHC

As decisões de design de baixa fidelidade foram fundamentadas nos princípios de IHC para redução de carga cognitiva e otimização do tempo de resposta do usuário:

* **Design para Uso com Um Polegar (Thumb Zone):** Atendendo diretamente à restrição física do usuário em movimento, toda a área de interação principal (barras de busca, botões de filtros, cards de seleção e o Menu de Navegação Inferior fixo) foi posicionada estritamente nos 40% inferiores das telas. O topo foi reservado exclusivamente para leitura de dados estáticos de confirmação.
* **Menu de Navegação Inferior Fixo:** Implementado de forma persistente em todas as telas (`Rotas`, `Carteira`, `Perfil`) para permitir a alternância de contexto (como abrir o meio de pagamento na catraca) com um único clique do polegar, eliminando caminhos complexos de navegação.
* **Hierarquia Visual Baseada na Pressa:** O tempo estimado para a chegada do transporte (ex: **"22 min"**) recebeu o maior peso visual e escala tipográfica do protótipo, posicionando-se à frente do número da linha, pois o tempo é o fator primordial de decisão para o usuário apressado.
* **Prevenção do Erro Catastrófico (Resposta à Provocação do Professor):** Para evitar que o usuário pegue o transporte no sentido inverso e vá para o lado errado da cidade, implementamos "Ancoragens de Direção" explícitas e redundantes em todas as etapas (Cards da Tela 2, Barra de Status da Tela 3 e Detalhes da Tela 5), exibindo o indicador textualmente: `Linha [X] — Sentido: [Destino Final]`.

---

## ♿ Acessibilidade e Resolução de Desafios

O protótipo incorpora soluções para limitações físicas, visuais e de infraestrutura técnica:

* **Acessibilidade Motora e Visual:** A Tela 5 foi estruturada com um checklist claro de acessibilidade (`Plataforma Operacional`, `Ar-condicionado`), permitindo que pessoas com mobilidade reduzida filtrem e escolham veículos adequados. Os elementos clicáveis possuem áreas de toque expandidas para evitar cliques errados por trepidação ou pressa.
* **Desafio Opcional - Modo Noturno:** Para evitar o ofuscamento visual em ambientes escuros na rua, a interface foi projetada para inverter sua paleta de cores para tons escuros (Grafite/Preto), mantendo o alto contraste tipográfico para leitura rápida sem fadiga ocular.
* **Desafio Opcional - Modo Offline (Túnel do Metrô):** Prevendo a perda de sinal 5G, o layout altera a barra superior para a cor amarela com o aviso `Sem sinal - Acessando rotas salvas localmente`. A interface bloqueia buscas externas e exibe rotas frequentes e dados de mapas armazenados previamente em cache, impedindo o travamento do app.

<img width="579" height="683" alt="screenshot 2026-05-20 at 20 46 31" src="https://github.com/user-attachments/assets/a2fb7aff-d884-40b9-b5e8-374746dabf4e" />
