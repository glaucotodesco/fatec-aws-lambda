Trabalho de Iniciação Científica:

Desenvolvimento de Aplicações Serverless em AWS Lambda

-Prof. Orientador. Dr Glauco Todesco

-Aluno Afonso Henrique de Eustaquio Araujo Melgar Ribes

--Este trabalho é referente a iniciação científica da FATEC Sorocaba, com o Objetivo de mostrar as principais diferenças, vantagens e desvantegens do desenvolvimento na nuvem, com as ferramentas da AWS, explorando ao máximo as ferramentas oferecidas.

--Todo o desenvolvimento e funções que foram desenvolvidas, serão colocadas aqui em passo a passo.

--Cronograma de entregas quizenais

26/09/2024 - Aplicações simples de Backend com Lambda, CRUD e endpoints Simples em Java, estudo sobre como funciona o desenvolvimento serverless em AWS Lambda, arquitetura e rotina de desenvolvimento na AWS, para melhor ambientação para o curso e para responder possíveis dúvidas dos alunos no minicurso

03/10/2024 - Entrega do Minicurso de AWS Lambda, que será ministrado pelo aluno no dia 08/10/2024, slides e todo o cronograma, tutorial explicativo no repositório github, todo com funcionamento pelas ferramentas oferecidas pelo learner Lab, além de um video explicativo ensinando todo o passo a passo

10/10/2024 - Entrega dos resultados do minicurso, escolha definitiva e início da migração de um sistema de baixa/média complexidade para a computação em nuvem

24/10/2024 - Desenvolvimento da transferência, seja back-end ou front-end, com algo funcional já nas ferramentas da AWS

07/11/2024 - Finalização da migração do sistema para a AWS, espera-se que somente precise de alguns ajustes mínimos e início dos testes e formulação do relatório sobre os resultados dos estudos, tanto do minicurso, com usabilidade das ferramentas, como o desempenho em relação a computação tradicional

21/11/2024 - Entrega do relatório final, com todos os resultados obtidos com o trabalho, tais como trabalhos futuros que podem ser feitos para uma pesquisa mais precisa e completa

***Passo a passo do Minicurso da Semana da Tecnologia:***

![image](https://github.com/user-attachments/assets/ed12b51c-1b5c-4a8c-bfc9-f5afc7ced5f6)

- AWS Amplify e fazer o deploy do index.html do helloWorld, e ver como funciona o deploy do site na AWS Amplify

- Criar Função Lambda com o código lambda no repositório, com o nome do database que irá criar no dynamoDB e função para o próprio lambda, que irá ser usado posteriormente. Aplicar o Role LabRole.

- Crie uma tabela no DynamoDb, com o nome especificado pelo lambda

- Edite a permissão AWS IAM que criou para o lambda, com as seguintes permissões, adicionando as políticas pelo JSON abaixo:

        {
            "Version": "2012-10-17",
            "Statement": [
            {
                "Sid": "VisualEditor0",
                "Effect": "Allow",
                "Action": [  
                    "dynamodb:PutItem",
                    "dynamodb:DeleteItem",
                    "dynamodb:GetItem",
                    "dynamodb:Scan",
                    "dynamodb:Query",
                    "dynamodb:UpdateItem"
                    ],
                    "Resource": "YOUR-TABLE-ARN"
                }
            ]
        }

- Copiar o ARN do DynamoDB table criada , em informações adicionaisdo dynamoDB, copia-la no lugar de YOUR-TABLE-ARN

- Criar uma API REST no API Gateway, com o método POST que faça a chamada na função lambda que criamos, ativando os CORS

- Realizar Teste diretamente a API, e ver o funcionamento do Banco de Dados

- Atualizar o Amplify, abrindo o arquivo index.html, e substituindo o link do API Gateway gerado pelo

-Gerar o arquivo. zip do index.html, adicionar a imagem a esta pasta .zip

- Fazer o deploy da nova pasta .zip e atualizar a aplicação

- Agora é para a aplcação estar funcionando perfeitamente, enviando um formulário e enviando para o dynamoDB, lembrando que o link é público.

- Tentar fazer a mesma coisa com o S3 Bucket, gerando um site estático com o index.html e tendo a mesma funcionalidade que o AWS Amplify

