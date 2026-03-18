# Cross-Domain Tracking

> **Type**: Task
> **Category**: tracking
> **Agents**: Traffic Chief, Deiss, Kusmich
> **Frameworks**: Cross-Domain Tracking Framework, Server-Side Tracking Architecture
> **Checklists**: tracking-checklist, cross-domain-checklist
> **Output template**: templates/tracking-setup-document.md

## ROUTING

> **Agents**: pixel-specialist
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Configurar cross-domain e cross-device tracking para garantir atribuição precisa quando o usuário navega entre múltiplos domínios (site principal, checkout, subdomínios) e dispositivos diferentes.

## Inputs
- Lista completa de domínios e subdomínios envolvidos na jornada do usuário
- Google Analytics 4 configurado
- GTM (Google Tag Manager) instalado em todos os domínios
- Pixels das plataformas de ads instalados
- Mapeamento da jornada do usuário cross-domain
- Política de privacidade e compliance (LGPD, GDPR)

## Steps
1. Mapear todos os domínios e subdomínios na jornada do usuário (site → checkout → thank you page)
2. Configurar cross-domain tracking no GA4 adicionando todos os domínios na configuração de data streams
3. Implementar linker parameter no GTM para passar o client ID entre domínios
4. Configurar o referral exclusion list no GA4 para evitar self-referrals entre domínios próprios
5. Verificar que os cookies first-party estão sendo mantidos corretamente na transição entre domínios
6. Implementar User-ID tracking no GA4 para rastrear usuários logados across devices
7. Configurar server-side GTM (sGTM) para melhorar a precisão do tracking em cenários de ITP/ETP
8. Validar que os pixels de ads (Meta, Google, TikTok) estão atribuindo corretamente cross-domain
9. Testar a jornada completa em diferentes browsers (Chrome, Safari, Firefox) e devices (mobile, desktop)
10. Configurar consent mode para compliance com LGPD/GDPR sem perder dados de atribuição
11. Documentar a arquitetura de tracking e criar runbook de troubleshooting

## Output
Cross-domain tracking configurado e validado, incluindo: mapa de domínios e fluxo de dados, configurações documentadas por ferramenta, relatório de testes cross-browser, e runbook de troubleshooting.

## Quality Gate
- Sessões não quebrando na transição entre domínios (validado no GA4 real-time)
- Self-referrals eliminados entre domínios próprios
- User-ID tracking funcionando para usuários logados
- Testes passando em Chrome, Safari e Firefox (mobile e desktop)
- Compliance com LGPD/GDPR validada
- Traffic Chief aprova a arquitetura de tracking antes de considerar finalizado

## Duration
6-10 horas para configuração técnica; 2-3 horas para testes cross-browser e documentação
