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
https://adoptium.net/

📌 Passos:

1. Acesse o site
2. Clique em **Latest LTS → JDK 17**
3. Baixe o instalador `.msi`
4. Instale normalmente

🖼️ Exemplo visual:
https://adoptium.net/images/installation.png

---

## 🎨 JavaFX SDK (21)

🔗 Download:
https://gluonhq.com/products/javafx/

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

🖼️ Exemplo visual:
https://gluonhq.com/wp-content/uploads/2020/02/javafx-download.png

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

🖼️ Exemplo visual:
https://www.eclipse.org/downloads/images/installer.png

---

# ⚙️ Configuração no Eclipse

## 📌 Criar Projeto

1. File → New → Java Project

🖼️
https://help.eclipse.org/latest/topic/org.eclipse.jdt.doc.user/images/ngj_newprj_wiz.png

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

🖼️
https://i.stack.imgur.com/1V7Zl.png

---

## 📌 Configurar VM Options (ESSENCIAL)

1. Run → Run Configurations
2. Aba Arguments
3. Em **VM arguments**, adicione:

```id="6hlsaf"
--module-path C:\javafx\lib --add-modules javafx.controls,javafx.web
```

🖼️
https://i.stack.imgur.com/6RZ4n.png

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
