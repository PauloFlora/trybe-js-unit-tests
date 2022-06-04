## O que é o projeto Testes Unitários JS

Neste projeto criei testes e as respectivas funções para diversos desafios propostos, com o objetivo de aprofundar meus conhecimentos com testes untiários utilizando Jest.

Algumas funções já foram fornecidas pelo desafio, para as quais realizei os testes que garantem a sua correta funcionalidade.

Exemplo abaixo:

```javascript
 describe('9 - Implemente os casos de teste da função `getCharacter`', () => {
  it('Verifica se a função `getCharacter` retorna o objeto do personagem corretamente.', () => {
    // ESCREVA SEUS TESTES ABAIXO:
    // Teste se a função, quando não recebe nenhum parâmetro, retorna undefined.
    assert.strictEqual(getCharacter(), undefined)
    // Teste se a função retorna o objeto correto para o parâmetro 'Arya',
    let result = {
      name: 'Arya Stark',
      class: 'Rogue',
      phrases: [ 'Not today', 'A girl has no name.' ]
    }
    assert.deepStrictEqual(getCharacter('Arya'), result)

    // Teste se a função retorna o objeto correto para o parâmetro 'Brienne',
    result = {
       name: "Brienne Tarth",
       class: "Knight",
       phrases: ["Im No Lady, Your Grace.", "I, Brienne Of Tarth, Sentence You To Die."]
    }

    assert.deepStrictEqual(getCharacter('Brienne'), result)
    // Teste se a função retorna o objeto correto para o parâmetro 'Melissandre',
    result = {
      name: "Melissandre",
      class: "Necromancer",
      phrases: ["Death By Fire Is The Purest Death.", "For The Night Is Dark And Full Of Terrors."]
    }

   assert.deepStrictEqual(getCharacter('Melissandre'), result)
    // Teste se a função se os parâmetros não são Case Sensitive.
    assert.deepStrictEqual(getCharacter('mEliSSanDRE'), result)
    assert.deepStrictEqual(getCharacter('MELISSANDRE'), result)
    assert.deepStrictEqual(getCharacter('melissandre'), result)

    // Teste se ao passar um nome que não está na tabela, a função retorna undefined.
    assert.deepStrictEqual(getCharacter('paulo'), undefined)
  });
});
```