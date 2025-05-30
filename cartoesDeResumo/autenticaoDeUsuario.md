# 🔑 Autenticação de Usuários no MySQL  

## 👤 Como MySQL Autentica Usuários  
No MySQL, os usuários são autenticados por meio de **contas armazenadas em um banco de dados do sistema**.  
A autenticação usa **três elementos principais**:  
1️⃣ **Nome de usuário** (username)  
2️⃣ **Nome do host** (hostname)  
3️⃣ **Senha** (password)  

🔍 **Exemplo lúdico:** Imagine um **clube exclusivo** 🎟️ – só entra quem tem um nome na lista, vindo de um local permitido e com uma senha correta!  

👨‍💻 **Exemplo prático:** Em um sistema corporativo, cada funcionário recebe um login MySQL que permite acesso apenas de computadores internos da empresa.  

---

## 🌍 Identificador da Conta  
O identificador contém:  
✅ **Nome do usuário** – Identifica quem está acessando.  
✅ **Host** – Define de onde o usuário pode se conectar (DNS ou IP).  

🔍 **Exemplo lúdico:** Como uma **lista VIP de convidados** 🥂 – só pode entrar quem estiver na lista e no local certo!  

👨‍💻 **Exemplo prático:** Um banco de dados pode permitir que usuários internos acessem apenas via VPN corporativa, bloqueando acessos externos.  

---

## 🎭 Wildcards e Permissões de Acesso  
Wildcards (`%`) podem ser usados para permitir conexões de **vários hosts**.  

🔍 **Exemplo lúdico:** Como uma **chave mestra** 🔑 – pode abrir várias portas sem precisar de uma chave específica para cada.  

👨‍💻 **Exemplo prático:** Em um sistema distribuído, um administrador pode configurar um usuário MySQL que pode acessar o banco de qualquer servidor na rede.  

---

## 🛠️ Criando um Usuário  
O comando `CREATE USER` cria um novo usuário no MySQL.  

🔹 **Exemplo:**  
```sql
CREATE USER 'test'@'%' IDENTIFIED BY 'senhaSegura';