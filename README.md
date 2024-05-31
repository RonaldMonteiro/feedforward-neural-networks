## Redes neurais feedforward para classificação de câncer de mama

### Descrição

Este notebook é uma aplicação prática de uma rede neural _feedforward_ para resolver um problema real de saúde - a classificação binária de câncer de mama. Utilizando o _dataset Breast Cancer_, que contém diversas características de tumores mamários, o modelo é treinado para distinguir entre tumores benignos e malignos.

---

### Stack de tecnologia

O projeto foi desenvolvido usando as seguintes tecnologias:  
[![](https://camo.githubusercontent.com/bb64b34d04a01cfa79658e2704085740d88e209c21905d0f5b55ebc87a83aa3a/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f507974686f6e2d4646443433423f7374796c653d666f722d7468652d6261646765266c6f676f3d707974686f6e266c6f676f436f6c6f723d626c7565)](https://camo.githubusercontent.com/bb64b34d04a01cfa79658e2704085740d88e209c21905d0f5b55ebc87a83aa3a/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f507974686f6e2d4646443433423f7374796c653d666f722d7468652d6261646765266c6f676f3d707974686f6e266c6f676f436f6c6f723d626c7565)![](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)[![](https://camo.githubusercontent.com/c484268661eef28f84e4888611778267794c78a0b2df7f16025d3f85f6227225/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f7363696b69745f6c6561726e2d4637393331453f7374796c653d666f722d7468652d6261646765266c6f676f3d7363696b69742d6c6561726e266c6f676f436f6c6f723d7768697465)](https://camo.githubusercontent.com/c484268661eef28f84e4888611778267794c78a0b2df7f16025d3f85f6227225/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f7363696b69745f6c6561726e2d4637393331453f7374796c653d666f722d7468652d6261646765266c6f676f3d7363696b69742d6c6561726e266c6f676f436f6c6f723d7768697465)[![](https://camo.githubusercontent.com/4487725c400789fceb3e540abc5b7cabe5dee39b7e4c91e1e906fccd26416cbd/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50616e6461732d3243324437323f7374796c653d666f722d7468652d6261646765266c6f676f3d70616e646173266c6f676f436f6c6f723d7768697465)](https://camo.githubusercontent.com/4487725c400789fceb3e540abc5b7cabe5dee39b7e4c91e1e906fccd26416cbd/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50616e6461732d3243324437323f7374796c653d666f722d7468652d6261646765266c6f676f3d70616e646173266c6f676f436f6c6f723d7768697465)[![](https://camo.githubusercontent.com/6eca86d3f9f9e48719c4958f16f78d98197b34f8928976e7b4c241d906f08738/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4e756d70792d3737374242343f7374796c653d666f722d7468652d6261646765266c6f676f3d6e756d7079266c6f676f436f6c6f723d7768697465)](https://camo.githubusercontent.com/6eca86d3f9f9e48719c4958f16f78d98197b34f8928976e7b4c241d906f08738/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4e756d70792d3737374242343f7374796c653d666f722d7468652d6261646765266c6f676f3d6e756d7079266c6f676f436f6c6f723d7768697465)

### Técnicas utilizadas

*   **Validação cruzada**: o conjunto de dados é dividido em partes, e o modelo é treinado com uma parte e testado com outra.
*   **Ajuste fino**: ajuste dos parâmetros do modelo para melhorar o desempenho.
*   **Dropout**: regularização durante o treinamento no qual alguns neurônios são desligadas para evitar _overfitting_.

### Arquitetura da rede

![Rede neural artificial – Wikipédia, a enciclopédia livre](https://upload.wikimedia.org/wikipedia/commons/3/3d/Neural_network.svg)

*   **🟢 Camada de entrada**: 30 neurônios de entrada e 16 neurônios de saída.
*   **🔵 Camada oculta**: 16 neurônios de entrada e 16 neurônios de saída.
*   **🟡 Camada de saída**: 16 neurônios de entrada e 1 neurônio de saída.
*   **⭕ ReLU** e **Sigmoid** foram utilizados como funções de ativação.