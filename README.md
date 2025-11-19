<p align="center">
  <img src="Capa.png" alt="Capa Personalizada" width="1000" />
</p>

# GitHub - Luiza Matos 👩‍💻
Seja bem-vindo(a) ao meu GitHub! Aqui você encontra minha trajetória, experiências e projetos desenvolvidos ao longo do caminho. 🚀

---
## 👤 Sobre Mim
- 🎓 Graduanda em **Análise e Desenvolvimento de Sistemas** pela [Newton Paiva](https://www.newtonpaiva.br/).
- 🗣️ Idiomas: **Português (nativo)** | **Inglês (técnico)**.
- ⚽ Hobbies: Futebol, quebra-cabeças e passeios.
- 💼 Objetivo profissional: Atuar com **Desenvolvimento de Sistemas** ou **Análise de Dados**.
- 📚 Atualmente estudando: **Java, JavaScript, HTML, CSS, SQL, Python e Power BI**.

---
## 🚀 Ferramentas & Tecnologias  

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![VSCode](https://img.shields.io/badge/VSCode-0078d7?style=for-the-badge&logo=visualstudiocode&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![Trello](https://img.shields.io/badge/Trello-0052CC?style=for-the-badge&logo=trello&logoColor=white)
![AutoCAD](https://img.shields.io/badge/AutoCAD-E51050?style=for-the-badge&logo=autodesk&logoColor=white)

---
## Contato
- 🔗LinkedIn: www.linkedin.com/in/luizamatos/
- 📩Email: luizamatoscontatos@gmail.com
- 🛜Site: https://lubmatos.github.io/Site/

---
![Contador de visitas](https://komarev.com/ghpvc/?username=Lubmatos&color=blue&style=for-the-badge)


```bash
// Projeto: Fechamento automático de janela com sensor de chuva
// Hardware: Arduino Nano + Relé 5V + Transistor + Sensor YL-38/39 + Fim de curso

int sensorChuva = A0;     // Entrada analógica do sensor de chuva
int rele = 2;             // Pino que aciona o transistor e o relé
int fimCurso = 3;         // Sensor de fim de curso

int limiteChuva = 400;    // Threshold para detectar chuva

void setup() {
  pinMode(rele, OUTPUT);
  pinMode(fimCurso, INPUT_PULLUP);
  digitalWrite(rele, LOW);

  Serial.begin(9600);
}

void loop() {

  int valorChuva = analogRead(sensorChuva);
  int estadoFimCurso = digitalRead(fimCurso);

  Serial.print("Sensor = ");
  Serial.println(valorChuva);

  // Se detectar chuva e a janela ainda não estiver totalmente fechada
  if (valorChuva < limiteChuva && estadoFimCurso == HIGH) {
    digitalWrite(rele, HIGH);   // Aciona o motor
  } 
  else {
    digitalWrite(rele, LOW);    // Desliga o motor
  }

  delay(200);
}
```

