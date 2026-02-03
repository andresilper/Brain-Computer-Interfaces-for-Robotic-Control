Utilização de Sinais Eletroencefalográficos (EEG) para Controle Robótico

---
Este projeto investiga o uso de métricas de conectividade cerebral funcional (PDC e DTF) para superar o desafio de distinguir movimentos realizados com o mesmo segmento corporal (ex: flexão e extensão do cotovelo) através de sinais de EEG.

---
# Visão Geral

A classificação de atividades motoras no mesmo membro é um desafio complexo porque essas tarefas ativam regiões com representações espaciais muito próximas no córtex motor. Enquanto métodos tradicionais baseados em energia (ERD/ERS) permitem detectar a realização de alguma tarefa cognitiva sendo realizada, a análise de conectividade permite mapear a direção e intensidade do fluxo de informação entre áreas corticais, proporcionando maior precisão na distinção dos comandos motores.

---
# Principais Características
#### • Métricas de Conectividade: Implementação de Coerência Direcionada Parcial (PDC) e Função de Transferência Direcionada (DTF) baseadas em modelos multivariados autorregressivos (MVAR).
#### • Causalidade de Granger: Avaliação de relações causais no domínio da frequência para identificar influências diretas entre canais de EEG.
#### • Classificadores de Alta Performance: Uso de Redes Neurais Artificiais (MLP) e Análise de Discriminante Linear (LDA) para categorizar 7 classes de tarefas (movimento, imaginação, observação e repouso).
---

# Metodologia
O pipeline de processamento segue estas etapas fundamentais:
1. Aquisição de Sinais: Registro via sistema de 19 ou 32 eletrodos (Sistema 10/20) focado nas áreas frontais, centrais e parietais.
2. Pré-processamento: Filtragem passa-faixa (ex: 0,5 a 40 Hz) e remoção seletiva de artefatos biológicos.
3. Estimação de Conectividade: Cálculo da gPDC (PDC Generalizada) ou DTF para extrair características compactas (média, desvio padrão e centroide espectral).
4. Treinamento e Validação: Classificação síncrona (online e offline) com foco nos ritmos Beta e Gama, que apresentam maior separabilidade para estas tarefas.
---

# Resultados de Classificação

A tarefa de classificação, neste caso, significa aplicar um algoritmo de aprendizado de máquina que consiga determinar se um determinado sinal de EEG veio de um movimento de extensão ou de flexão do mesmo braço, que é uma tarefa tradicionalmente mais difícil do que classificar entre movimento e imaginação.

| Critério | Offline | Online |
|-------------|-----------|----------|
| **Acurácia** |  80-90% |  39-40% |
| **Melhor** |  90% |   58% |
| **Sensibilidade** |  Homogênea | Heterogênea |

--- 

## Interação Humano-Robô
O sistema será validado através do controle de um manipulador robótico, que está sendo construído e irá atuar como realimentação visual para o usuário, mimetizando os movimentos de flexão e extensão imaginados.



---
### Artigos de Periódicos e Conferências
    ◦ KAUATI-SAITO, Eric et al. Classification of Different Motor Imagery Tasks with the Same Limb Using Electroencephalographic Signals. Sensors, v. 25, 2025.    
    ◦ MOHAMMAD, Awwab et al. Feature Extraction from EEG Signals: A deep learning perspective. 2021 11th International Conference on Cloud Computing, Data Science & Engineering (Confluence), 2021.
    ◦ PÉREZ-VELASCO, Sergio et al. Bridging motor execution and motor imagery BCI paradigms: An inter-task transfer learning approach. Biomedical Signal Processing and Control, v. 107, 107834, 2025.
    ◦ SAHA, Simanto et al. Progress in Brain Computer Interface: Challenges and Opportunities. Frontiers in Systems Neuroscience, v. 15, 578875, 2021.
    ◦ SANTOS-COUTO-PAZ, Clarissa C. et al. The addition of functional task-oriented mental practice to conventional physical therapy improves motor skills in daily functions after stroke. Brazilian Journal of Physical Therapy, v. 17, n. 6, p. 564-571, 2013.
    ◦ SANTOS-CUEVAS, Diana Carolina et al. Effective brain connectivity related to non-painful thermal stimuli using EEG. IOP Publishing Ltd, 2024.
    ◦ WANG, Hewei et al. Motor network reorganization after motor imagery training in stroke patients with moderate to severe upper limb impairment. CNS Neuroscience & Therapeutics, v. 29, p. 619-632, 2023.
    ◦ WANG, Hewei et al. The Reorganization of Resting-State Brain Networks Associated With Motor Imagery Training in Chronic Stroke Patients. IEEE Transactions on Neural Systems and Rehabilitation Engineering, v. 27, n. 10, p. 2237-2245, 2019.
    ◦ ZHAO, Li Juan et al. Effects of Motor Imagery Training for Lower Limb Dysfunction in Patients With Stroke: A Systematic Review and Meta-analysis of Randomized Controlled Trials. American Journal of Physical Medicine & Rehabilitation, v. 102, n. 5, p. 409-418, 2023.
    ◦ MIZUGUCHI, Nobuaki et al. Brain activity during motor imagery of an action with an object: A functional magnetic resonance imaging study. Neuroscience Research, v. 76, p. 150-155, 2013.

