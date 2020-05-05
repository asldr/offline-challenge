<script>
  import { v4 as uuidv4 } from "uuid";
  function submitForm() {
    let name = document.querySelector("input[name='text-1']").value;
    let data = {};

    data.uuid = uuidv4();
    name ? (data.name = name) : (data.name = null);

    fetch("http://localhost:1337/participants", {
      method: "POST",
      headers: {
        "Content-Type": "application/json"
      },
      body: JSON.stringify(data)
    })
      .then(response => response.json())
      .then(data => {
        let userData = {};
        userData.name = data.name;
        userData.uuid = data.uuid;
        localStorage.setItem("userData", JSON.stringify(userData));
      });
  }
</script>

<article class="stack">
  <h1>Sei dabei!</h1>
  <h2>Hier legen wir dir erstmal ein Konto an</h2>
  <p>
    Schön, dass du den Weg zu uns gefunden hast. Du kannst dich hier anmelden
    und direkt an einer der zahlreichen Herausforderungen teilnehmen.
  </p>
  <p>
    Bei uns musst du keinen Namen angeben, aber es hilft dabei, dich als dich zu
    identifizieren.
  </p>
  <form class="stack" action="#">
    <div>
      <label for="frm-text-1">Name:</label>
      <input type="text" name="text-1" id="frm-text-1" />
    </div>
    <div class="controls">
      <button on:click|preventDefault={submitForm} class="primary">
        Ich will mitmachen!
      </button>
      <button class="alternate">Mehr erfahren</button>
    </div>
  </form>
</article>
