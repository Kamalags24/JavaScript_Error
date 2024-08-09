# JavaScript_Error


En JavaScript, il existe plusieurs types d'erreurs que vous pouvez rencontrer lors du développement. Voici les principaux types :

### 1. **SyntaxError**
   - **Description** : Cette erreur se produit lorsque le moteur JavaScript rencontre une syntaxe incorrecte. Cela empêche le code de s'exécuter.
   - **Exemple** : 
     ```javascript
     if (true {
         console.log("Erreur de syntaxe");
     }
     ```
   - **Message d’erreur** : `SyntaxError: Unexpected token '{'`

### 2. **ReferenceError**
   - **Description** : Cette erreur se produit lorsqu'une variable ou une fonction est référencée, mais n'a pas été déclarée ou n'est pas accessible dans la portée actuelle.
   - **Exemple** : 
     ```javascript
     console.log(nonDeclaree);
     ```
   - **Message d’erreur** : `ReferenceError: nonDeclaree is not defined`

### 3. **TypeError**
   - **Description** : Cette erreur se produit lorsqu'une opération est effectuée sur une valeur du mauvais type.
   - **Exemple** : 
     ```javascript
     let nombre = 42;
     nombre.toUpperCase();
     ```
   - **Message d’erreur** : `TypeError: nombre.toUpperCase is not a function`

### 4. **RangeError**
   - **Description** : Cette erreur se produit lorsque vous essayez d'utiliser un nombre qui est en dehors de la plage de valeurs légales. Par exemple, passer un nombre inapproprié à une méthode qui attend un indice valide ou une taille.
   - **Exemple** : 
     ```javascript
     let tableau = new Array(-1);
     ```
   - **Message d’erreur** : `RangeError: Invalid array length`

### 5. **EvalError**
   - **Description** : Cette erreur est liée à l'utilisation incorrecte de la fonction `eval()`. Bien que cette erreur soit rarement rencontrée aujourd'hui, car l'utilisation de `eval()` est déconseillée pour des raisons de sécurité.
   - **Exemple** :
     ```javascript
     // Peu probable, mais pour l'exemple
     eval("var x = ");
     ```
   - **Message d’erreur** : `EvalError: Bad string`

### 6. **URIError**
   - **Description** : Cette erreur se produit lors de l'utilisation incorrecte des fonctions de manipulation d'URI telles que `encodeURI()` ou `decodeURIComponent()`.
   - **Exemple** : 
     ```javascript
     decodeURIComponent('%');
     ```
   - **Message d’erreur** : `URIError: URI malformed`

### 7. **AggregateError**
   - **Description** : Cette erreur représente un ensemble d'erreurs qui se sont produites lors de l'exécution d'une seule opération. Elle est souvent utilisée avec les Promises combinées avec `Promise.any()` ou `Promise.allSettled()`.
   - **Exemple** :
     ```javascript
     let p = Promise.any([
       Promise.reject(new Error("Erreur 1")),
       Promise.reject(new Error("Erreur 2")),
     ]).catch(e => console.log(e.errors));
     ```
   - **Message d’erreur** : `AggregateError: All promises were rejected`

Ces erreurs peuvent être gérées en utilisant des blocs `try...catch` pour éviter que le programme ne plante de manière inattendue.


Lors de la rédaction du code JavaScript dans Visual Studio Code (VSCode), vous pouvez rencontrer différents types d'erreurs qui sont généralement détectées par l'éditeur avant même l'exécution du code. Voici les principales erreurs que vous pouvez rencontrer :

### 1. **Erreurs de syntaxe**
   - **Description** : Ces erreurs se produisent lorsque le code ne respecte pas la syntaxe correcte de JavaScript. Elles sont souvent signalées en temps réel par un soulignement rouge dans VSCode.
   - **Exemple** :
     ```javascript
     let x = 10
     if (x > 5) {
         console.log("Erreur de syntaxe")
     }
     ```
   - **Problème détecté** : Le point-virgule manquant après `let x = 10`, ou les accolades manquantes.

### 2. **Erreurs de référence (ReferenceError)**
   - **Description** : Ces erreurs se produisent lorsqu'une variable ou une fonction est référencée mais n'est pas déclarée ou définie.
   - **Exemple** :
     ```javascript
     console.log(maVariable);  // maVariable n'est pas définie
     ```
   - **Problème détecté** : L'éditeur signale que `maVariable` n'est pas définie.

### 3. **Erreurs de type (TypeError)**
   - **Description** : Ces erreurs se produisent lorsque vous essayez d'effectuer une opération sur un type de données incorrect.
   - **Exemple** :
     ```javascript
     let nombre = 10;
     nombre();  // nombre n'est pas une fonction
     ```
   - **Problème détecté** : VSCode peut indiquer que vous essayez d'appeler une variable qui n'est pas une fonction.

