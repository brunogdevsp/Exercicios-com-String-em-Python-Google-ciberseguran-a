# 🛡️ Exercícios de Python - Curso de Cibersegurança (Google + CIEE + Coursera)

Este repositório contém 10 exercícios práticos desenvolvidos em Python como parte do curso de **Cibersegurança** oferecido pelo **Google**, em parceria com o **CIEE** e a **Coursera**. Os exercícios abordam fundamentos essenciais de manipulação de strings, variáveis e estruturas condicionais — habilidades cruciais para profissionais de segurança digital e ciência de dados.

---

## 📚 Lista de Exercícios

| Tarefa | Tema | Descrição |
|-------|------|-----------|
| Task 1 | Conversão de tipo | Converte um ID numérico para string |
| Task 2 | Validação de formato | Verifica se o ID possui 5 dígitos |
| Task 3 | Padronização | Adiciona prefixo para padronizar IDs curtos |
| Task 4 | Extração de caractere | Extrai o 4º caractere de um ID de dispositivo |
| Task 5 | Fatiamento de string | Extrai os 3 primeiros caracteres de um ID |
| Task 6 | Protocolo de URL | Extrai o protocolo (https://) de uma URL |
| Task 7 | Localização de extensão | Localiza o índice de ".com" em uma URL |
| Task 8 | Armazenamento de índice | Salva o índice de ".com" em uma variável |
| Task 9 | Extração de extensão | Extrai ".com" usando fatiamento baseado no índice |
| Task 10 | Extração de nome do site | Extrai o nome do site entre protocolo e extensão |

---

## 🧠 Por que esses exercícios são importantes?

### 🔐 Cibersegurança
- Identificação de padrões em URLs e IDs é essencial para detectar ameaças, phishing e domínios maliciosos.
- Padronização de identificadores evita falhas em sistemas de autenticação e controle de acesso.

### 📊 Ciência de Dados
- Manipulação de strings permite categorizar, agrupar e enriquecer dados com base em fontes e padrões.
- Extração de componentes de URLs é útil para análise de tráfego, segmentação e validação de dados.

# Exercício: Conversão de ID de funcionário para string

# Atribui um número de 4 dígitos à variável 'employee_id'
employee_id = 4186
# Exibe o tipo de dado atual da variável (deve ser 'int')
print("Tipo antes da conversão:", type(employee_id))
# Converte o número para string e reatribui à mesma variável
employee_id = str(employee_id)
# Exibe o tipo de dado após a conversão (deve ser 'str')
print("Tipo após a conversão:", type(employee_id))



# Exercício: Verificar se o ID do funcionário atende ao novo padrão de 5 dígitos
# Atribui um número de 4 dígitos à variável 'employee_id'
employee_id = 4186
# Converte o número para string para facilitar a verificação de comprimento
employee_id = str(employee_id)
# Verifica se o ID possui menos de 5 dígitos
if len(employee_id) < 5:
    print("Este ID de funcionário possui menos de cinco dígitos e não atende aos requisitos de padronização.")



# Exercício: Atualizar o ID do funcionário para o novo padrão de 5 caracteres
# Atribui um número de 4 dígitos à variável 'employee_id'
employee_id = 4186
# Converte o número para string para facilitar manipulação e verificação
employee_id = str(employee_id)
# Exibe o ID atual
print("ID original:", employee_id)
# Verifica se o ID possui menos de 5 caracteres
# Se sim, concatena a letra "E" no início para padronizar
if len(employee_id) < 5:
    employee_id = "E" + employee_id
# Exibe o ID atualizado
print("ID padronizado:", employee_id)



# Exercício: Extração de caractere específico de um ID de dispositivo
# Atribui um ID de dispositivo alfanumérico à variável 'device_id'
device_id = "r262c36"
# Extrai o quarto caractere (índice 3, pois a contagem começa em 0)
# Isso pode representar uma informação técnica específica do dispositivo
print("Quarto caractere do device_id:", device_id[3])



# Exercício: Extração de fatia de caracteres de um ID de dispositivo
# Atribui um ID de dispositivo alfanumérico à variável 'device_id'
device_id = "r262c36"
# Extrai os três primeiros caracteres (índices 0, 1 e 2)
# A notação [0:3] inclui o índice 0 e vai até o índice 2 (o 3 é exclusivo)
prefixo = device_id[0:3]
# Exibe o resultado da fatia extraída
print("Primeiros três caracteres do device_id:", prefixo)


# Exercício: Extração do protocolo de uma URL
# Atribui uma URL à variável 'url'
url = "https://exampleURL1.com"
# Extrai os primeiros 8 caracteres da URL, que correspondem ao protocolo "https://"
# Isso é útil para identificar o tipo de conexão (segura ou não)
print("Protocolo da URL:", url[0:8])



# Exercício: Localizar o índice da extensão de domínio ".com" em uma URL
# Atribui uma URL à variável 'url'
url = "https://exampleURL1.com"
# Utiliza o método .index() para encontrar a posição inicial da extensão ".com"
# Isso é útil para extrair partes específicas da URL, como o domínio
print("Índice onde começa '.com':", url.index(".com"))



# Exercício: Armazenar o índice da extensão de domínio ".com" em uma variável
# Atribui uma URL à variável 'url'
url = "https://exampleURL1.com"
# Utiliza o método .index() para encontrar a posição inicial da extensão ".com"
# Armazena esse valor na variável 'ind' para facilitar rastreamento e reutilização
ind = url.index(".com")
# Este código não gera saída visível, mas 'ind' agora contém o índice onde ".com" começa


# Exercício: Extração da extensão de domínio ".com" usando fatiamento de string
# Atribui uma URL à variável 'url'
url = "https://exampleURL1.com"
# Localiza o índice onde começa a extensão ".com"
ind = url.index(".com")
# Utiliza fatiamento para extrair os 4 caracteres da extensão, começando em 'ind'
# Isso resulta em ".com"
print("Extensão de domínio extraída:", url[ind:ind+4])



# Exercício: Extração do nome do site a partir da URL
# Atribui uma URL à variável 'url'
url = "https://exampleURL1.com"
# Localiza o índice onde começa a extensão ".com"
ind = url.index(".com")
# Utiliza fatiamento para extrair o nome do site entre o protocolo (índice 8) e o início de ".com"
# Isso resulta em "exampleURL1"
print("Nome do site extraído da URL:", url[8:ind])
