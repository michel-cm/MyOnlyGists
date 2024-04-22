<script setup>
import PublicHeadline from '../components/PublicHeadline/PublicHeadline.vue';
import WidgetGroup from '@/modules/reports/components/Widget/Group/Group.vue';
import WidgetGroupLoader from '@/modules/reports/components/Widget/Group/loader.vue';
import WidgetCondensed from '@/modules/reports/components/Widget/Condensed/Condensed.vue';

</script>

<template>
  <PublicHeadline />

  <WidgetGroup>
    <WidgetGroupLoader :loading="true" :amount="3">
      <WidgetCondensed :value="10" label="Gists do total" />
      <WidgetCondensed :value="5" label="Gists gratuitos" />
      <WidgetCondensed :value="5" label="Gists pagos"/>
    </WidgetGroupLoader>
  </WidgetGroup>
</template>