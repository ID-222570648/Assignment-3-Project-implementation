
<script src="https://cdn.jsdelivr.net/npm/vue@2.7.10/dist/vue.js"></script>

<template>
    <div>
        <form-helper>
            <div slot="form-header">//Custom header
                <h3> Fill in your details for order </h3>
                
                </div>

                <div slot="form-fields">// transfered from parent component
                    
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
                    <label> Your message </label>
                    <textarea></textarea>
                    <label> Payment </label>
                    <input type = "text" placeholder = "Card type" required/>
                    <input type = "text" placeholder = "Card number" required/>
                    <input type = "text" placeholder = "CCV" required/>
                    <input v-model="special instruction" placeholder="Write special instruction">
                    <p>Message is: {{ special instruction }}</p>
                   </div>


                    <div slot="form-controls">//Event handler to handle even of submit button click. 
                        <button v-on:click = 
                        "handleSubmit">Place order</button>
                    </div>
            </form-helper>
        </div>
    </template>

    <script>
        import formHelper from './formHelper.vue';
        
        export default {
            components: {
                'form-Helper': form-Helper
            },
            data(){
                return {
                
                }
            },

            method: {//Method to handle submit event.
                handleSubmit: function(){
                    alert('Thanks for your order. We will be in contact with you. ');
                }
            }
        }
        </script>
