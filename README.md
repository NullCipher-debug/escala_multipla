Controle de Folga Semanal — 4 Lojas
Gerenciador simples e rápido de escalas semanais para 4 lojas, com controle de folgas, turnos M/T/D e exportação em TXT e PDF. 100% front-end, sem backend, salva automaticamente no navegador.

### [➡️ Acesse a Calculadora Ao Vivo] https://projetos.nullcipher.site/escala/

<img width="694" height="863" alt="Captura de tela 2026-10-12 210611" src="https://github.com/user-attachments/assets/33d1a638-94a6-4d5f-aea5-802b97fe020d" />


Projeto feito em HTML + CSS + JS puro, com tema dark/light e armazenamento em localStorage.

Preview
Abra o arquivo escala.html no navegador — não precisa instalar nada.

✨ Funcionalidades
4 lojas em abas com contador de funcionários por loja
Adicionar funcionário fixo por loja (nome + sobrenome)
Ciclo de horários por clique:
M 6:30 — Manhã
T 13:30 — Tarde
FOLGA — Folga (verde)
D 13:00 — Domingo especial
Semana de referência com input date

Resetar semana para M 6:30 em todos
Remover funcionário com confirmação
Salvar automático no localStorage (escala-dados)
Tema escuro por padrão com toggle para claro (persiste em escala-tema)
Exportação:
TXT — direto, com formato João Silva: Seg M 6:30, Ter T 13:30...
PDF — via jsPDF carregado dinamicamente
Responsivo e com legenda visual de turnos
🧩 Estrutura de dados
Cada loja armazena:

{
  semanaDe: "2025-10-13",
  employees: [
    {
      id: "uuid",
      nome: "João",
      sobrenome: "Silva",
      horarios: ["M 6:30", "M 6:30", "FOLGA", "T 13:30", "M 6:30", "M 6:30", "D 13:00"]
      // index 0-6 = Seg a Dom
    }
  ]
}
localStorage key: escala-dados
DEFAULT_WEEK: M 6:30 todos os dias
🚀 Como usar
Baixe ou clone o repositório
Abra escala.html duplo clique ou Live Server
Selecione a loja no topo
Adicione funcionários fixos
Clique nas células para ciclar o horário
Exporte em TXT ou PDF
Não precisa de npm, build ou servidor.

🎨 Temas
data-theme="dark" (padrão #0b0b0d)
data-theme="light" (#fafaf9)
Toggle com ícones sun/moon, salva em escala-tema
Cores via CSS variables em :root.

📤 Exportação
TXT
Gera arquivo escala-loja-X-YYYY-MM-DD.txt

LOJA 1 - Semana de 13/10/2025
João Silva: Seg M 6:30, Ter M 6:30, Qua FOLGA, Qui T 13:30, Sex M 6:30, Sáb M 6:30, Dom D 13:00
PDF
Carrega jsPDF via CDN sob demanda. Se falhar, mostra status PDF indisponível — usaremos TXT.

Para funcionar offline 100%, você pode embutir o jspdf.umd.min.js inline ou trocar por geração de PDF manual.

🛠️ Tecnologias
HTML5 semântico
CSS puro com variables, sem frameworks
JavaScript vanilla (IIFE)
localStorage para persistência
jsPDF para PDF
📁 Estrutura sugerida para o GitHub
/
├── escala.html   # app principal (single file)
├── README.md     # este arquivo
└── LICENSE       # opcional
Se quiser separar em arquivos:

/
├── index.html
├── css/style.css
├── js/app.js
└── README.md
🔧 Melhorias futuras
 Editar nome do funcionário
 Duplicar semana
 Contador de folgas por funcionário
 Validação de 1 folga obrigatória
 Importar CSV
 PWA para instalar no celular
 PDF offline sem CDN
👤 Autor
Cipher_Arthur

Feito para controle rápido de escala de 4 lojas.

📝 Licença
MIT — livre para usar e modificar.
