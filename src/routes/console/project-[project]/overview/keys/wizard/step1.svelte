<script lang="ts">
    import { FormList, InputText } from '$lib/elements/forms';
    import { WizardStep } from '$lib/layout';
    import ExpirationInput from '../expirationInput.svelte';
    import { key } from './store';
</script>

<WizardStep>
    <svelte:fragment slot="title">Create an API Key</svelte:fragment>
    <svelte:fragment slot="subtitle">Let's create an API Key.</svelte:fragment>
    <FormList>
        <InputText
            id="name"
            label="Name"
            placeholder="API Key Name"
            required
            bind:value={$key.name} />
        <ExpirationInput bind:value={$key.expire} />
    </FormList>
</WizardStep>