---
### Teses e Dissertações
    ◦ MASSOTE, Mariana Aguiar. Avaliação do efeito da estimulação magnética transcraniana nos sinais de eletroencefalograma usando o teste F espectral e a função de coerência. 2018. Dissertação (Mestrado em Engenharia Biomédica) – COPPE, Universidade Federal do Rio de Janeiro, Rio de Janeiro, 2018.
    ◦ PEREIRA, André da Silva. Análise de ritmos cerebrais durante imaginação e execução de movimento do membro superior com e sem interação humano-robô. 2022. Dissertação (Mestrado em Engenharia Biomédica) – COPPE, Universidade Federal do Rio de Janeiro, Rio de Janeiro, 2022.
    ◦ SAITO, Éric Kauati. Conectividade cerebral para o controle online de interfaces cérebro-máquina. 2019. Dissertação (Mestrado em Engenharia Biomédica) – COPPE, Universidade Federal do Rio de Janeiro, Rio de Janeiro, 2019.
    ◦ SILVA, Alexsandro de Souza Teixeira da. Estudo da conectividade funcional cerebral em sinais de EEG durante interação humano robô. 2016. Dissertação (Mestrado em Engenharia Biomédica) – COPPE, Universidade Federal do Rio de Janeiro, Rio de Janeiro, 2016.
    ◦ SILVA, Lucas Coutinho Pereira da. Análise de sinais de EEG após reabilitação com imagética motora em indivíduos pós-AVC. 2018. Dissertação (Mestrado em Engenharia Biomédica) – COPPE, Universidade Federal do Rio de Janeiro, Rio de Janeiro, 2018.
    ◦ SILVEIRA, Gustavo Fraga Millen da. Conectividade cerebral como característica para classificar tarefas motoras de mesmo segmento corporal: interação humano-robô. 2017. Dissertação (Mestrado em Engenharia Biomédica) – COPPE, Universidade Federal do Rio de Janeiro, Rio de Janeiro, 2017.
    ◦ ULLOA, Ernesto Pablo Lana. Estudo sobre interfaces cérebro-máquina e interação humano-robô. 2013. Dissertação (Mestrado em Engenharia Elétrica) – Escola de Engenharia da Universidade Federal de Minas Gerais, Belo Horizonte, 2013.
---
### Vídeos e Mídias Digitais
    ◦ A BRAIN Implant That Turns Your Thoughts Into Text | Tom Oxley. TED, 2022. Disponível em: https://www.youtube.com/watch?v=vVpSww9Xv-A.
    ◦ AI, Machine Learning, Deep Learning and Generative AI Explained. IBM Technology, 2023. Disponível em: https://www.youtube.com/watch?v=khKhK_zSAt0.
    ◦ BASICS of EEG-based Brain-Computer Interfaces. NeuroTechnology Exploration, 2021. Disponível em: https://www.youtube.com/watch?v=2e6i-H5pAnY.
    ◦ WHAT do neuroscientists really think about brain-computer interfaces (BCIs)? Medtronic, 2024. Disponível em: https://www.youtube.com/watch?v=680w9v_8H00.
    ◦ WHAT Is Consciousness? – A Question of Science with Brian Cox. The Francis Crick Institute, 2024. Disponível em: https://www.youtube.com/watch?v=8qN7Y7McljU.


---
## Link para o notebook


**https://notebooklm.google.com/notebook/653951be-e7c7-4167-ac8c-58573e16e242




