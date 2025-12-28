
# Blue Team Authentication Monitoring Lab

## 📌 Objetivo
Este projeto tem como objetivo demonstrar habilidades básicas de **Blue Team / SOC** por meio da análise de eventos de autenticação em um sistema Linux, simulando tentativas de acesso via SSH e investigando os logs gerados pelo sistema.

O laboratório foi desenvolvido para fins educacionais e para compor portfólio profissional.

---

## 🛠️ Ambiente Utilizado
- Sistema Operacional: Ubuntu Linux (VM)
- Serviço analisado: SSH
- Gerenciador de logs: systemd-journald
- Ferramentas:
  - journalctl
  - ssh
  - sudo

---

## 🔍 Cenário Simulado
Foram realizadas tentativas de acesso SSH utilizando:
- Usuário inexistente
- Senhas incorretas

Essas ações simulam comportamentos comuns em ataques de **força bruta** e **enumeração de usuários**.

---

## 📑 Evidências Coletadas

### Tentativa de login com usuário inválido
![Invalid User]screenshots/Captura de tela de 2025-12-27 17-15-29.png

### Falha de autenticação por senha incorreta
![Failed Password]screenshots/Captura de tela de 2025-12-27 17-15-10.png

---

## 🧠 Análise dos Logs

Os eventos foram identificados através do comando:

```bash
sudo journalctl -u ssh

