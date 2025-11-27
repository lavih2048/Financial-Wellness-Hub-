🌊 Fluxo – Financial Wellness Hub
🚀 Solução Desenvolvida para o Hackathon Financeiro 2025

O Fluxo é mais que um banco digital — é um Assistente de Bem-Estar Financeiro.
A missão é simples e poderosa: traduzir a complexidade bancária em uma experiência humana, reduzindo a ansiedade financeira e guiando o usuário em direção aos seus objetivos por meio de um extrato inteligente, claro e integrado.

🎯 O Desafio

Milhões de usuários enfrentam um problema recorrente:

Extratos cheios de siglas e códigos confusos

Apps fragmentados que não conversam entre si

Falta de personalização e orientação

O Fluxo resolve isso ao centralizar informações e transformar dados bancários em linguagem compreensível, visual e útil.

💡 A Solução

Criamos um Hub Financeiro Integrado que reúne:

✔ Tradução automática de dados (“bancuês” → português claro)
✔ Controle visual de gastos
✔ Serviços financeiros essenciais unificados
✔ Insights que melhoram a saúde financeira do usuário

✨ Funcionalidades Principais (MVP)
🧠 Extrato Inteligente & Humano

Tradução automática de códigos bancários

Exemplo: PGTO *UBER → Uber – Viagens

Categorização visual com ícones e cores

Agrupamento amigável por data (ex: Hoje, Ontem, Esta Semana)

🔗 Hub de Serviços Integrados

Pix Inteligente
Sugere pagamentos recorrentes e lembra transações importantes.

Cashback com Propósito
Cashback direcionado diretamente para uma meta de sonho (ex: viagem).

Seguro On-Demand
Ative ou desative proteções com apenas um clique.

🎨 Personalização & Insights

Saudações dinâmicas baseadas no saldo, data e humor financeiro

Alertas de saúde financeira e recomendações inteligentes

🛠️ Tecnologias Utilizadas
Área	Tecnologias
Front-end	React + Vite
Estilização	Tailwind CSS
Ícones	Lucide React
Gráficos	Recharts
Back-end & Banco de Dados	Firebase (Firestore + Authentication)
🚀 Como Rodar o Projeto Localmente
✔ Pré-requisitos

Node.js instalado

Conta no Firebase configurada

📥 Instalação
1️⃣ Clone o repositório
git clone https://github.com/SEU-USUARIO/fluxo-hackathon.git
cd fluxo-hackathon

2️⃣ Instale as dependências
npm install

3️⃣ Configure o Firebase

Crie um projeto no Firebase Console

Ative:

Firestore Database (modo teste)

Authentication (Login Anônimo)

Pegue suas chaves de configuração e substitua em:

📌 src/App.jsx → variável firebaseConfig

4️⃣ Execute o projeto
npm run dev

📂 Modelagem de Dados (Entregável Técnico)

A modelagem foi pensada para garantir escalabilidade e clareza.

Tabela de Usuários
CREATE TABLE Users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    risk_profile VARCHAR(50) -- Conservador, Moderado, Arrojado
);

Tabela de Transações
CREATE TABLE Transactions (
    id SERIAL PRIMARY KEY,
    user_id INT REFERENCES Users(id),
    amount DECIMAL(10, 2),
    type VARCHAR(10), -- 'in' ou 'out'
    raw_description VARCHAR(255), -- Descrição original
    clean_description VARCHAR(255), -- Ex: Uber Viagens
    category VARCHAR(50),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

🤝 Contribuições

Contribuições são bem-vindas!
Sinta-se à vontade para abrir issues e pull requests.

📜 Licença

Este projeto está sob a licença MIT.
Sinta-se livre para explorar, modificar e compartilhar.

Se quiser, posso:

✅ Criar uma versão em inglês
✅ Criar o badge de tecnologias para deixar o README mais visual
✅ Criar screenshots falsas (mockups) para valorizar o projeto
✅ Criar um logo simples para o Fluxo