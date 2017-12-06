# AffdexExperiment
Aplicação desenvolvida para o teste de acurácia da ferramenta Affdex para o trabalho de conclusão de curso intitulado 
"Investigação da acurácia de ferramentas de computação afetiva: concepção de arcabouço e análise de uma ferramenta para 
inferência de emoções em expressões faciais."
A aplicação grava vídeos utilizando uma webcam (interna ou externa) de duas formas, com e sem marcações dos pontos fiduciais elencados pelo Affdex.
Além da gravação dos vídeos a aplicação salva em arquivos txt. distintos as pertinências das 7 emoções e 21 expressões faciais suportadas pelo Affdex.

# Pré-Requisitos
* Possuir instalado o SDK Affdex 3.4 (64 bits) em "C:\Program Files (x86)\Affectiva\AffdexSDK\data" - [Download](https://knowledge.affectiva.com/docs/getting-started-with-the-emotion-sdk-for-windows)
* AForge.Video.FFMEG.dll - [Download](http://www.aforgenet.com/framework/downloads.html)
* VisualStudio 2013 ou superior

# Alterações
Modificar os seguintes endereços para os caminhos onde serão salvos os vídeos com pontos fiduciais, videos originais, arquivos de pertinência das emoções e arquivos de pertinência das expressões respectivamente.

Form2.cs
```C#
136  videoWriterPoints.Open("C:\\Users\\joao-\\OneDrive\\UFC\\TCC\\Experimento\\Videos\\" + videoName + "Points.mp4", 640, 480, 15, VideoCodec.MPEG4);
137  videoWriterOriginal.Open("C:\\Users\\joao-\\OneDrive\\UFC\\TCC\\Experimento\\Videos\\" + videoName + "Original.mp4", 640, 480, 15, VideoCodec.MPEG4);
 ---
140  string path0 = @"C:\Users\joao-\OneDrive\UFC\TCC\Experimento\Results\Emotions\" + videoName;
141  string pathex = @"C:\Users\joao-\OneDrive\UFC\TCC\Experimento\Results\Expression\" + videoName;

```
