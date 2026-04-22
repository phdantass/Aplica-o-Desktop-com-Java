# 💻 Aplicação Desktop com Java + JavaFX + HTML/CSS/JS

Este projeto demonstra como criar uma aplicação desktop utilizando Java e JavaFX, integrando uma interface moderna desenvolvida com HTML, CSS e JavaScript através do componente WebView.

---

# 🚀 Tecnologias Utilizadas

| Tecnologia  | Versão                |
| ----------- | --------------------- |
| Java        | JDK 17                |
| JavaFX      | 21                    |
| Eclipse IDE | 2024-06 (ou superior) |
| HTML/CSS/JS | Padrão Web            |

---

# 📥 Downloads Necessários

## ☕ Java (JDK 17)

🔗 Download:
[https://adoptium.net/](https://adoptium.net/pt-BR/temurin/releases?version=17&os=any&arch=any&mode=filter)

📌 Passos:

1. Acesse o site
2. Clique em **Latest LTS → JDK 17**
3. Baixe o instalador `.msi`
4. Instale normalmente

<img width="1351" height="645" alt="image" src="https://github.com/user-attachments/assets/a57979db-b1e1-4c79-9af7-06ed85f42da8" />

---

## 🎨 JavaFX SDK (21)

🔗 Download:
[https://gluonhq.com/products/javafx/](https://www.oracle.com/java/technologies/downloads/javafx/#javafx26-linux)

📌 Passos:

1. Acesse o site
2. Clique em **Download JavaFX**
3. Escolha:

   * Windows
   * JavaFX 21
4. Extraia o arquivo

📁 Coloque em:

```id="4r1y47"
C:\javafx
```

<img width="1294" height="366" alt="image" src="https://github.com/user-attachments/assets/2a34750e-ee71-4212-a794-89fff5810889" />


---

## 💻 Eclipse IDE

🔗 Download:
https://www.eclipse.org/downloads/

📌 Passos:

1. Baixe o **Eclipse Installer**
2. Abra o instalador
3. Clique em:

👉 **Eclipse IDE for Java Developers**

4. Clique em Install

<img width="1350" height="540" alt="image" src="https://github.com/user-attachments/assets/d749cc2f-8ace-4298-84da-89ba2a5404b1" />


---

# ⚙️ Configuração no Eclipse

## 📌 Criar Projeto

1. File → New → Java Project

<img width="702" height="497" alt="image" src="https://github.com/user-attachments/assets/6d6b3be6-50b2-4057-958c-e03b450edd86" />

---

## 📌 Adicionar JavaFX

1. Botão direito no projeto
2. Build Path → Configure Build Path
3. Aba Libraries
4. Clique em **Add External JARs**
5. Selecione TODOS os arquivos de:

```id="1lmn4l"
C:\javafx\lib
```

<img width="597" height="551" alt="image" src="https://github.com/user-attachments/assets/efdf6cbe-a670-48d8-bd23-20813d63ff1d" />

---

## 📌 Configurar VM Options (ESSENCIAL)

1. Run → Run Configurations
2. Aba Arguments
3. Em **VM arguments**, adicione:

```id="6hlsaf"
--module-path C:\javafx\lib --add-modules javafx.controls,javafx.web
```


---

# 📁 Estrutura do Projeto

```id="f43wjr"
src/
 └── meuapp/
      ├── Main.java
      ├── index.html
      ├── style.css
      └── script.js
```

📌 IMPORTANTE:

* O `index.html` deve estar no mesmo pacote do `Main.java`

---

# ☕ Código Principal

```java id="n1rtqz"
WebView webView = new WebView();

webView.getEngine().load(
    getClass().getResource("index.html").toExternalForm()
);
```

---

# ❗ Problemas Comuns

## 🔴 Erro: getResource(...) retorna null

👉 Causa:
Arquivo HTML fora do lugar

👉 Solução:
Colocar dentro do mesmo pacote do Main

---

## 🔴 Erro: JavaFX runtime components are missing

👉 Solução:
Verificar VM Options

---

## 🔴 Eclipse não atualiza arquivos

👉 Solução:

* F5 (Refresh)
* Project → Clean

---

# 📸 Prints do Projeto

💡 Recomenda-se adicionar:

* Tela do Eclipse com projeto aberto
* Estrutura de pastas
* Aplicação rodando

Você pode tirar prints com:

* Windows: `Win + Shift + S`

---

# 💡 Observações

* Projeto desktop (não usa Tomcat/Servlet)
* JavaFX funciona como ponte entre Java e HTML
* Pode ser expandido com banco de dados (MySQL)

---

# 📌 Conclusão

Este projeto demonstra como integrar tecnologias web dentro de aplicações desktop Java de forma simples e eficiente.

---

# 👨‍💻 Autor

Projeto desenvolvido para fins educacionais.