### 4. **Erreurs d'importation/exportation**
   - **Description** : Ces erreurs se produisent lors de l'importation ou de l'exportation incorrecte de modules.
   - **Exemple** :
     ```javascript
     import { nonExistant } from './monModule';  // nonExistant n'est pas exporté par ./monModule
     ```
   - **Problème détecté** : VSCode signale que le module ou l'élément import


Lors de la rédaction du code JavaScript dans Visual Studio Code (VSCode), vous pouvez rencontrer différents types d'erreurs. Certaines sont directement liées au langage JavaScript lui-même, tandis que d'autres peuvent provenir de l'environnement de développement ou des extensions que vous utilisez. Voici un aperçu des erreurs les plus courantes :

### 1. **Erreurs de syntaxe (SyntaxError)**
   - **Description** : Ces erreurs se produisent lorsque vous écrivez du code qui ne respecte pas la syntaxe correcte de JavaScript. Elles sont souvent signalées en temps réel avec un soulignement rouge.
   - **Exemples** :
     ```javascript
     let x = 10
     if (x > 5 {
         console.log("Erreur de syntaxe");
     }
     ```
   - **Indications dans VSCode** : Points rouges dans la barre de défilement, soulignement rouge dans le code.

### 2. **Erreurs de référence (ReferenceError)**
   - **Description** : Ces erreurs se produisent lorsque vous essayez d'utiliser une variable ou une fonction qui n'a pas été déclarée.
   - **Exemples** :
     ```javascript
     console.log(variableInexistante);
     ```
   - **Indications dans VSCode** : Un message peut indiquer que la variable n'est pas définie.

### 3. **Erreurs de type (TypeError)**
   - **Description** : Ces erreurs surviennent lorsque vous essayez d'exécuter une opération sur un type de données incorrect.
   - **Exemples** :
     ```javascript
     let nombre = 10;
     nombre();  // Erreur, car nombre n'est pas une fonction
     ```
   - **Indications dans VSCode** : Les extensions comme ESLint peuvent vous alerter sur ces erreurs.

### 4. **Erreurs d'importation/exportation**
   - **Description** : Ces erreurs se produisent lorsque vous importez ou exportez des modules de manière incorrecte ou tentez d'importer quelque chose qui n'existe pas.
   - **Exemples** :
     ```javascript
     import { fonctionInexistante } from './module.js';
     ```
   - **Indications dans VSCode** : Souvent signalé par une extension de linting ou par VSCode lui-même, indiquant que l'importation n'est pas valide.

### 5. **Erreurs liées aux extensions**
   - **Description** : Certaines erreurs peuvent être causées par des extensions VSCode comme ESLint, Prettier, ou TypeScript si vous les utilisez avec JavaScript. Ces extensions peuvent signaler des erreurs spécifiques basées sur les règles de style ou de typage.
   - **Exemples** :
     - ESLint peut signaler une violation de style de code.
     - Prettier peut reformater votre code de manière inattendue si le format est incorrect.
     - TypeScript (dans des fichiers `.ts` ou avec du code JavaScript typé) peut signaler des erreurs de type.

### 6. **Erreurs de configuration**
   - **Description** : Si votre projet est mal configuré (par exemple, des problèmes dans `package.json`, `webpack.config.js`, ou `.eslintrc.json`), cela peut entraîner des erreurs ou des dysfonctionnements dans VSCode.
   - **Indications dans VSCode** : Messages d'erreur dans le terminal ou la console de débogage.

### 7. **Erreurs de style et de formatage**
   - **Description** : Si vous utilisez des outils comme ESLint ou Prettier, vous pouvez rencontrer des erreurs ou des avertissements liés au style de code, comme les indentations incorrectes, l'absence de point-virgule, etc.
   - **Exemples** :
     ```javascript
     let x = 10
     console.log(x)  // Absence de point-virgule
     ```
   - **Indications dans VSCode** : Soulignement, avertissement, ou reformatage automatique selon les règles définies.

### 8. **Erreurs de compatibilité**
   - **Description** : VSCode peut signaler des erreurs liées à la compatibilité avec les navigateurs si vous utilisez des fonctionnalités JavaScript modernes qui ne sont pas prises en charge par tous les environnements.
   - **Indications dans VSCode** : Des extensions ou des plugins spécifiques peuvent signaler ces problèmes.

### 9. **Problèmes de performance**
   - **Description** : Si votre code contient des boucles infinies ou des calculs complexes, VSCode peut devenir lent ou se bloquer lors de l'analyse en temps réel.
   - **Indications dans VSCode** : Ralentissement de l'éditeur, messages d'erreur indiquant que le code est trop complexe à analyser.

Ces erreurs peuvent être identifiées et souvent corrigées grâce à des extensions utiles comme **ESLint**, **Prettier**, et en utilisant des outils intégrés de débogage dans VSCode.

