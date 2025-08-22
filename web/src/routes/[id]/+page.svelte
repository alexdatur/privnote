<script lang="ts">
  import { page } from '$app/stores';
  import Debug from '$lib/components/utils/Debug.svelte';
  import ReadNote from '$lib/components/pages/note/ReadNote.svelte';
  import ConfirmReadNote from '$lib/components/pages/note/ConfirmReadNote.svelte';
  import type { Messages, ResponseBody } from '$lib/@types';

  export let data: ResponseBody<Boolean>;

  $: shouldAskPassword = ($page.form?.messages as Messages[] | undefined)?.some(
    (m: Messages) => m.path === 'body' || m.path === 'manual_password'
  );
  $: hasNoteData = Boolean((($page.form?.data as any)?.note) || ((data as any)?.data?.note));
</script>

<Debug />

{#if shouldAskPassword || hasNoteData || !data?.data}
  <ReadNote />
{:else}
  <ConfirmReadNote />
{/if}
