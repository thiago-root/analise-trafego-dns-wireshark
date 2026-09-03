# 🔍 Análise de Tráfego DNS com Wireshark e Ubuntu Server

Este repositório contém o relatório prático de análise de tráfego de rede e resolução de nomes (DNS), integrando uma máquina virtual **Ubuntu Server** (configurada em modo *Bridge* via VirtualBox) ao **Wireshark** rodando no host.

---

## 🎯 Objetivos
- Executar comandos de gerenciamento de cache e resolução de nomes no Linux via CLI.
- Capturar e inspecionar pacotes DNS utilizando o Wireshark.
- Analisar os cabeçalhos Ethernet II, IPv4 e UDP, validando o mapeamento de endereços de origem e destino.
- Inspecionar as *Flags* do protocolo DNS para identificar suporte à consulta recursiva.

---

## 🛠️ Tecnologias e Ferramentas Utilizadas
- **Sistema Operacional Guest:** Ubuntu Server (Linux)
- **Virtualização:** Oracle VM VirtualBox (Rede em Modo *Bridge*)
- **Analisador de Pacotes:** Wireshark
- **Utilitários CLI:** `resolvectl`, `nslookup`, `ip address`

---

## 📋 Passo a Passo Executado

### 1. Limpeza de Cache e Consulta DNS no Linux
No terminal do Ubuntu Server, limpou-se o cache do resolvedor e foi feita a consulta direta ao domínio target:

```bash
# Limpeza do cache DNS
sudo resolvectl flush-caches

# Verificação do status do cache
sudo resolvectl statistics

# Consulta de resolução de nomes
nslookup [www.cisco.com](https://www.cisco.com)
