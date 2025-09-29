# DIO - Trilha .NET - Explorando a linguagem C#
www.dio.me

## Desafio de projeto
Para este desafio, você precisará usar seus conhecimentos adquiridos no módulo de explorando a linguagem C#, da trilha .NET da DIO.

## Contexto
Você foi contratado para construir um sistema de hospedagem, que será usado para realizar uma reserva em um hotel. Você precisará usar a classe Pessoa, que representa o hóspede, a classe Suíte, e a classe Reserva, que fará um relacionamento entre ambos.

O seu programa deverá cálcular corretamente os valores dos métodos da classe Reserva, que precisará trazer a quantidade de hóspedes e o valor da diária, concedendo um desconto de 10% para caso a reserva seja para um período maior que 10 dias.

## Regras e validações
1. Não deve ser possível realizar uma reserva de uma suíte com capacidade menor do que a quantidade de hóspedes. Exemplo: Se é uma suíte capaz de hospedar 2 pessoas, então ao passar 3 hóspedes deverá retornar uma exception.
2. O método ObterQuantidadeHospedes da classe Reserva deverá retornar a quantidade total de hóspedes, enquanto que o método CalcularValorDiaria deverá retornar o valor da diária (Dias reservados x valor da diária).
3. Caso seja feita uma reserva igual ou maior que 10 dias, deverá ser concedido um desconto de 10% no valor da diária.


![Diagrama de classe estacionamento](diagrama_classe_hotel.png)

## Solução
O código está pela metade, e você deverá dar continuidade obedecendo as regras descritas acima, para que no final, tenhamos um programa funcional. Procure pela palavra comentada "TODO" no código, em seguida, implemente conforme as regras acima.

---

## ✅ Implementações Realizadas:
### 1. Método ObterQuantidadeHospedes
- Retorna a quantidade de hóspedes através de Hospedes.Count
### 2. Método CalcularValorDiaria
- Calcula o valor total: DiasReservados × Suite.ValorDiaria
- Aplica desconto de 10% para reservas ≥ 10 dias
- Fórmula do desconto: valor × 0.9m
### 3. Validação de Capacidade
- Verifica se Suite.Capacidade >= hospedes.Count
- Lança exceção quando a capacidade é insuficiente
- Mensagem: "A capacidade da suíte é menor que o número de hóspedes recebido"
## 🧪 Testes Realizados:
1. 1. Teste Normal : 2 hóspedes, 5 dias → 150 (2 × 5 × 30)
2. 2. Teste Desconto : 2 hóspedes, 10 dias → 270 (2 × 10 × 30 × 0.9)
3. 3. Teste Exceção : 3 hóspedes em suíte capacidade 2 → Exceção lançada

Todas as regras de negócio foram implementadas corretamente e o programa está funcionando conforme especificado no contexto. O sistema agora valida adequadamente a capacidade das suítes, calcula os valores com desconto quando aplicável, e retorna a quantidade correta de hóspedes.