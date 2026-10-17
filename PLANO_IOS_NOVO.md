# FASSEB iOS - nova base Android

## Origem e isolamento
Branch criada a partir de `fasseb-reinicio`. Não alterar nem mesclar na branch Android sem revisão.

## Objetivo da primeira etapa
Construir a aplicação iOS para simulador em macOS no GitHub Actions, sem assinatura Apple, publicação ou acesso de escrita à produção.

## Procedimento
1. Executar manualmente o workflow `FASSEB iOS - Diagnostico a partir do Android` selecionando esta branch.
2. Examinar os logs de falha; não presumir que a compilação teve sucesso.
3. Corrigir dependências e configurações apenas nesta branch, com commits pequenos.
4. Validar recursos iOS (ícones, splash, permissões em português, navegação, login Moodle, notificações e acessibilidade).
5. Configurar assinatura, testes em dispositivo, TestFlight e App Store somente após a compilação de diagnóstico passar.

## Restrições
- Não armazenar certificados, chaves ou senhas no código.
- Não modificar o Moodle em produção.
- Não executar migrações ou alterações em dados de alunos.
- A build de simulador não é um IPA para App Store.
- Conferir disponibilidade e compatibilidade das versões de Node, Cordova e Xcode antes de avançar.
