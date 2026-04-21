# 💻 Aplicação Desktop com Java + JavaFX + HTML/CSS/JS

Este projeto demonstra como criar uma aplicação desktop utilizando Java com JavaFX, integrando uma interface desenvolvida com HTML, CSS e JavaScript.

A ideia principal é utilizar o componente `WebView` do JavaFX para renderizar páginas web dentro de uma aplicação Java, permitindo unir o poder do Java com a flexibilidade do front-end web.

---

# 🚀 Tecnologias utilizadas

* ☕ Java JDK 17+
* 🎨 JavaFX SDK
* 💻 Eclipse IDE
* 🌐 HTML, CSS e JavaScript

---

# 📥 Instalações necessárias

## 1. Java (JDK)

Para executar o projeto, é necessário ter o Java instalado.

👉 Download:
https://adoptium.net/

Passos:

1. Baixar o **Temurin JDK 17**
2. Instalar normalmente (Next → Next → Finish)
3. Marcar:

   * Add to PATH
   * Set JAVA_HOME

Verificação:

```bash
java -version
```

---

## 2. JavaFX SDK

O JavaFX não vem incluso no Java moderno, então precisamos baixar separadamente.

👉 Download:
https://gluonhq.com/products/javafx/

Passos:

1. Baixar o JavaFX SDK (versão compatível com seu Java)
2. Extrair o arquivo .zip
3. Salvar em um diretório fixo, exemplo:

```
C:\javafx
```

---

## 3. Eclipse IDE

👉 Download:
https://www.eclipse.org/downloads/

Utilizado para desenvolvimento e execução do projeto.

---

# ⚙️ Configuração do projeto

## 1. Criar projeto Java

No Eclipse:

* File → New → Java Project

---

## 2. Adicionar JavaFX ao projeto

1. Botão direito no projeto → Build Path → Configure Build Path
2. Aba Libraries → Add External JARs
3. Selecionar todos os arquivos dentro de:

```
C:\javafx\lib
```

---

## 3. Configurar VM Options (IMPORTANTE)

Run → Run Configurations → Arguments

Adicionar:

```
--module-path C:\javafx\lib --add-modules javafx.controls,javafx.web
```

---

# 📁 Estrutura do projeto

```
src/
 └── meuapp/
      ├── Main.java
      ├── index.html
      ├── style.css
      └── script.js
```

---

# ☕ Código principal (Java)

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.web.WebView;
import javafx.stage.Stage;

public class Main extends Application {

    @Override
    public void start(Stage stage) {

        WebView webView = new WebView();

        webView.getEngine().load(
            getClass().getResource("index.html").toExternalForm()
        );

        Scene scene = new Scene(webView, 800, 600);

        stage.setTitle("Meu App Desktop");
        stage.setMaximized(true);
        stage.setScene(scene);
        stage.show();
    }

    public static void main(String[] args) {
        launch();
    }
}
```

---

# 🌐 Interface (HTML)

```html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<h1>Meu App Desktop 🚀</h1>
<button onclick="clicar()">Clique aqui</button>

<script src="script.js"></script>
</body>
</html>
```

---

# 🎨 Estilo (CSS)

```css
body {
    font-family: Arial;
    text-align: center;
    margin-top: 50px;
}
```

---

# ⚡ Script (JavaScript)

```javascript
function clicar() {
    alert("Funcionando dentro do Java 😎");
}
```

---

# ❗ Problemas comuns e soluções

### 🔴 Erro: getResource(...) retorna null

Causa:

* Arquivo HTML fora da pasta correta

Solução:

* Garantir que o `index.html` esteja dentro do mesmo pacote do `Main.java`

---

### 🔴 Erro: JavaFX runtime components are missing

Solução:

* Verificar VM Options

---

### 🔴 Arquivos não atualizam no Eclipse

Solução:

* Clicar com botão direito → Refresh (F5)
* Project → Clean

---

# 💡 Observações importantes

* Este projeto é desktop, não utiliza Servlet ou Tomcat
* O JavaFX atua como "ponte" entre Java e HTML
* É possível integrar com banco de dados futuramente (MySQL, por exemplo)

---

# 📌 Conclusão

Este projeto demonstra uma forma simples e eficiente de criar aplicações desktop modernas utilizando tecnologias web dentro do Java.

---

# 👨‍💻 Autor

Pedro Henrique Dantas Silva
