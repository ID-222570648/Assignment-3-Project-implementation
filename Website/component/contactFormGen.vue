
<script src="https://cdn.jsdelivr.net/npm/vue@2.7.10/dist/vue.js"></script>

<template>
    <div>
        <form-helper>
            <div slot="form-header">
                <h3> Fill this for to send your enquiry </h3> //Custom header
               </div>
               
                <div slot="form-fields"> // transfered from parent component
                    <label> Title </label>
                    <input type = "text" placeholder = "title" required/>
                    <label> First name </label>
                    <input type = "text" placeholder = "First name" required/>
                    <label> Last name </label>
                    <input type = "text" placeholder = "Last name" required/>
                    <label> Tel: </label>
                    <input type = "text" placeholder = "Tel. Num" required/>
                    <label> Email: </label>
                    <input type = "text" placeholder = "Email" required/>
                    <label> Address: </label>
                    <input type = "text" placeholder = "Unit" required/>
                   
                    <input type = "text" placeholder = "St no. and name" required/>
                  
                    <input type = "text" placeholder = "Suburb" required/>
                    
                    <input type = "text" placeholder = "Postcode" required/>
                    
                    <label> Your message </label>
                    <textarea></textarea>
                   
                    </div>
                    <div slot="form-controls">
                        <button v-on:click = //Event handler to handle even of submit button click. 
                        "handleSubmit">Submit</button>
                    </div>
            </form-helper>
        </div>
    </template>
<script>
        import formHelper from './formHelper.vue';
        export default {
            components: {
                'form-helper':formHelper},
            data(){
                return {
                    }
        },
            methods: //Method to handle submit event.
            {handleSubmit:function() 
               {alert('Enquiry submitted.');
            } 
            }
        }
        </script>
