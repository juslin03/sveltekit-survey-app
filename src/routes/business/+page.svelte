<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<form>
    <div class="nom-form-group">
      <label for="exampleFormControlTextarea1">Nom</label>
      <textarea class="form-control" id="exampleFormControlTextarea1" rows="1"></textarea>
    </div>
    <div class="prenom-form-group">
      <label for="exampleFormControlTextarea1">Prenoms</label>
      <textarea class="form-control" id="exampleFormControlTextarea1" rows="1"></textarea>
    </div>
    <div class="form-container for-business-container">
      <label for="exampleFormControlInput1">Adresse email</label>
      <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="name@example.com">
    </div>
    <div class="form-container -container">
      <label for="exampleFormControlInput1">Contact</label>
      <input type="contact" class="form-control" id="exampleFormControlInput1" placeholder="">
    </div>
    <div class="form-group">
      <label for="exampleFormControlTextarea1">Ecrivez votre préoccupation</label>
      <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
    </div>
    <div class="form-check">
      <input type="checkbox" class="form-check-input" id="exampleCheck1">
      <label class="form-check-label" for="exampleCheck1">Enregistrer moi</label>
    </div>
    <button type="submit" class="btn btn-primary">Envoyez</button>
</form>