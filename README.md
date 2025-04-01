# ESLint

## ¿Qué es?

Eslint es una herramienta quie analiza el codigo y detecta problemas dentro de codigos en JavaScript, sirve para señalar errores de sintaxis, malas practicas, o asegurar que se sgan convenciones de estilo de manera correcta.

## ¿Cómo instalarlo?

Iniciar un proyecto Node.js
```bash
npm init -y
```

Instalar ESLint como dependencia de desarrollo
```bash
npm install eslint --save-dev
```

Configurar ESLint
```bash
npx eslint --init
```

## Reglas y configuración

De entre las reglas que se pueden configurar en el proyecto las más comunes son:

- **no-unused-vars**: Señala variables que se declaran pero no se utilizan.
- **semi**: Requiere o prohíbe el uso de punto y coma al final de las líneas.
- **quotes**: Define si se deben usar comillas simples o dobles.
- **indent**: Establece el número de espacios para la indentación.

Las reglas se configuran dentro del archivo **.eslintrc**, ejemplo:

```bash
{
    "rules": {
        "no-unused-vars": "warn",  // advertencia si hay variables no usadas
        "semi": ["error", "always"],  // error si no se usa punto y coma
        "quotes": ["error", "single"],  // error si no se usan comillas simples
        "indent": ["error", 2]  // error si la indentación no tiene 2 espacios
    }
}
```

## ¿Cómo se usa?

Una vez instalado y configurado se puede usar haciendo uso de diversos comandos:
1. **Comando para analizar archivos**

    Para un archivo en especifico:
    ```bash
    npx eslint archivo/directorio
    ```

    Para todos los archivos JavaScript en el proyecto:
    ```bash
    npx eslint .
    ```

2. **Corregir automáticamente errores**

    ```bash
    npx eslint . --fix
    ```

El ejemplo lo agregue como comentario al archivo index.js