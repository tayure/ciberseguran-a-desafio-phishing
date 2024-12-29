# ciberseguran-a-desafio-phishin

# Ferramentas:
- Kali Linux
- kit de ferramentas de configuração

# Configurando o Phishing no Kali Linux
- Acesso root:sudo su
- Iniciando o setoolkit:setoolkit
- Tipo de ataque:Social-Engineering Attacks
- Vetor de ataque:Web Site Attack Vectors
- Método de ataque:Credential Harvester Attack Method
- Método de ataque:Site Cloner
- Obtendo o endereço da máquina:ifconfig
- URL para clonar: http://www.facebook.com

# Porém, o meu resultado foi diferente do esperado, segue o anexo:
![teste](https://github.com/user-attachments/assets/a0143a03-3741-4f5f-8707-796e96749b73)

Tendo em vista que alguns sites enviam as credenciais em requisições assíncronas (AJAX) após o envio do formulário,
resolvi usar o Burp Suite para ver se o caso era realmente esse:
![Burp Suite](https://github.com/user-attachments/assets/f9b81341-4f28-4b37-a961-52f8f2c9c3cb)

# O Problema com Requisições AJAX
- O que acontece: Quando o usuário insere o login e a senha e clica em "Entrar",
o site pode enviar esses dados em uma requisição separada (via JavaScript), que não passa pelo formulário diretamente.
- Impacto: O SEToolkit captura apenas os dados iniciais, mas a requisição AJAX subsequente com as credenciais pode não
ser interceptada pelo ataque de clonagem padrão.



