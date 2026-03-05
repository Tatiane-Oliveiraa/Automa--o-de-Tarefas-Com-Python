# Automação de Cadastro de Produtos

Este projeto utiliza a biblioteca `PyAutoGUI` para automatizar o processo de cadastro de produtos em um sistema web, a partir de um arquivo CSV contendo informações sobre os produtos. O objetivo é acelerar o processo de inserção de dados, poupando tempo na repetição de tarefas manuais.

## Requisitos

* Python 3.x
* Bibliotecas:

  * `pyautogui`
  * `pandas`

Você pode instalar as dependências utilizando o seguinte comando:

```bash
pip install pyautogui pandas
```

## Descrição

O programa realiza as seguintes etapas:

1. **Abrir o navegador**: O script abre o navegador Microsoft Edge.
2. **Acessar o sistema de cadastro**: O link do sistema de cadastro é acessado.
3. **Login no sistema**: O script preenche automaticamente os campos de login com o e-mail e a senha fornecidos.
4. **Leitura de dados do arquivo CSV**: O script lê um arquivo `produtos.csv` contendo informações de produtos, como código, marca, tipo, categoria, preço, custo e observações.
5. **Cadastro dos produtos**: Para cada linha do CSV, o script preenche automaticamente os campos de cadastro no sistema web, incluindo o código do produto, marca, tipo, categoria, preço unitário, custo e observações, quando presente.
6. **Repetição do processo**: O processo é repetido para todos os produtos presentes no arquivo CSV.

## Arquivo CSV

O arquivo `produtos.csv` deve ter o seguinte formato:

| codigo     | marca    | tipo   | categoria | preco_unitario | custo | obs              |
| ---------- | -------- | ------ | --------- | -------------- | ----- | ---------------- |
| MOLO000251 | Logitech | Mouse  | 1         | 25.95          | 6.5   |                  |
| MOLO000192 | Logitech | Mouse  | 2         | 19.95          | 5.0   |                  |
| CAHA000251 | Hashtag  | Camisa | 1         | 25.00          | 11.0  | Conferir estoque |
| ...        | ...      | ...    | ...       | ...            | ...   | ...              |

### Colunas do CSV:

* `codigo`: Código do produto.
* `marca`: Marca do produto.
* `tipo`: Tipo do produto.
* `categoria`: Categoria do produto (ex.: 1, 2, 3).
* `preco_unitario`: Preço unitário do produto.
* `custo`: Custo do produto.
* `obs`: Observações sobre o produto (opcional).

## Como usar

1. Clone o repositório para sua máquina local:

   ```bash
   git clone https://github.com/seuusuario/automacao-cadastro-produtos.git
   cd automacao-cadastro-produtos
   ```

2. Abra o terminal e execute o script Python:

   ```bash
   python automacao.py
   ```

3. O script abrirá automaticamente o navegador e realizará o cadastro de produtos no sistema.

## Considerações

* **Segurança**: Certifique-se de que as credenciais de login e outros dados sensíveis estão devidamente protegidos.
* **Erros comuns**: Caso o script falhe, verifique se as coordenadas de clique estão corretas. O `PyAutoGUI` usa coordenadas de tela, então as posições podem precisar ser ajustadas conforme a resolução da sua tela.

## Contribuições

Sinta-se à vontade para abrir issues ou enviar pull requests para contribuir com melhorias ou correções no projeto.

## Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.

