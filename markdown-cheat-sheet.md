# Linters i ESLint

## Introducció

Un linter es una eina que permet optimizar el codi font, es un instrument que analitza el codi font per determinar si existeix alguna inconsistencia.
En serveix per detectar si hi han errors en el codi, fa depuracio del codi, fa examens d'analisis del codi entre altres.

Els linters són útils per a llenguatges de programació compilats, però també són importants per als llenguatges interpretats, 
ja que en aquests no es té l'opció d'un compilador que identifiqui les inconsistències durant el període de desenvolupament del sistema.

## Origen

El seu origen prové d'un antic recurs implementat en el llenguatge de programació C, anomenat lint en l'any 1979.

## Funcions

- Anàlisi d'errors de sintaxi: Verifiquen que el codi no contingui errors de sintaxi, com errors de puntuació o ús incorrecte de funcions. 
- Identificació de problemes potencials: Detecten problemes en el desenvolupament del codi, com trucades a funcions obsoletes o variables no declarades.
- Verificació d'estils de codi: Asseguren que el codi segueixi les pautes d'estil establertes, la qual cosa ajuda a mantenir la llegibilitat i la coherència.
- Seguretat del codi: Es poden configurar per detectar vulnerabilitats de seguretat en el codi font. 
- Manteniment del codi: Faciliten la revisió i millora contínua del codi, ajudant els desenvolupadors a mantenir el seu codi més net i fàcil d'entendre.

## Exemples de linters

- ESLint: Eina per a JavaScript que ajuda a mantenir la qualitat del codi i assegura que segueixi certes regles d'estil.
- Stylelint: Eina per a CSS que verifica el compliment de les directrius d'estil.
- Pylint: Eina per a Python que serveix identificar errors, aplicar estàndards de codificació i millorar la qualitat del codi.
- HTMLHint: Eina que seveix per validar HTML
- Commitlint: Eina que ajuda a mantenir la coherència als fitxers de codi d'un repositori.
- Ktlint: Eina per al llenguatge de programació Go que verifica el compliment de les regles d'estil.
- TSLint: Eina per a TypeScript que ajuda a mantenir la qualitat del codi.

## Comandes ESLint

ESLint per poguer utilizar, es fa servir uns ordes de comandes.

Es requereix instal·lar "npm", per poguer utilizar ESLint, que es un paquet per generar arxius per gestions generals per JavaScript

Primer es te de instal·lar el ESLint que es te de fer servir les ordes de comandes que son aquest:

npm init @eslint/config@latest

Aquest comanda, us generara un arxiu de configuracio tots, on es podra aplicar les regles que requereixen el projecte. Aquest arxiu generat es tenir aquesta configuracio:

**import js from "@eslint/js";** <br>
**import globals from "globals";** <br>
**import { defineConfig } from "eslint/config";** <br>

**export default defineConfig([** <br> 
  **{ files: ["**/*.{js,mjs,cjs}"], plugins: { js }, extends: ["js/recommended"], languageOptions: { globals: globals.browser } },** <br>
**]);** <br>

per fer la primera comprovacio es posa aquest orde de comanda: 

**npx eslint nom_arxiu.js**

tambe podem comprovar multiples arxius: 

**npx eslint arxiu1.js arxiu2.js**

si tenim gran quantitat arxius, per estalviar escriure es pot utilizar aquest comanda:

**npx eslit ./**

si necessitem tindre varios tipos de configuracions, per diferents contextos de desenvolupament o situacions, podem indicar una configuracio especifica amb aquesta comanda:

**npx eslint -c nom_configuracio.config.mjs arxiu1.js**
