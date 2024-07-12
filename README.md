# CI&T/FLOW VSCode Extension

<br>
<br>

## Instalação

1. Abra seu Vscode

2. Va na aba extensões

3. Pesquise por: cit-code-flow-generator

    <img src="prints/print-marketplace-find-ext.png" alt="">

4. Baixe e instale.
5. Na sua pasta pessoal crie o arquivo prompts.yaml `/home/< user >/dev/flow/prompts.yaml`

    <img src="prints/print-folder-person.png" alt="">

6. Adicione o prompt default ou o `prompts.yaml` atual.

```sh
prompts:
- name: "Prompt - Explain Code (selected)"
  description: "Detailed Prompt to Explain the Selected Code"
  model: gpt-4o
  temperature: 0.7
  messages:
  - role: "system"
    content: |
      You are a highly experienced software engineer, responsible for explaining code in a clear and detailed manner. Your objective is to provide a comprehensive explanation of the code's functionality, logic, and structure.
  - role: "user"
    content: |
      ### Instructions:
      1. Thoroughly analyze the selected code.
      2. Provide a detailed explanation of the code's functionality and logic.
      3. Describe the purpose of each function/method, including parameters and return values.
      4. Explain key sections and logic within the code.
      5. Ensure your explanation covers the following aspects:
         - Code readability and style
         - Performance considerations
         - Security implications
         - Adherence to best practices and coding standards
         - Maintainability and scalability
      6. Provide your response in markdown format, with clear explanations for each point.


      ### Task:
      Explain the following code snippet:


      <SourceCode>
      {{selectedText}}
      </SourceCode>


- name: "Prompt - Explain Code (file)"
  description: "Detailed Prompt to Explain the Selected Code"
  model: gpt-4o
  temperature: 0.7
  messages:
  - role: "system"
    content: |
      You are a highly experienced software engineer, responsible for explaining code in a clear and detailed manner. Your objective is to provide a comprehensive explanation of the code's functionality, logic, and structure.
  - role: "user"
    content: |
      ### Instructions:
      1. Thoroughly analyze the selected code.
      2. Provide a detailed explanation of the code's functionality and logic.
      3. Describe the purpose of each function/method, including parameters and return values.
      4. Explain key sections and logic within the code.
      5. Ensure your explanation covers the following aspects:
         - Code readability and style
         - Performance considerations
         - Security implications
         - Adherence to best practices and coding standards
         - Maintainability and scalability
      6. Provide your response in markdown format, with clear explanations for each point.


      ### Task:
      Explain the following code snippet:


      <SourceCode>
      {{code}}
      </SourceCode>
```

7. Salve e feche o prompts.yam.
8. Use as Teclas `CTRL+P`.
9. Digite >`settings.json`.
8. Clique no primeiro e abra o json.

    <img src="prints/print-open-settings-user.png" alt="">

9. Adicione os itens abaixo.

```sh
"cit-code-flow-generator.pathToYamlWithPrompts": "",
```

10. Em `cit-code-flow-generator.pathToYAMLWithPrompt` coloque o caminho até o seu prompts.yaml.

11. Ex: `/home/< you_user >/dev/flow/prompts.yaml`.

12. Agora abra a aba do `CI&T/FLOW` e clique em `CI&T/FLOW - Login`.

    <img src="prints/print-extension-cit-flow.png" alt="">

13. Feito o login você já pode usar a extensão.

<br />
<br />
<br />

## Doc Oficial - Atualizado pelo time

- [Doc](https://docs.google.com/document/d/1BAUAbDTS5UBEHNe5a2RLDo628u6FAy5BR-r5I-0457E/edit#heading=h.4psw5ymq8a90)
