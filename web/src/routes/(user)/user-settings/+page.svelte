<script lang="ts">
  import UserPageLayout from '$lib/components/layouts/user-page-layout.svelte';
  import UserSettingsList from '$lib/components/user-settings-page/user-settings-list.svelte';
  import type { PageData } from './$types';

  export let data: PageData;
</script>

<UserPageLayout user={data.user} title={data.meta.title}>
  <section class="mx-4 flex place-content-center">
    <div class="w-full max-w-3xl">
      <UserSettingsList user={data.user} keys={data.keys} devices={data.devices} partners={data.partners} />
    </div>
  </section>
</UserPageLayout>
