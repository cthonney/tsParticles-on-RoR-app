# tsParticles Project with Rails

You can clone the repo to test TsParticles.
Or follow the instructions below.

## Setup

1. **Add tsParticles**:
   - In `config/importmap.rb`:
     ```erb
     pin "tsparticles", to: "https://cdn.jsdelivr.net/npm/tsparticles"
     ```
   - In `app/javascript/application.js`:
     ```erb
     import "tsparticles";
     ```


2. **Stimulus Controller**:
   - Create a file `app/javascript/controllers/tsparticles_controller.js`:
     ```javascript
     import { Controller } from "stimulus";

     export default class extends Controller {
       connect() {
         tsParticles.load("particles-js", {
           // ...options
         });
       }
     }
     ```

3. **HTML**:
   - Add the following element where you want the particles to appear, with the `data-controller` attribute for Stimulus:
     ```html
     <div data-controller="tsparticles" id="particles-js"></div>
     ```

4. **CSS/SCSS**:
   - In your CSS or SCSS file:
     ```scss
     #particles-js {
       position: fixed;
       top: 0;
       left: 0;
       width: 100%;
       height: 100%;
       z-index: 0;
     }
     ```


     ...

Thank you to @diogolsq for the importmap section.🎉

For more information on tsParticles, visit [tsParticles on GitHub](https://github.com/matteobruni/tsparticles).

