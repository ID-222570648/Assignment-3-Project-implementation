/** This file demonstrates how a component can change output 
dynamically to target HTML component.  
*  https://www.youtube.com/watch?v=F44OoFk8spg&list=PL4cUxeGkcC9gQcYgjhBoeQH7wiAyZNrYa&index=28 date accessed: 27/09/2022
* https://www.youtube.com/watch?v=09n2945JW_0&list=PL4cUxeGkcC9gQcYgjhBoeQH7wiAyZNrYa&index=29 date accessed: 27/09/2022
*/

<template>
    <div>
        <keep-alive> /*keep-alive retains data even when a new instance of the component is created.*/
        <component v-bind:is="component"></component> /*v-bind binds dynamic component with changing value.*/
        </keep-alive>
        /*v-on handles the event of button click. Here the event is changing form on button click*/
        <button v-on:click="component='contact-Form1'">General enquiry</button> 
        <button v-on:click="component='contact-Form2'">Order form</button>
    </div>
</template>
<script>
    /* importing forms */
import contactForm from "./component/contactFormGen.vue";
import contactForm1 from "./component/contactFormSale.vue";
        export default { //exporting to make it available to other parts of the app
            components: {
                'contact-Form1': contactFormGen, //Registering components
                'contact-Form2': contactFormSale
            },
            data(){
                return {
                    component:'contactFormGen' // setting up output for the dynamic component.
                }
            },
            methods: {

            }
        }
</script>
