<script>
    export default{
        
        props: ['archivoUno','archivo'],

        data(){
            return{
                count:0,
                
            }
        }
    }
    
</script>

<template>
    <li>  
        <input type="checkbox" class="mr-2" @click="check=true" >{{archivo.titulo}}
        <div>
            Descripción: {{archivo.descripcion}} <br>
            Entregable:{{archivo.Entregable}}
            
            
            

        </div>
         

        
        

        
    </li>
</template>