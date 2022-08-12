# Chemotherapy Safety
Application of Artificial Intelligence in Chemotherapy Traceability and Patient Safety

O procedimento de identificação dos objetos em classes (ampola, garrafa e seringa) foi treinado em uma rede neural convolucional classificadora (RNCC), onde ela identificava qual objeto era apresentado à câmera. Todas as imagens utilizadas neste treinamento foram marcadas para informar o objeto apresentado, gerando um tutor a RNCC durante seu treinamento supervisionado. Esta etapa tem como objetivo um pré-processamento da imagem, preparando a escolha para uma RNC posterior, específica para identificar o volume da seringa.

O volume da seringa é identificado por uma rede neural convolucional regressiva (RNCR) onde sua saída contínua obtém o valor de volume, em mililitros, do conteúdo da seringa. A RNCR só pode ser aplicada a seringas, por isso a necessidade de uma RNCC realizando a filtragem das imagens de ampolas, garrafas e seringas. O procedimento de treinamento é similar a RNCC, a diferença é que o tutor agora não é uma classe, mas sim um valor numérico do volume presente na seringa na imagem, isso garante um processo regressivo de treinamento supervisionado sobre a rede e melhorando significativamente sua eficácia na entrega do volume.

Bibtex:
'''
@article{cortez2021quimio,
  title={Controle da Manipulação em Mesa Aberta de Medicamentos Quimioterápicos},
  author={Cortez, Pedro Paulo and Valério de Moraes, Carlos Henrique and Yoshinari Junior, Gerson Hiroshi},
  journal={Trabalho Final de Graduação de Engenharia de Controle e Automação da UNIFEI},
  year={2021}
}
'''
