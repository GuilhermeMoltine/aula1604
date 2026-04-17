Caso de Uso 3 – Realizar Check-in (Controle de Acesso)

Ator principal: Aluno
Atores secundários: Sistema, Catraca

Requisitos relacionados:
RF04 — Regularidade do Aluno
RF05 — Controle de Acesso

📝 Descrição

Este caso de uso permite que o aluno realize o acesso à academia por meio da catraca utilizando RFID, desde que esteja com a mensalidade em dia.

✅ Pré-condições
Aluno deve estar cadastrado no sistema
Aluno deve possuir RFID cadastrado
Aluno deve estar com pagamento em dia
🎯 Pós-condições
Acesso registrado no sistema
Entrada liberada ou negada
🔹 Fluxo Principal
O aluno aproxima o RFID da catraca
O sistema identifica o aluno
O sistema verifica a regularidade do pagamento (RF04)
O sistema valida o acesso (RF05)
O sistema registra o acesso
A catraca libera a entrada do aluno
🔹 Fluxos Alternativos

A1 – Aluno inadimplente

No passo 3, se o pagamento estiver atrasado:
O sistema nega o acesso
Exibe mensagem: "Mensalidade em atraso"

A2 – RFID inválido

No passo 2, se o RFID não for reconhecido:
O sistema nega o acesso
Exibe mensagem: "Usuário não identificado"

A3 – Falha no sistema

Se ocorrer erro na validação:
O acesso é bloqueado por segurança
O sistema registra a tentativa
🔹 Regras de Negócio
Apenas alunos com pagamento em dia podem acessar
Cada acesso deve registrar data e hora
O RFID deve ser único para cada aluno
🔹 Classes Envolvidas
Aluno (RF04, RF05)
Acesso (RF05, RF09)
Pagamento (RF03, RF04)
