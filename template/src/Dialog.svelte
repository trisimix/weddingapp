<script>
    import { getContext } from 'svelte';
    import Confet from "./Confet.svelte"
    export let message;
      export let hasForm = false;
      export let onCancel = () => {};
      export let onOkay = () => {};
  
    const { close } = getContext('simple-modal');
      
      let value;
      let onChange = () => {};
      
      function _onCancel() {
          onCancel();
          close();
      }
      
      function _onOkay() {
          onOkay(value);
          close();
      }
      
      $: onChange(value)
  </script>
  
  <style>
    label {
        font-family: 'open sans',arial,sans-serif;
		

    }
    h2 {
          font-size: 2rem;
          text-align: center;
      }
      
      input {
          width: 100%;
      }
      
      .buttons {
          display: flex;
          justify-content: space-between;
      }
  </style>
  
  <!-- <h2>{message}</h2>-->
  <Confet ></Confet>
 <h2>
  <!-- modify this form HTML and place wherever you want your form -->
<form
  action="https://formspree.io/f/mnqwgjpl"
  method="POST"
>
  <label>
    Your email:
    <input style="border-radius: 25px;border:1px solid black" type="email" name="email">
  </label>
  <label>
    Your name:
    <input style="border:1px solid black;border-radius: 25px;" type="name" name="name">
  </label>
  <!-- your other form fields go here -->
  <label>
    How many adults?:
    <input type="number" style="border-radius: 25px;border:1px solid black;width:25%" name="adults" value="1">
  </label>
  <label>
    How many children?:
    <input type="number" style="border-radius: 25px;border:1px solid black;width:25%" name="children" value="0">
  </label>
  <button style="font-family: 'open sans',arial,sans-serif;
		font-size: 1em" type="submit">Send</button>
</form>
</h2> 