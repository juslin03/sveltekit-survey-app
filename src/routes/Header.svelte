<script lang="ts">
  import { applyAction, enhance, type SubmitFunction } from '$app/forms';
	import { invalidate } from '$app/navigation';
	import { page } from '$app/stores';

	let loading = false;
	const handleLogout: SubmitFunction = () => {
		loading = true;
		return async ({ result }) => {
			if (result.type === 'redirect') {
				await invalidate('supabase:auth');
			} else {
				await applyAction(result);
			}
			loading = false;
		};
	};
</script>

<header>
    <nav class="navbar navbar-expand-md ">
      <div class="container-fluid">
        <img src="/images/nobg.jpg"width="50" height="50" class="d-inline-block align-text-top mr-3" alt="aucun"/>
      <button class=" navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarCollapse" aria-controls="navbarCollapse" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarCollapse">
          <ul class="navbar-nav me-auto mb-2 mb-md-0">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="/">Accueil</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="/about">A propos de nous</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="/business">For Business</a>
            </li>
          </ul>
          <div class="d-flex">
            <ul class="navbar-nav me-auto mb-2 mb-md-0">
              {#if $page.data.session}
              <form action="/logout" method="post" use:enhance={handleLogout}>
                <button disabled={loading} type="submit">Sign out</button>
              </form>
              {:else}
                <li class="nav-item">
                  <a class="nav-link" href="/connexion">Connexion</a>
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="/inscription">Inscription</a>
                </li>
              {/if}
            </ul>
        </div>
      </div>
    </nav>
</header>