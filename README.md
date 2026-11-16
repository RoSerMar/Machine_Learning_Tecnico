# Machine Learning Técnico

Repositório de trabalho. Aqui guardamos notebooks, exercícios, experiências e pequenos projetos.

> Para evitar o clássico "na minha máquina funciona", **todos usamos exatamente as mesmas versões** listadas abaixo.

---

## Versões usadas

| Componente | Versão |
|---|---|
| Python | 3.11.x |
| TensorFlow | 2.18.0 |
| Keras | 3.6.0 (vem com o TensorFlow) |
| NumPy | 2.0.2 |
| Pandas | 2.2.3 |
| Matplotlib | 3.9.2 |
| scikit-learn | 1.5.2 |
| SciPy | 1.14.1 |
| Jupyter (JupyterLab) | 4.2.5 |

> **Nota:** o TensorFlow 2.16+ usa o **Keras 3** por defeito. Código antigo escrito para o Keras 2 (`tf.keras` com `tf-keras`) pode precisar de pequenos ajustes.

---

## Instalação

### 1. Clonar o repositório

```bash
git clone <URL_DO_REPOSITORIO>
cd <NOME_DO_REPOSITORIO>
```

### 2. Criar um ambiente virtual (Python 3.11)

```bash
python3.11 -m venv .venv
```

Ativar:

```bash
# Linux / macOS
source .venv/bin/activate

# Windows (PowerShell)
.venv\Scripts\Activate.ps1
```

### 3. Instalar as dependências

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Verificar a instalação

```bash
python -c "import tensorflow as tf, keras, numpy; print(tf.__version__, keras.__version__, numpy.__version__)"
```

Resultado esperado:

```
2.18.0 3.6.0 2.0.2
```

---

## requirements.txt

```txt
tensorflow==2.18.0
keras==3.6.0
numpy==2.0.2
pandas==2.2.3
matplotlib==3.9.2
scikit-learn==1.5.2
scipy==1.14.1
jupyterlab==4.2.5
```

---

## GPU (opcional)

Quem tiver uma GPU NVIDIA em **Linux** pode instalar o TensorFlow com suporte CUDA:

```bash
pip install "tensorflow[and-cuda]==2.18.0"
```

Verificar se a GPU é reconhecida:

```bash
python -c "import tensorflow as tf; print(tf.config.list_physical_devices('GPU'))"
```

No **Windows**, o suporte nativo a GPU já não existe nas versões recentes — usar CPU ou o WSL2. Para as aulas, a CPU é suficiente.

---

## Estrutura do repositório

```
.
├── notebooks/        # Notebooks de estudo e exercícios
├── src/              # Código reutilizável (módulos, funções)
├── data/             # Datasets pequenos (os grandes não vão para o Git)
├── models/           # Modelos treinados / checkpoints leves
├── requirements.txt  # Dependências fixadas
└── README.md
```

---

## Regras de colaboração

1. **Não alterar versões** no `requirements.txt` sem avisar o grupo.
2. Trabalhar em **branches** (`nome/tema`) e abrir *Pull Request* para a `main`.
3. Limpar o *output* dos notebooks antes de fazer commit (`Cell → All Output → Clear`).
4. **Não** fazer commit de datasets grandes nem de ambientes virtuais (`.venv/` está no `.gitignore`).
5. Fixar *seeds* aleatórias nos exercícios, para os resultados serem reproduzíveis:

```python
import numpy as np
import tensorflow as tf

np.random.seed(42)
tf.random.set_seed(42)
```

---

## Problemas comuns

| Problema | Solução |
|---|---|
| `No matching distribution found for tensorflow` | Confirmar que estás a usar Python 3.11 (`python --version`). |
| Erros de `numpy` ao importar o TensorFlow | Reinstalar com `pip install -r requirements.txt` num ambiente limpo. |
| Avisos `oneDNN custom operations` | São informativos. Para os silenciar: `export TF_ENABLE_ONEDNN_OPTS=0`. |
| Código antigo de Keras 2 falha | Ver o guia de migração do Keras 3 ou usar o pacote `tf-keras`. |

---

## Membros

| Nome | GitHub |
|---|---|
| Rodrigo Martins | RoSerMar |
| _(adicionar)_ | _(adicionar)_ |
| _(adicionar)_ | _(adicionar)_ |
| _(adicionar)_ | _(adicionar)_ |
| _(adicionar)_ | _(adicionar)_ |
| _(adicionar)_ | _(adicionar)_ |
| _(adicionar)_ | _(adicionar)_ |
| _(adicionar)_ | _(adicionar)_ |
| _(adicionar)_ | _(adicionar)_ |
