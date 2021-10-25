# Contribuciones

Las contribuciones son bienvenidas, te invitamos a enviarlas a través de un _pull request_, un _issue_
o una _discusión_ de GitHub. Te pedimos que sigas esta guía en caso de enviar un _pull request_.

## Proceso

1. Haz un _fork_ del proyecto.
1. Crea una nueva rama.
1. Haz tu código, corre las pruebas y comparte tus cambios.
1. En el _pull request_ detalla los cambios.

## Guía básica

- Apégate al estándar de código del proyecto.
- Asegúrate que las pruebas actuales son exitosas. Si has agregado algo crea las pruebas oportunas.
- Envía una historia de _commits_ coherente, haz que cada _commit_ en tu _pull request_ tenga sentido.
- Tal vez necesites hacer _[rebase](https://git-scm.com/book/en/v2/Git-Branching-Rebasing)_ para evitar _merge conflicts_.
- Si estás cambiando el comportamiento o la UI pública entonces cambia también la documentación.
- Corre las revisiones en tu entorno de desarrollo antes de enviar tu _pull request_, asegúrate que tus pruebas son exitosas.

## Preparación del ambiente de desarrollo

### Instala las dependencias

```shell
yarn
```

### Prepara los archivos de ambiente

```shell
cp .env.example .env
```

Y actualiza el reciente archivo con los datos correctos.

### Inicia la aplicación en modo desarrollo (SPA).

```shell
yarn dev:spa
```

### Contruye la aplicación

```shell
yarn build:spa
```

## Estilo

Apégate al estándar de código del proyecto, verificado usando [ESLint][eslint].

Para corregir el código automáticamente:

```shell
yarn run lint
```

También es necesario que te apeges al estándar de commit del proyecto, verificado usando [CommitLint][commitlint]. Configurado en una configuración estandar para web [Conventional - Angular][conventional].

## Pruebas

El proyecto tiene diferentes tipos de pruebas, divido en dos librerias usadas principalmente:

Para pruebas unitarias y de integración se utiliza [Jest][jest]. Según sea el caso usaras alguno de los siguientes comandos.

```shell
yarn run test:unit
yarn run test:unit:ci
yarn run test:unit:coverage
yarn run test:unit:watch
yarn run test:unit:watchAll
yarn run serve:test:coverage
yarn run concurrently:dev:jest
```

Para pruebas end to end se utiliza [Cypress][cypress].

```shell
yarn run test:e2e
yarn run test:e2e:ci
```

### Prettier

[Prettier][prettier] es una herramienta que se usa para dar formato a tu código, siendo una de las mejores opciones cuando quieres obtener un estilo de programación consistente.

## Otras herramientas

### Quasar Cli

Tener instalado [QuasarCli][quasarcli] te permitira correr globalmente los [comandos de quasar][quasarcommands], permitiendo generar rápidamente templates de componentes, store, boot, etc.

[eslint]: https://eslint.org/
[commitlint]: https://commitlint.js.org/#/
[conventional]: https://www.conventionalcommits.org/en/v1.0.0-beta.4/
[jest]: https://jestjs.io/
[cypress]: https://www.cypress.io/
[prettier]: https://prettier.io/
[quasarcli]: https://quasar.dev/quasar-cli/installation
[quasarcommands]: https://quasar.dev/quasar-cli/commands-list
