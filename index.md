# 📡 Net_Test — Plataforma Completa de Testes de Rede

Bem-vindo ao **Net_Test**, um sistema completo para automação, orquestração e análise de testes de rede.  
Desenvolvido em **Python + Streamlit**, o Net_Test oferece inventários em YAML, banco SQLite versionado, geração de agentes PowerShell, dashboards avançados e integração com APIs de firewall.

Ideal para equipes de **Infraestrutura, Redes, DevOps, SRE, NOC/SOC, Segurança e Observabilidade**.

---

## 🚀 Por que usar o Net_Test?

O sistema fornece tudo o que uma operação de rede distribuída precisa:

- ✔ Testes paralelos por loja/site  
- ✔ Automação completa via YAML  
- ✔ Relatórios automáticos em HTML e JSON  
- ✔ Dashboards visuais com métricas reais  
- ✔ Versionamento de inventários  
- ✔ Integração com automações corporativas  
- ✔ Interface intuitiva e segura (login incluso)

---

## 🔍 Testes Suportados

### ICMP / Ping
- Status: UP / DOWN  
- Gráficos de latência, jitter e perda

### TCP Check
- Porta **OPEN** ou **CLOSED**

### UDP Check
- Resposta / Timeout

### DNS Resolution
- RESOLVED / UNRESOLVED  
- Suporte para FQDN interno e externo

### HTTP/HTTPS Check
- Status code  
- Tempo de resposta  
- Acessibilidade

---

## 📁 Inventário em YAML + SQLite Versionado

```yaml
sites:
  LOJA_CENTRO:
    hosts:
      - name: API_SERVER
        role: API
        ip_or_fqdn: api.loja.com.br
        testes:
          - tipo: tcp
            porta: 443
            regra: must_pass
```

---

## 🤖 Agente PowerShell Automático

O agente:

- Lê os testes do YAML/SQLite  
- Executa tudo localmente na máquina  
- Salva relatório **HTML**  
- Gera **JSON completo**  
- Pode ser enviado ao sistema via aba *Testes Remotos*

---

## 📊 Dashboards

### Latência
- 24h / 7 dias / 30 dias  
- Histórico  
- Jitter e perda  
- Gráficos interativos

### Portas
- TCP / UDP  
- Comparação por loja  
- Roles (API, POS, DB etc.)

### Heatmap de Falhas
- Horários críticos  
- Instabilidades por site

---

## 📦 Instalação

```bash
git clone https://github.com/SEU-USER/Net_Test.git
cd Net_Test
pip install -r requirements.txt
streamlit run appv5.py
```

---

## 🗂️ Estrutura do Projeto

```
Net_Test/
│── appv5.py
│── requirements.txt
│── README.md
│── REALMENTE.md
│── install.md
│── db/
│── backups/
│── yaml/
│── agents/
│── reports/
└── utils/
```

---

## 🔥 Status dos Testes

| Teste | OK | Falha |
|-------|------|--------|
| TCP | OPEN | CLOSED |
| DNS | RESOLVED | UNRESOLVED |
| ICMP | UP | DOWN |

---

## 🤝 Contribuições

Contribuições são bem-vindas!  
Abra Issues ou PRs.

---

## 📜 Licença

MIT License.

---


