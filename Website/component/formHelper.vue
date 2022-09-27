  
  /** This file demonstrates use of slot to pass HTML 
  * element like headers, paragraphs and input fields.
  * This file works like a basic structure template of similar forms,
  * When more then one for is involved. So it streamlines the process of coding.*/
  <template>
    <div>
        <h1>
           Client enquiry form 
        </h1>
        /* Following code is to create all parts of the basic structure of a form.*/
        <form>
            <div id="form-header"> 
                <slot name = "form-header"></slot>
            </div>
            <div id="form-fields">
                <slot name = "form-fields"></slot> 
            </div>
            <div id="form-controls">
                <slot name = "form-controls"></slot>
            </div>

            </form>
    </div>
    </template>

    <script>
        /*https://www.youtube.com/watch?v=09n2945JW_0&list=PL4cUxeGkcC9gQcYgjhBoeQH7wiAyZNrYa&index=27
        https://www.youtube.com/watch?v=F44OoFk8spg&list=PL4cUxeGkcC9gQcYgjhBoeQH7wiAyZNrYa&index=28*/
        export default {
            components: {

            },
            data (){
                return {

                }
            },
            methods:{

            }
        }
    </script>