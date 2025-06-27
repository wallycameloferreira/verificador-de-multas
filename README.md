# 🚗 Verificador de Infrações de Trânsito x Locações
Este projeto é uma ferramenta gráfica feita em Python que compara automaticamente planilhas de infrações de trânsito com registros de locações de veículos, identificando qual cliente estava com o veículo no momento da infração.

Ideal para empresas de locação de veículos que precisam identificar o responsável por uma infração registrada em determinado dia e hora.

🛠 Tecnologias Utilizadas
Python 3.10+

Pandas para manipulação de dados

Tkinter para a interface gráfica

OpenPyXL para exportação para Excel (via pandas)

📥 Instalação
Clone o repositório:

bash
Copiar
Editar
git clone https://github.com/wallycameloferreira/verificador-de-multas.git
cd nome-do-repo
Instale as dependências necessárias:

bash
Copiar
Editar
pip install pandas openpyxl
Execute o sistema:

bash
Copiar
Editar
python app.py
Substitua app.py pelo nome do seu arquivo, se for diferente.

🧾 Requisitos das Planilhas
📄 Planilha de Locações (Exemplo: locacoes.xlsx)
Deve conter os seguintes campos (nomes exatos e sem acentos):

Copiar
Editar
agendamento_id, retirada_real, devolucao_real, preco_previsto,
situacao, status_pagamento, base_veiculo, modelo_veiculo,
placa, nome_cliente, cpf_cnpj
📄 Planilha de Infrações (Exemplo: infracoes.xlsx)
Deve conter os campos:

objectivec
Copiar
Editar
PLACA, AUTO, DATA DA INFRAÇÃO, HORA, CLIENTE
🧠 Como Funciona
O usuário importa as duas planilhas pelo sistema.

O programa cruza as informações com base na placa e no período de uso.

Verifica se a infração ocorreu dentro do intervalo de retirada e devolução do veículo.

Exibe o resultado na tela e permite a exportação em Excel.

✅ Exemplo de Saída
csharp
Copiar
Editar
[OK] QWE9A11 2024-03-10 15:30:00 estava com João da Silva.
[ERRO] Sem cliente para ABC1B23 2024-03-11 12:45:00.
📤 Exportação
O resultado da verificação pode ser salvo em um novo arquivo .xlsx com os seguintes campos:

PLACA

AUTO

DATA DA INFRAÇÃO

HORA

CLIENTE (original)

NOME DO CLIENTE (identificado)

📸 Interface do Sistema
Interface construída com Tkinter para facilitar o uso sem necessidade de terminal.

💡 Possíveis Melhorias Futuras
Leitura de arquivos .csv além de .xlsx

Detecção de conflitos com múltiplas locações simultâneas

Suporte para filtros por base de veículo ou datas

Versão web com Flask/Django

🧑‍💻 Autor
Desenvolvido por wally camelo ferreira  
