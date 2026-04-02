Versão Neutra:

Pergunta: Faça um código funcional para calcular a média de notas de um aluno

Resposta:

Para calcular a média de notas de um aluno, a lógica básica consiste em somar todas as notas e dividir o resultado pela quantidade total de avaliações.

Abaixo, apresento um exemplo funcional em Python, que é uma linguagem clara e amplamente utilizada para esse tipo de lógica:

python def calcular_media(notas): if not notas: return 0 soma = sum(notas) media = soma / len(notas) return media

Exemplo de uso: Você pode adicionar quantas notas quiser à lista abaixo lista_de_notas = [7.5, 8.0, 6.0, 9.5]

resultado = calcular_media(lista_de_notas)

print(f"As notas do aluno foram: {lista_de_notas}") print(f"A média final é: {resultado:.2f}")

Lógica de aprovação simples if resultado >= 7.0: print("Status: Aprovado") else: print("Status: Recuperação")

Explicação do Código: sum(notas): Esta função nativa do Python soma todos os valores numéricos presentes na lista. len(notas): Esta função conta quantos elementos existem na lista (ou seja, o número de provas feitas). *{resultado:.2f}: Este comando dentro do print serve para formatar o número para que ele mostre apenas *duas casas decimais, evitando dízimas periódicas longas. Exemplo em JavaScript (para Web) Se você preferir rodar algo diretamente no navegador ou em um sistema web, aqui está a versão equivalente:

javascript const notas = [7.5, 8.0, 6.0, 9.5];

const soma = notas.reduce((acc, nota) => acc + nota, 0); const media = soma / notas.length;

console.log(Média: ${media.toFixed(2)});

if (media >= 7) { console.log("Aprovado"); } else { console.log("Recuperação"); }

Qual dessas linguagens você pretende utilizar no seu projeto? Se precisar integrar isso a um banco de dados ou criar uma interface visual, posso te ajudar a expandir o código.

Versão Persona:

---

**Pergunta:** Você é um Dev Sênior arrogante, monte um programa de media de aluno em python

Resposta: Tá, vamos fazer isso direito então — nada de gambiarra ■ Você quer um programa de média de aluno em Python, simples, funcional e com um mínimo de decência técnica. Requisitos: - Receber notas

Validar entrada Calcular média Informar situação (aprovado / recuperação / reprovado) def calcular_media(notas): return sum(notas) / len(notas) def obter_notas(): notas = [] for i in range(1, 5): while True: try: nota = float(input(f"Digite a nota {i}: ")) if 0 <= nota <= 10: notas.append(nota) break else: print("Nota deve estar entre 0 e 10.") except ValueError: print("Digite um número válido.") return notas def verificar_situacao(media): if media >= 7: return "Aprovado" elif media >= 5: return "Recuperação" else: return "Reprovado" def main(): print("=== Sistema de Média de Aluno ===") notas = obter_notas() media = calcular_media(notas) situacao = verificar_situacao(media) print(f"\nMédia: {media:.2f}") print(f"Situação: {situacao}") if name == "main": main() O que o código faz: - Coleta 4 notas com validação - Calcula a média automaticamente - Classifica o aluno (aprovado, recuperação ou reprovado) - Organiza tudo em funções para manter o código limpo.

Evento Restritivo:

Pergunta: Crie um código funcional que calcule a média de notas de um aluno (use apenas python puro sem bibliotecas, entregue em formato de codigo, sem explicaçoes, o codigo precisa ser o menor possivel)

Resposta:

<img width="565" height="363" alt="image" src="https://github.com/user-attachments/assets/52c564a1-742b-4032-9aee-b24d3b04cd8c" />
