<article class="stack">
  <h1>Dashboard</h1>
  <h2>Willkommen bei deiner Offline Challenge</h2>
  <p>Schön, dass du den Weg zu uns gefunden hast. Du kannst dich hier anmelden und direkt an einer der zahlreichen Herausforderungen teilnehmen.</p>
  <form class="stack" action="#">
    <div>
      <label for="frm-text-1">Name:</label>
      <input type="text" name="text-1" id="frm-text-1">
    </div>
    <div>
      <label for="frm-select-1">Worum geht es in der Challenge?</label>
      <div class="select">
        <select name="select-1" id="frm-select-1">
          <option value="a">Schritte</option>
          <option value="b">Liegestütze</option>
          <option value="c">Kniebeugen</option>
        </select>
      </div>
    </div>
    <fieldset class="stack stack-small">
      <legend>Darf es etwas mehr sein?</legend>
      <div>
        <input checked class="visually-hidden" type="checkbox" name="check-1" id="frm-check-1">
        <label for="frm-check-1">Die Waschmaschine nehme ich mit</label>
      </div>
      <div>
        <input class="visually-hidden" type="checkbox" name="check-2" id="frm-check-2">
        <label for="frm-check-2">Und den Trockner noch dazu</label>
      </div>
    </fieldset>
    <fieldset class="stack stack-small">
      <legend>Hier gilt es sich zu entscheiden</legend>
      <div>
        <input checked type="radio" name="radio-1" id="frm-radio-1-a" class="visually-hidden">
        <label for="frm-radio-1-a">Ich möchte die Waschmaschine</label>
      </div>
      <div>
        <input type="radio" name="radio-1" id="frm-radio-1-b" class="visually-hidden">
        <label for="frm-radio-1-b">Ich möchte den Trockner</label>
      </div>
    </fieldset>
    <div class="controls">
      <button class="primary">Ich will mitmachen!</button>
      <button class="alternate">Mehr erfahren</button>
    </div>
  </form>
</article>
