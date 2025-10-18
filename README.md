# 🔐 Login Bitrix PBKDF2

Um login simples em HTML/CSS/JS com validação local (no navegador) e **criptografia PBKDF2** via [Web Crypto API].  
Após a validação bem-sucedida, o script carrega dinamicamente o formulário Bitrix24.

> ⚠️ Este projeto é apenas para fins de demonstração ou uso interno (ambiente local).  
> Não utilize este método de autenticação em produção — toda a lógica e os hashes ficam expostos no cliente.

---

## 🚀 Funcionalidades

- Interface de login responsiva e minimalista  
- IDs e senhas armazenadas de forma **criptografada** (PBKDF2 + Salt)  
- Validação de credenciais diretamente no browser  
- Execução controlada de um script Bitrix apenas após o login válido  
- Função embutida para gerar novos usuários (hash + salt)

---

## 🧠 Como funciona

1. O usuário digita o **ID da empresa** e a **senha**.  
2. O JavaScript usa `crypto.subtle` (Web Crypto API) para gerar um **hash PBKDF2** com base na senha digitada e no salt do ID.  
3. O hash gerado é comparado com o hash armazenado.  
4. Se coincidir → login aceito → o script Bitrix é executado.  
5. Caso contrário → mensagem de erro exibida.

---

## 🧰 Tecnologias

- **HTML5 / CSS3**
- **JavaScript puro (Vanilla JS)**
- **Web Crypto API (PBKDF2 / SHA-256)**
- **Bitrix24 Embedded Form**

---

## ⚙️ Uso

1. Clone o repositório:
   ```bash
   git clone https://github.com/seuusuario/login-bitrix-pbkdf2.git
   cd login-bitrix-pbkdf2
