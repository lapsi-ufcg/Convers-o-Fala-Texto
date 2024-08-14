# Fala-Texto
# . Configuração do Ambiente local 
  A ferramenta Fala-Texto é um sistema de registro de informações em saúde controlado por comandos de voz nos sistemas de informações de saúde do SUS. E para utilizar essa ferramenta é necessário configurar um ambiente local de implementação. Os requisitos desse ambiente são o python , já que o todo o sistema Fala-texto é baseado nesta linguagem de programação, e bibliotecas. A seguir será mencionado as etapas para configuração desse ambiente no Windows e no linux. 
  
# Instalação do python no Windows: 

-Se você ainda não tem o Python instalado, baixe a versão mais recente do Python neste Link : https://www.python.org/downloads/ e instale-a;
-Certifique-se de adicionar o Python ao PATH durante a instalação.

 <div align="center">
 <img src="https://github.com/user-attachments/assets/9d43e535-7d9d-4da3-b922-ed350344251d" width = "350px"/>
 </div>

# Instalação do python no linux: 
-O Python geralmente já está instalado no Ubuntu. Verifique digitando python3 no terminal;
-Se não estiver instalado, use o seguinte comando:  “sudo apt-get update && sudo apt-get install python3“.
# Instalação da ferramenta mpg321 no linux: 
Essa ferramenta realiza a execução de arquivos de áudio e para instalar o mpg321, use o comando: “sudo apt-get -y install mpg321”

# Instalação das Bibliotecas: 
Use o gerenciador de pacotes pip para instalar as bibliotecas python. No windons, esse gerenciador já vem instalado, quando você instala o python. Já no linux é necessário executar o seguinte comando no terminal:  “sudo apt-get update && sudo apt-get install python-pip". 
Em seguida, deve-se instalar as bibliotecas, que possuem os recursos necessários para o sistema Fala-Texto funcionar corretamente. Tanto no windons como no linux,  o comando no terminal é “pip install nome-do-pacote", como na imagem abaixo:

Exemplo de utilização do pip:
 <div align="center">
 <img src="https://github.com/user-attachments/assets/99fa57ba-ca14-47d6-b9c8-92a3b7607876" width = "350px"/>
 </div>

# A lista abaixo, indica as bibliotecas que precisam ser instaladas por meio do gerenciador pip: 
.whisper;

.faster_whisper;

.pdfplumber;

.PyPDF2;

.PyMuPDF

.pandas;

.pyttsx3;

.gtts;

.subprocess;

.thefuzz;

.unidecode;

.selenium;

.unicodedata; 

.pyaudio; 

.wave; 

.threading;

.SpeechRecognition;

.tkinter.

Consulte a documentação oficial de cada biblioteca para aprender mais sobre suas funcionalidades e como usá-las. E explore tutoriais online e exemplos de projetos para aprofundar seu conhecimento. 

# Arquivo para Gravação

-Baixar arquivo onlyrecorder.py do repositório;

-Para executar o código:

---Pressionar o botão indicado para  início de gravação;

---Ao término, pressionar o botão indicado para parada de gravação;

---Nomear o arquivo conforme preciso exemplo:(procedimentos datasus: formato xxxxxxxxx-x).

# Ferramentas de transcrição de áudio

 .São necessários áudios gravados da etapa de gravação de áudio;
 
 .Para a biblioteca whisper, baixar arquivo onlywhisper.py e executar o código:
 
 ---Selecione o índice do áudio que se deseja a transcrição.

 .Para a biblioteca faster_whisper, baixar arquivo teste_faster.py e executar o código:
 
 ---Selecione o índice do áudio que se deseja a transcrição.

# Cálculo de Custos associados a procedimentos gravados

.São necessários áudios gravados da etapa de gravação de áudio;

--Padrão utilizado para pronúncia: (QUANTIDADE DE VEZES QUE PROCEDIMENTO FOI REALIZADO + NOME DO PROCEDIMENTO)

.Baixar arquivo continue2.py e tabela_consulta2.csv do repositório;
.Executar o código:

---Será pedido o índice do áudio .wav (formato de arquivo usado até então) ou a faixa de áudios

---Caso a parte numérica tenha sido má interpretada (ex. número e procedimento sem espaçamento) será solicitada a correção para o arquivo em específico;

---Caso a transcrição realizada do procedimento não corresponda ao pronunciado, serão mostrados três outros procedimentos similares ao dito. Escolhida a opção que de fato equivalha ao informado, prossegue-se para o cálculo do custo.

.No final da execução do código, serão informados a soma dos valores de cada procedimento e a soma geral.

# Formulário via web

.São necessários áudios gravados da etapa de gravação de áudio:

---Padrão utilizado para pronúncia: Ex: (NOME: FULANO DE TAL, GÊNERO: MASCULINO, IDADE: 30 ANOS, ESTADO CIVIL: CASADO, PROFISSÃO: ENGENHEIRO)

.Baixar arquivo demoWeb.py do repositório;

.Executar o código:

---Navegador escolhido para submissão do formulário: Microsoft Edge. 

 <div align="center">
 <img src="https://github.com/user-attachments/assets/dbac0c48-165b-4425-917b-1029cc23fd95" width = "450px"/>
 </div>

# Preenchimento do Laudo de Colposcopia

.São necessários áudios gravados da etapa de gravação de áudio:

---Padrão utilizado para pronúncia: Ex: (NOME Lorem, PRONTUÁRIO ipsum, DATA dolor, INDICAÇÃO DO EXAME sit, VULVOSCOPIA amet, EXAME ESPECULAR consectetur, descrição do exame com os campos a serem marcados, CONCLUSÃO adispiscing, CONDUTA elit, EXAMINADOR sed)

.Baixar arquivos LaudoCelio2.py , tabela_consulta2.csv e Laudo4.pdf do repositório;

.Executar o código:

---Será pedido o índice do áudio .wav (formato de arquivo usado até então)

.Nesta versão do código, o arquivo está sendo salvo como “pdf_editado.pdf”. (OBS: Caso já haja um arquivo com esse nome, ele será sobrescrito)

.Exemplo de preenchimento de laudo:

 <div align="center">
 <img src="https://github.com/user-attachments/assets/7f83b4f6-2d0c-4056-89df-4747ad3ad98d" width = "400px"/>
 </div>

# Preenchimento do Modelo de Fatura

.São necessários áudios gravados da etapa de gravação de áudio:

---Padrão utilizado para pronúncia: Ex: (QUANTIDADE DE VEZES QUE PROCEDIMENTO FOI REALIZADO + NOME DO PROCEDIMENTO)

.Baixar arquivos preencheUCPIA.py , tabela_consultaZ1.csv e NOVO MODELO DE FATURA.pdf do repositório;

.Executar o código:

---Será pedido o índice do áudio .wav (formato de arquivo usado até então) ou a faixa de áudios

.Nesta versão do código, o arquivo está sendo salvo como “pdf_editado[numero].pdf”. (OBS: esse número começa com um e vai sendo incrementado a medida que são salvos novos pdf's)

.O arquivo consta com os campos seguidos pelas descrições dos procedimentos preenchidos com o valor informado nos áudios.

.Exemplo de preenchimento realizado pelo modelo: 

 <div align="center">
 <img src="https://github.com/user-attachments/assets/053f8c75-2894-4dab-93c2-afedbbf97198" width = "500px"/>
 </div>




