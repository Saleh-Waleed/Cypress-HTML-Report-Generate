# Cypress-HTML-Report-Generate
Cypress provides a feature to generate HTML report of the test cases.


1)  install cypress-mochawesome-reporter			
			
npm i --save-dev cypress-mochawesome-reporter			
or			
			
yarn add -D cypress-mochawesome-reporter			

							
2) Edit config file (cypress.config.js by default)							
							
const { defineConfig } = require('cypress');							
module.exports = defineConfig({                 //add this line to config.js							
reporter: 'cypress-mochawesome-reporter',							
e2e: {							
setupNodeEvents(on, config) {                  //add this line to config.js							
require('cypress-mochawesome-reporter/plugin')(on);							
},							
},							
});							
							
3)  Add to cypress/support/e2e.js							
import 'cypress-mochawesome-reporter/register';							
							
							
Copy the path of any particular test case or E2E (which has all the test cases)							
open that coped path on browser  like   C://path/cypress/reports/html/index.html							
