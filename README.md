# Tech-Challenge-Fase4-FIAP

Processamento de Vídeo para Detecção de Emoções e Ações

### Como Rodar o Código no Jupyter Notebook (.ipynb) ou Google Colab ###

Para executar o código no Jupyter Notebook ou Google Colab e analisar os vídeos gerando um relatório, siga os passos abaixo:

1. Configuração do Ambiente

Antes de rodar o código, certifique-se de que as bibliotecas necessárias estão instaladas. Caso contrário, instale-as executando o seguinte comando no notebook ou Colab:

!pip install opencv-python numpy mediapipe tqdm deepface

2. Carregar o Notebook e Definir os Caminhos

No Jupyter Notebook ou Colab, certifique-se de que o arquivo de vídeo que deseja analisar está no caminho correto.

Altere a variável VIDEO_PATH no código para apontar para o arquivo correto.

Se necessário, altere OUTPUT_VIDEO_PATH para definir onde o vídeo processado será salvo.

O relatório gerado será salvo no caminho definido pela variável REPORT_PATH.

3. Executar o Código

Execute todas as células do notebook.

O código processará o vídeo frame a frame, detectando emoções e ações.

O vídeo processado será salvo no diretório indicado e um relatório será gerado no formato .txt.

4. Acessar os Resultados

O vídeo resultante conterá sobreposições com as emoções e ações detectadas.

O relatório relatorio_video.txt conterá a contagem de frames onde cada emoção e ação foi identificada.

### Objetivo do Código ###

O código foi desenvolvido para contar a quantidade de frames em que cada emoção e ação foi detectada, em vez de contar apenas quantas vezes uma nova emoção ou ação apareceu.

Isso significa que:

Se uma pessoa estiver "dançando" por 50 frames, todos esses 50 frames serão contados na distribuição de ações.

Se a emoção "feliz" for detectada em 100 frames, essa será a contagem final.

O objetivo é ter uma visão quantitativa das emoções e ações ao longo do vídeo.

### Limitações e Melhorias Futuras ###

-Limitações

Precisão Limitada: O código usa heurísticas simples para identificar ações, o que pode resultar em erros para movimentos mais sutis.

Variação de Iluminação e Qualidade do Vídeo: Emoções podem ser mal interpretadas dependendo da iluminação e da resolução.

Detecção de Emoções: O modelo de detecção de emoções pode apresentar limitações dependendo da diversidade dos rostos no vídeo.

-Melhorias Futuras

Uso de Machine Learning: Para maior precisão, seria ideal utilizar modelos de aprendizado profundo treinados especificamente para reconhecimento de ações humanas.

Aprimorar Regras: Ajustar os limiares de detecção de movimento para melhorar a precisão na identificação de ações.

Integração com Modelos Avançados: Utilizar redes neurais como LSTMs ou Vision Transformers para melhorar a classificação de ações dinâmicas.

### Conclusão ###

Este código permite analisar vídeos com base em emoções e movimentos. No entanto, as detecções no vídeo não ficaram perfeitas, pois foram baseadas em heurísticas simples e métodos básicos. Com mais tempo e desenvolvimento, seria possível aprimorar bastante os resultados e tornar o sistema mais preciso com técnicas avançadas de IA. No momento, a intenção principal é demonstrar como é possível realizar uma análise de sentimentos e ações em vídeos, servindo como um ponto de partida para projetos mais avançados nessa área.
