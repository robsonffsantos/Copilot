# Explorando Ferramentas de IA: Copiloto e OpenAI

## 📋 Sobre o Projeto

Este repositório documenta minha jornada explorando as funcionalidades do Copiloto e das ferramentas da OpenAI, com foco especial nos filtros de conteúdo e nos recursos de criação assistida por inteligência artificial. Aqui você encontrará exemplos práticos, prompts testados e anotações detalhadas sobre os aprendizados adquiridos durante o curso da DIO.

## 🎯 Objetivos

- Aplicar conceitos de IA Generativa em ambiente prático
- Documentar interações com ferramentas de IA
- Analisar comportamentos dos filtros de conteúdo
- Explorar técnicas eficientes de prompt engineering
- Compartilhar descobertas e melhores práticas

## 🧠 Ferramentas Exploradas

### GitHub Copilot

O GitHub Copilot é uma ferramenta de IA que funciona como um assistente de programação, oferecendo sugestões de código em tempo real enquanto você programa.

#### Exemplos de Uso:

1. **Autocompletar Código**
   ```python
   def calcular_media(lista_numeros):
       # O Copilot sugeriu completar a função
       total = sum(lista_numeros)
       return total / len(lista_numeros) if lista_numeros else 0
   ```

2. **Geração de Funções Completas**
   ```javascript
   // Solicitei ao Copilot: "função para validar email"
   function validarEmail(email) {
     const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
     return regex.test(email);
   }
   ```

3. **Documentação Automática**
   ```python
   def processar_dados(dados, formato="json"):
       """
       Processa os dados no formato especificado.
       
       Args:
           dados (dict): Dicionário contendo os dados a serem processados
           formato (str, opcional): Formato de saída. Padrão é "json".
           
       Returns:
           str: Dados processados no formato especificado
       """
       # Implementação sugerida pelo Copilot
   ```

### OpenAI API (GPT-4 e DALL-E)

#### Exemplos de Prompts e Resultados:

1. **Geração de Texto (Artigo Técnico)**

   **Prompt:**
   ```
   Escreva um artigo técnico sobre as aplicações práticas de Large Language Models em ambientes corporativos, focando em casos de uso para automação de processos.
   ```

2. **Geração de Imagens com DALL-E**

   **Prompt:**
   ```
   Uma visualização futurista de um escritório onde humanos e assistentes de IA trabalham juntos, estilo digital art, cores vibrantes.
   ```

3. **Análise de Dados com GPT-4**

   **Prompt:**
   ```
   Analise os seguintes dados de vendas e extraia insights importantes:
   [dados de exemplo]
   ```

## 🚫 Filtros de Conteúdo e Limitações

Durante os testes, identifiquei diversos comportamentos relacionados aos filtros de conteúdo:

### Observações sobre Filtros:

1. **Recusa em Gerar Conteúdo Prejudicial**
   - A IA recusa consistentemente solicitações para criar:
     - Conteúdo que promova atividades ilegais
     - Informações que possam causar danos
     - Conteúdo que viole propriedade intelectual

2. **Respostas Equilibradas em Tópicos Sensíveis**
   - Ao discutir tópicos políticos ou controversos, os modelos tendem a:
     - Apresentar múltiplas perspectivas
     - Evitar posicionamentos extremos
     - Sinalizar quando uma informação é opinativa

3. **Limitações Técnicas Observadas:**
   - Conhecimento limitado a eventos até sua data de corte de treinamento
   - Impossibilidade de executar código ou acessar internet em tempo real
   - Ocasionalmente gera informações plausíveis mas incorretas

## 💡 Técnicas de Prompt Engineering

### Estratégias Eficientes Testadas:

1. **Prompts com Contexto Detalhado**
   ```
   Contexto: Sou um desenvolvedor frontend trabalhando em uma aplicação React para e-commerce.
   Tarefa: Preciso criar um componente de carrinho de compras.
   Requisitos: O componente deve permitir adicionar/remover itens, atualizar quantidades e calcular o total.
   Formato desejado: Componente React funcional com hooks.
   ```

2. **Técnica de Chain-of-Thought (Raciocínio em Cadeia)**
   ```
   Explique passo a passo como resolver este problema de otimização: [problema].
   Para cada etapa, mostre o raciocínio e as possíveis alternativas consideradas.
   ```

3. **Role Prompting (Definição de Papéis)**
   ```
   Atue como um especialista em segurança cibernética e analise as vulnerabilidades potenciais neste trecho de código: [código]
   ```

## 📊 Resultados e Aprendizados

### Principais Descobertas:

1. **Especificidade Melhora Resultados**
   - Prompts detalhados com contexto claro produziram respostas significativamente melhores
   - Exemplificar o formato de saída desejado aumentou a precisão

2. **Limitações Importantes**
   - Os modelos ainda precisam de verificação humana, especialmente em:
     - Cálculos matemáticos complexos
     - Referências a eventos recentes
     - Código que exige otimização de desempenho

3. **Casos de Uso Mais Promissores**
   - Prototipagem rápida de código
   - Brainstorming e ideação
   - Automação de documentação
   - Simplificação de conceitos complexos

## 🛠️ Como Reproduzir os Experimentos

1. **Configuração da API OpenAI**
   ```python
   import openai
   
   # Configure a chave da API (utilize variáveis de ambiente para maior segurança)
   openai.api_key = os.getenv("OPENAI_API_KEY")
   
   # Exemplo de chamada à API
   response = openai.ChatCompletion.create(
       model="gpt-4",
       messages=[
           {"role": "system", "content": "Você é um assistente especialista em Python."},
           {"role": "user", "content": "Como implementar um decorador em Python?"}
       ]
   )
   ```

## 📚 Recursos Adicionais

- [Documentação Oficial da OpenAI](https://platform.openai.com/docs/)
- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [Melhores Práticas de Prompt Engineering](./recursos/prompt_engineering.md)
- [Exemplos de Código Completos](./exemplos/)
