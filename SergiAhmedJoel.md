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

Despres de cridar el comanda, demanara quins llenguatge vols fer serivir, que tenim JavaScript, CSS, JSON, Markdown, etc... <br>
<img width="287" height="166" alt="image" src="https://github.com/user-attachments/assets/d5e06f4d-9896-4878-a479-583fce2689a9" />

Ens demanara si volem comprovar sol la sintaxis o comprovar la sintaxis i buscar problemes que poden provocar errors. <br>
<img width="361" height="71" alt="image" src="https://github.com/user-attachments/assets/91509ce9-3692-4f86-b9c5-065ab5fa1aa1" />

Quin tipo de moduls volem fer serivir: <br>
<img width="415" height="91" alt="image" src="https://github.com/user-attachments/assets/3f8f9e15-3d2f-445c-a879-d583a159cef1" />

Ens demana si tambe es vol comprovar algun frameworks disponibles de ESLint. <br>
<img width="413" height="91" alt="image" src="https://github.com/user-attachments/assets/287c7b10-935e-4756-b706-350b81b3b65b" />

Ens demana si fem servir TypeScript per comprovar. <br>
<img width="435" height="34" alt="image" src="https://github.com/user-attachments/assets/10c219b6-0d4a-42a8-9f0d-f481145a2a35" />

Pregunta si el codi del projecte es fa servir un nevegador. <br>
<img width="287" height="70" alt="image" src="https://github.com/user-attachments/assets/b068e3d2-4321-4878-95c9-200853b805e4" />

Si ens falta certes dependencies, ens demanara si volem instal·lar, per poguer funcionar les comprovacions. <br>
<img width="619" height="90" alt="image" src="https://github.com/user-attachments/assets/ebfb9084-f7c5-40af-bfaa-1982f452c7ac" />

Ens demanara quin tipo de gestor de paquets volem fer servir. <br>
<img width="438" height="108" alt="image" src="https://github.com/user-attachments/assets/76a431f4-0e7a-466b-8e4f-0c980a0f609f" />

Aquest comanda, us generara un arxiu de configuracio tots, on es podra aplicar les regles que requereixen el projecte. Aquest arxiu generat es te de tenir aquesta configuracio:

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
