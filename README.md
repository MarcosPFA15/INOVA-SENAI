Este é o PROUT - Projeto Capacete de Segurança Inteligente

🏆 Projeto premiado com o 3º lugar na competição Inova SENAI 2025! 🏆

Este repositório contém o desenvolvimento do nosso site para o projeto de capacete de segurança inteligente, uma solução de IoT projetada para aumentar a segurança de trabalhadores em ambientes industriais, de mineração e em locais isolados.

O principal objetivo é reduzir drasticamente o tempo de resposta em caso de acidentes e monitorar o uso correto de Equipamentos de Proteção Individual (EPIs), salvando vidas e garantindo a conformidade com as normas de segurança.

✨ Funcionalidades Principais

🤕 Detecção de Queda: Utiliza sensores para detectar quedas bruscas com um sistema de confirmação em duas etapas (2FA) via notificação para minimizar alarmes falsos.

📍 Localização em Tempo Real: Módulo GPS integrado para rastreamento da localização exata do trabalhador, crucial para equipes de resgate em áreas amplas ou remotas.

❓ Motionless: Inatividade e Ausência: O sistema monitora a inatividade (falta de movimento por um período configurável) e a ausência (não registro da jornada no horário previsto), gerando alertas para o supervisor.

💳 Identificação por RFID: Cada funcionário possui um crachá com um UID único, lido por um módulo RFID no capacete para identificação e registro de jornada.

🌐 Dashboard de Monitoramento: Uma plataforma web completa que exibe a estrutura da equipe, o status de cada funcionário em tempo real (online, offline, em risco) e gera relatórios detalhados.

📊 Relatórios Avançados: A interface web permite a análise de eventos por período e gera gráficos de duração de atividades, como "Jornada de Trabalho", "Tempo em Altura", "Inatividade" e "Tempo de Almoço".

🚨 Sistema de Alertas: O backend envia notificações instantâneas para supervisores em caso de qualquer ocorrência de risco.

🏗️ Arquitetura do Sistema
A solução opera em quatro camadas principais:

Hardware (O Capacete): Um microcontrolador como cérebro, conectado a sensores e um sistema de rádio ou wifi para comunicação.

Comunicação (MQTT): Os capacetes publicam seus dados e eventos em um Broker MQTT, um protocolo leve e eficiente ideal para IoT.

Backend (Node-RED): Um servidor que se inscreve nos tópicos MQTT, recebe os dados, processa todas as regras de negócio (verifica horários, valida alertas, etc.), armazena as informações e as expõe através de uma API.

Frontend (Dashboard Web): Uma interface de usuário construída em HTML, CSS e JavaScript que consome a API do backend para exibir os dados de forma visual e interativa para os gestores.

🚀 Próximos Passos (Roadmap)
Integrar o sistema de notificações com o Microsoft Teams através de Webhooks.

Desenvolver e treinar uma rede neural para detecção de anomalias ou reconhecimento de uso de EPIs a partir de câmeras.

Evoluir a arquitetura de armazenamento para um banco de dados robusto para suportar um histórico de longo prazo.

((Este projeto foi desenvolvido no âmbito do programa Inova SENAI, visando aplicar tecnologia e inovação para resolver problemas reais da indústria brasileira.))
