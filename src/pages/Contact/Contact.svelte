
<script>

import { toasts } from "svelte-toasts";

let fromEmail;
let subject;
let text;

async function handleSubmit(e){

    e.preventDefault();
  

    const response = await fetch("http://localhost:3000/send", {
        method: 'POST',
        body: JSON.stringify({
            fromEmail,
            subject,
            text
        }),
        headers: {
            "Content-type": "application/json; charset=UTF-8"
        }
    })
    const json = await response.json();

    const contactForm = document.getElementById("contactForm");
    contactForm.reset();
    toasts.success("Mail sent successfully!");
}

</script>




<div class="headline">
    <h1>Contact</h1>
</div>

<div id="formDiv">

    <form id = "contactForm" on:submit={handleSubmit} >
        *<input id="fromField" bind:value={fromEmail} placeholder="Email" required><br>
        *<input id="subjectField" bind:value={subject} placeholder="Subject" required><br>
        *<textarea id="textField" bind:value={text} placeholder="Type here..." cols="40" rows="5" required></textarea>
        <button id="sendInfo" type="submit">Send</button>
    </form>
    



</div>