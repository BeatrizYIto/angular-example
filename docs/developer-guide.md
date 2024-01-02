# Guia do desenvolvedor

## 1. Nomenclaturas de variáveis e funções

### Deve

- 1.1. Utilizar o idioma inglês;
- 1.2. Utilizar o padrão camelCase;
- 1.3. Utilizar a regra [SID](https://github.com/kettanaito/naming-cheatsheet#s-i-d) (short, intuitive, descriptive);
- 1.4. Utilizar o padrão [A/HC/LC](https://github.com/kettanaito/naming-cheatsheet#ahclc-pattern).
- 1.5. Utilizar o prefixo `is` para variáveis boolean. ex: `isDisabled`, `isEnabled` e etc.

### Não deve

- 1.6. Utilizar abreviações;

## 2. Padrões de projeto

### Deve

- 2.1. Priorizar variants dos componentes sobre estilos personalizados;
- 2.2. Priorizar `early return` sobre `else`;
- 2.3. Seguir padrão de Naming do próprio angular. ex: feature.type.ts.
- 2.4. Use o principio do T-DRY (Try to not Repeat Yourself) para evitar duplicação de código. [T-DRY](https://angular.io/guide/styleguide#t-dry-try-to-be-dry)
- 2.5. Use a estrutura de pastas [Folders-by-feature structure](https://angular.io/guide/styleguide#folders-by-feature-structure)

### Não deve

- 2.6. Utilizar `else if`;
- 2.7. Inverter lógica em condições, se possível. Exemplo: `!isEnabled` ao invés de `isDisabled`.
- 2.8. Criar componentes/arquivos muito grandes se estes podem ser separados em componentes/arquivos menores;
- 2.9. Criar bordas, cores, opacidade, sombras, espaçamentos e estilos de texto com valores fixos, sem utilizar tema;
- 2.10. Ultrapassar 400 linhas por arquivo.
- 2.11. Ultrapassar 75 linhas por função.

## 3. Angular

### Deve

- 3.1 Utilizar lazy loading nas navegações dos modulos
- 3.2. Delegar estrutura de logicas complexas para um service e não deixar no component.
- 3.3. Controlar logica de View diretamente no component.ts.
- 3.4. Prefira usar Enum ao invés de string para definir valores pré estabelecidos.
- 3.5. Use SwitchMap para lidar com observables aninhadas.

### Não deve

- 3.6. Utilizar logica no HTML `<p *ngIf="role==='developer'"> Status: Developer </p>`
- 3.7. Utilizar tipo string `private myStringValue: string;` para definir tipagem de valores pré estabelecidos, alterar para `private myStringValue: 'First' | 'Second'`
- 3.8. Nao use JS para pegar referencias de elementos do HTML. ex: `document.getElementById('myId')`

## 4. CSS

### Deve

- 4.1. Utilizar shorthand sintaxe para CSS.
  **_Exemplo:_**

  ```CSS
  .bg {
    background-color: #000;
    background-image: url(images/bg.gif);
    background-repeat: no-repeat;
    background-position: left top;
  }
  ```

  **_Para:_**

  ```CSS
  .bg {
    background: #000 url(images/bg.gif) no-repeat left top;
  }
  ```

### Não deve

- 4.2. Ultrapassar 3 níveis de indentação nos arquivos CSS.
- 4.3. Utilizar várias propriedades CSS na mesma linha, priorize estilizações multiline.
- 4.4. Utilizar mais de 3 seletores para criar uma regra de estilo. ex: `#home .features .feature-item-wrapper .feature-item h1 {/*...*/}`
