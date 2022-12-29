<script>
	import Header from '../Header.svelte';
	import { supabaseClient } from '$lib/db'
	import { invalidate } from '$app/navigation'
	import { onMount } from 'svelte'

	onMount(() => {
		const { data: { subscription } } = supabaseClient.auth.onAuthStateChange(() => {
			invalidate('supabase:auth')
		});
		console.log(subscription)

		return () => {
		subscription.unsubscribe()
		}
	})
</script>

<div>
	<Header />
	<main>
		<slot />
	</main>

	<footer class="py-5 container-footer">
		<div class="row">
		  <div class="col-3">
			<h5>Section</h5>
			<ul class="nav flex-column">
			  <li class="nav-item mb-2"><a href="/" class="nav-link p-0 text-muted">Acceuil</a></li>
			  <li class="nav-item mb-2"><a href="/about" class="nav-link p-0 text-muted">A propos de nous</a></li>
			  <li class="nav-item mb-2"><a href="/business" class="nav-link p-0 text-muted">For Business</a></li>
			  <li class="nav-item mb-2"><a href="/connexion" class="nav-link p-0 text-muted">Connexion</a></li>
			  <li class="nav-item mb-2"><a href="/inscription" class="nav-link p-0 text-muted">Inscription</a></li>
			</ul>
		  </div>
	
		  <div class="col-4 offset-1">
			<form>
			  <h5>Souscrivez à notre newsletter</h5>
			  <p>Résumé mensuel de ce qui est nouveau et passionnant de notre part.</p>
			  <div class="d-flex w-100 gap-2">
				<label for="newsletter1" class="visually-hidden">Adresse Email</label>
				<input id="newsletter1" type="text" class="form-control" placeholder="Email address">
				<button class="btn btn-primary" type="button">Souscrivez</button>
			  </div>
			</form>
		  </div>
		</div>
	
		<div class="d-flex justify-content-between py-4 my-4 border-top">
			<img src="/images/nobg.jpg" width="50" height="50" alt="ok"/>
			&copy; 2022 Company, Inc. Tous les droits sont réservés.
			<div>Riviera Golf,Tour DIVAT 8ème étage</div>
			<div>+225 27 22 43 49 09 / +225 07 79 41 39 69</div>
			<ul class="list-unstyled d-flex">
				<li class="ms-3">
					<a class="link-dark" href="https://www.linkedin.com/company/nov-act/">
						<img src="/images/LinkedIn_icon.png" width="24" height="24" alt="ok"> 
						<use xlink:href="linkedin"/>
					</a>
				</li>
			</ul>
		</div>
	  </footer>
</div>