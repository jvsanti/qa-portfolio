# QA Portfolio

Este repositório reúne o trabalho prático da minha certificação em QA Engineering (Mate Academy): planejamento de testes, design de casos de teste, execução e reporte de bugs. Parte foi feita em aplicações de treino (Conduit, PetStore, OWASP Juice Shop), parte em sites reais em produção (AIESEC, Domino's Brasil).

Antes de QA de software, passei 6+ anos como Analista de Qualidade em manufatura automotiva (IATF 16949 / ISO 9001), como residente em cliente OEM (Stellantis, Nissan). A lógica de causa raiz que uso lá — 8D, Pareto, Ishikawa — é a mesma que apliquei aqui pra investigar bugs.

## O que tem aqui

**test-plans/** — Test Plan completo pro app Conduit: escopo, critérios de suspensão e saída, cronograma.

**test-cases/** — casos de teste formais. Inclui um ciclo STLC completo no carrinho do PetStore (30 casos, 100% executados, 73% de aprovação) e 36 casos desenhados a partir de user stories de um job board fictício.

**bug-reports/** — os bugs que encontrei, um arquivo por site/app testado. No total são 34+ bugs documentados em 13 sites/apps diferentes. Dois valem destaque:

- No checkout da **Domino's Brasil** (site real, em produção), o carrinho não limita a quantidade de um item — depois de um certo ponto, o total para de atualizar e a página quebra com um erro visível pro usuário.
- No **OWASP Juice Shop** (plataforma feita pra treino de segurança), a política de senha do cadastro não é aplicada de verdade: o formulário diz que exige 8+ caracteres com maiúscula, número e símbolo, mas aceita senha fraca sem reclamar.

Os outros bugs são de sites menores — Bern.com, Global Lives Project, Lumos, Stellarium, Cinks Labs, EnergyTelecom, Sweet Shop — a maioria também sites reais, usados como exercício de "achar bug em produção" do curso.

**test-design-techniques/** — equivalence partitioning, boundary value analysis, decision table e pairwise testing.

**api-testing/** — testes de API feitos no Postman, com assertions em JavaScript.

Mais projetos (incluindo automação com Playwright) vão sendo adicionados aqui conforme ficam prontos.

## Stack

SQL, Git, HTML/CSS, JavaScript, Postman, Jira, TestRail, Playwright.

## Contato

jv.santiago@live.com · [LinkedIn](https://linkedin.com/in/jvsanti)
