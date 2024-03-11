# 🧔 XandLeandro
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/alexandre-d%C3%B3ria-leandro-59764816/)

# 📽 Sobre mim
### Tenho 54 anos e mais de 30 anos de experiência na área de tecnologia. Desenpenhei várias funções ao longo de minha carreira, sendo: Programador, DBA, Gerente de Tecnologia, Gerente de Projetos. Nesta jornada desenvolvi soluções para utilização de Visual Souce Safe, TFS onde criei os primeiros modelos para integração de controle de releases e integração com o MS Project até chegar no Azure DevOps. 

![PL](https://img.shields.io/badge/PL%2FSQL-FFFFFF?style=for-the-badge&logo=oracle&logoColor=FF0000&labelColor=FFFFFF&color=FF0000)

![Azure](https://img.shields.io/badge/Azure-blue?style=for-the-badge&logo=microsoft%20azure&logoColor=blue&labelColor=FFFFFF&link=https%3A%2F%2Fimages.app.goo.gl%2FK7PN1jYJd57x4q7A8)

# ❓ Porque estou aqui?
### Sou motivado a inovação, acredito que precisamos manter nossa mente sempre ativa e desafiada e inteligencia artificial é um tema que sempre me dispertou interesse e curiosidade.

# 🔬 Sobre este projeto dio-lab-machinelearn
### Projeto para criação de modelo de previsão utilizando Machine Learn

Para realizar este projeto, primeiramente você precisa criar uma conta no [Azure portal](https://portal.azure.com) utilizando suas credenciais da Microsoft.
No meu caso, eu já possuia esta conta e por isso puei esta etapa.
Este é o link para criar uma conta gratuíta [Conta Gratuíta Azure](https://azure.microsoft.com/pt-br/free/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=docs&utm_campaign=visualstudio).

No Azure portal selecione **Criar um Recurso** e selecione ***Azure Machine Learning***, preencha as informações solicitadas conforme documentação do LAB. 

| Título | Descrição |
| -------| --------- |
| `Assinatura` | Sua assinatura do Azure. |
| `Grupo de recursos` | Insira um nome exclusivo para seu espaço de trabalho. Eu utilizei ***Laboratorioai900***. |
| `Região` | informe **East US** |
| `Conta de armazenamento` | Manter como está |
| `Cofre de chaves` | Manter como está |
| `Insights de aplicativo` | Manter como está |
| `Registro de contêiner` | Nenhum |
||

Agora selecione **Revisar e Criar** e posteriormente selecione **Criar**. Aguarde concluir o processo (isso pode demorar alguns minutos).

Tudo pronto, já podemos entrar no [Azure Machine Learning studio](https://ml.azure.com).

No menu lateral do ML Studio selecione ***ML automatizado*** e configure conforme informado no LAB na sessão ***Use automated machine learning to train a model***.

Quando seu JOB concluir passaremos para etapa de teste.
Clique no **nome do algoritmo** na janela do lado direito chamada ***Melhor resumo do modelo*** e selecione **Métricas** e analise os gráficos.

Agora vá até a aba ***Modelo** e selecione ***Implantar*** e escolha ***Serviço WEB***.
Configure da seguinte forma:

| Campo | Preenchimento |
| -----| ---------------|
| Nome | predict-rentals |
| Descrição | Predict cycle rentals |
| Tipo Computação | Azure Container Instance |
| Habilitar autenticação | Selecionar esta opção |

Aguardar a conclusão da implantação (aproximadamente 10 minutos).
Quando concluir a implantação no menu esquerdo selecione ***Pontos de extremidade*** e escola ***predict-rentals***.

Em ***predict-rentals*** selecione a aba ***Testar*** e preencha o template JASON conforme solicitado no descritivo do LAB e selecione o botão ***Testar***.

Revise os resultados do teste, que incluem um número previsto de aluguéis com base nos recursos de entrada - semelhante a este:

 {
   "Results": [
     444.27799000000000
   ]
 }

 Pronto, LAB concluído.


