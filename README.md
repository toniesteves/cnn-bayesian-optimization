# CNN Bayesian Optimization Implementation



## Funcionamento

A otimização bayesiana funciona construindo uma distribuição posterior de funções (processo gaussiano) que melhor descreve a função que você deseja otimizar. À medida que o número de observações aumenta, a distribuição posterior melhora e o algoritmo torna-se mais certo de quais regiões no espaço de parâmetros valem a pena explorar e quais não, como visto na figura abaixo.

![BayesianOptimization in action](bo_example.png)

À medida que você repete continuamente, o algoritmo equilibra suas necessidades de exploração, levando em consideração o que sabe sobre a função de destino. Em cada etapa, um processo gaussiano é ajustado às amostras conhecidas (pontos explorados anteriormente), e a distribuição posterior, combinada com uma estratégia de exploração (Limite de Confiança Superior) ou (Melhoria Esperada)), são usadas para determinar o próximo ponto que deve ser explorado.

![BayesianOptimization in action](bayesian_optimization.gif)

Esse processo foi projetado para minimizar o número de etapas necessárias para encontrar uma combinação de parâmetros próximos à combinação ideal. Para fazer isso, esse método usa um problema de otimização de proxy (encontrando o máximo da função de aquisição) que, embora ainda seja um problema difícil, é mais barato (no sentido computacional) e ferramentas comuns podem ser empregadas. Portanto, a otimização bayesiana é mais adequada para situações em que a amostragem da função a ser otimizada é um empreendimento muito caro. Veja as referências para uma discussão apropriada sobre esse método.


# Dependências
* Tensorflow
* Keras
* Numpy
* Scipy
* Scikit-learn

# Referências:
* http://papers.nips.cc/paper/4522-practical-bayesian-optimization-of-machine-learning-algorithms.pdf
* http://arxiv.org/pdf/1012.2599v1.pdf
* http://www.gaussianprocess.org/gpml/
* https://www.youtube.com/watch?v=vz3D36VXefI&index=10&list=PLE6Wd9FR--EdyJ5lbFl8UuGjecvVw66F6
* https://github.com/fmfn/BayesianOptimization
* https://stackoverflow.com/questions/55586472/mnist-data-set-up-batch
* https://keras.io/examples/mnist_cnn/
* https://www.youtube.com/watch?v=sXdxyUCCm8s
* https://machinelearningapplied.com/hyperparameter-search-with-bayesian-optimization-for-keras-cnn-classification-and-ensembling/
* https://www.tensorflow.org/api_docs/python/tf/keras/optimizers/Adam
* https://stackoverflow.com/questions/55586472/mnist-data-set-up-batch
