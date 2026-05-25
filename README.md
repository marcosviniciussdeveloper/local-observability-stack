Aqui está um modelo de `README.md` simples, direto e limpo, bem focado no padrão técnico que o mercado gosta de ver em portfólios de DevOps e infraestrutura.

Basta criar um arquivo chamado `README.md` na mesma pasta dos seus arquivos e colar o conteúdo abaixo:

```markdown
# Prometheus & Grafana Docker Stack 🚀

Este repositório contém a estrutura de arquivos necessária para subir um ambiente local completo de observabilidade e monitoramento de infraestrutura utilizando o Docker Compose.

O objetivo deste laboratório é coletar e visualizar em tempo real as métricas de hardware (CPU, Memória, Disco e Rede) do sistema operacional host.

## 🏗️ Arquitetura da Stack

- **Prometheus**: Banco de dados temporal (TSDB) responsável por realizar o scraping (modelo Pull) das métricas a cada 15 segundos.
- **Node Exporter**: Agente que roda no servidor coletando e expondo as métricas nativas do Linux em formato de texto simples.
- **Grafana**: Ferramenta de analytics conectada ao Prometheus para renderizar dashboards visuais via consultas em PromQL.

## 🚀 Como Executar o Projeto

### Pré-requisitos
- Docker instalado
- Docker Compose instalado

### Passo a Passo

1. Clone este repositório na sua máquina local:
```bash
git clone [https://github.com/marcosviniciussdeveloper/prometheus-grafana-docker.git](https://github.com/marcosviniciussdeveloper/prometheus-grafana-docker.git)
cd prometheus-grafana-docker

```

2. Inicialize a stack de containers em background:

```bash
docker compose up -d

```

3. Verifique se todos os serviços estão de pé e rodando:

```bash
docker ps

```

## 🌐 Portas e Acessos Mundiais

Após subir os containers, você pode acessar as ferramentas através do seu navegador:

* **Prometheus UI:** `http://localhost:9090` (Acesse `Status -> Targets` para validar a saúde dos coletores)
* **Node Exporter Metrics:** `http://localhost:9100/metrics` (Dados brutos gerados pela máquina)
* **Grafana Dashboard:** `http://localhost:3000`

### 🔑 Credenciais Padrão do Grafana

* **Usuário:** `admin`
* **Senha:** `admin`

*(O Grafana solicitará a alteração da senha no primeiro login).*

## 📊 Importando o Dashboard de Monitoramento Linux

Para visualizar os gráficos sem precisar criá-los do zero:

1. No menu lateral do Grafana, vá em **Dashboards -> New -> Import**.
2. No campo de ID do grafana.com, digite **1860** (ID do painel oficial do Node Exporter) e clique em **Load**.
3. Selecione o `Prometheus` como fonte de dados (Data Source) e clique em **Import**.

```

Salve o arquivo, faça o commit final e mande tudo pro seu repositório remoto! 🦾

```
