# ☁️ Azure Virtual Machine: Configuração e Documentação de Lab

Este repositório contém a documentação técnica do desafio prático realizado na plataforma **DIO**, focado no provisionamento e configuração de Máquinas Virtuais na **Microsoft Azure**.

---

## 🎯 Objetivos do Projeto

- Aplicar conceitos de Infraestrutura como Serviço (IaaS).
- Provisionar uma Máquina Virtual (VM) de forma estruturada no portal Azure.
- Configurar regras de segurança e conectividade.
- Demonstrar boas práticas de organização e encerramento de recursos.

---

## 🛠️ Passo a Passo da Configuração

### 1. Organização com Resource Group

Criei um **Resource Group (Grupo de Recursos)** específico para este laboratório.

> **Por que?** Isso permite que todos os componentes (VM, Disco, IP Público, VNet) sejam deletados simultaneamente ao final do teste, garantindo que não restem custos residuais.

### 2. Especificações da Máquina Virtual

As configurações escolhidas para este laboratório foram:

- **Nome da VM:** `Lab-VM-DIO`
- **Região:** `East US` (Leste dos EUA)
- **Sistema Operacional:** `Windows Server 2022 Datacenter: Azure Edition`
- **Tamanho:** `Standard_B1s` (1 vCPU, 1 GiB de memória)
- **Tipo de Disco:** `SSD Standard (LRS)`

### 3. Configuração de Rede e Segurança (NSG)

Para permitir o acesso à máquina, configurei o **Network Security Group (NSG)**:

- **Porta de Entrada:** Liberada a porta `3389` (Protocolo RDP) para acesso remoto.
- **IP Público:** Configurado como dinâmico para este ambiente de teste.

---

## 🖥️ Validação e Acesso

Após o status da VM mudar para **Running (Executando)**, realizei a conexão utilizando o cliente de _Conexão de Área de Trabalho Remota_.

**Ações realizadas dentro da VM:**

1. Verificação de status do sistema.
2. Teste de conectividade com a internet.
3. [OPCIONAL: Mencione aqui se instalou algo, como o IIS].

---

## 💡 Insights e Lições Aprendidas

- **Segurança em Primeiro Lugar:** Aprendi que expor portas de gerenciamento (como RDP/SSH) para a internet exige cuidado. O ideal é usar firewalls ou VPNs em ambientes reais.
- **Custo-Benefício:** A escolha do tamanho `B1s` é ideal para laboratórios por ser econômica e funcional para tarefas simples.
- **Automação:** Notei que a Azure oferece modelos (Templates JSON/Bicep) que facilitam a criação de máquinas idênticas no futuro.

---

## 🧹 Finalização

Para cumprir o **Modelo de Responsabilidade Compartilhada** e evitar cobranças desnecessárias, o Grupo de Recursos foi deletado após a validação dos testes.

---

## 🧑‍💻 Autor

Desenvolvido por **[SEU NOME AQUI]**

- [Link para seu LinkedIn]
- [Link para seu Portfólio no GitHub]
