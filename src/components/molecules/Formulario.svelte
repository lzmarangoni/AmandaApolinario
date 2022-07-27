<script>
import ButtonSecondary from "../atoms/ButtonSecondary.svelte";
import InputFormulario from "../atoms/inputFormulario.svelte";
import TextArea from "./TextArea.svelte";
import CloseForm from "../atoms/CloseForm.svelte";
import axios from "axios";

let url = "https://sac-api.vercel.app/api/leads_amanda/insert";


</script>
<form on:submit={async (event)=>{
    event.preventDefault();
    let formulario = event.target
    const dados = {
        created_date: new Date(),
        nome: formulario.nome.value,
        email: formulario.email.value,
        telefone: formulario.telefone.value,    
        assunto: formulario.assunto.value,
        mensagem: formulario.mensagem.value,
    }
    await axios.post(url, dados)
    console.log(dados)  


}} class="pl-2 pr-42 md:p-5 fixed top-14 md:left-96 w-full h-full md:w-1/2 md:h-1/2 ">
    <div class="flex justify-end">
        <CloseForm/>
    </div>
    <InputFormulario name='nome' label={["Nome"]} placeholder={["Qual o seu nome?"]} type="text"/>
    <InputFormulario name={["email"]} label={["E-mail"]} placeholder={["Informe o seu melhor e-mail para contato"]} type="email"/>
        <div class="md:flex">
            <InputFormulario name={["telefone"]} class="md:w-2/5" label={["Telefone"]} placeholder={["(xx)xxxxx-xxxx"]} type="tel" />
            <InputFormulario name={["assunto"]} class="md:w-3/5" label={["Assunto"]} placeholder={["Por qual motivo está nos contatando?"]} type="text" />
        </div>  
    <TextArea name={["mensagem"]} label={["Mensagem"]} placeholder={["Fique a vontade para nos contar o que precisa..."]}/>
    <div class="flex justify-end">
        <ButtonSecondary class="m-2 pl-auto">Enviar</ButtonSecondary>
    </div>
</form>

