<template>
  <div>
    <button v-if="$i18n.locale === 'de'" @click="setLocale('en')">
      <img
        src="/svg/flags/de.svg"
        class="h-6 w-6 text-second-600 group-hover:text-second-500 dark:text-second-400"
        aria-hidden="true"
        alt="DE"
      />
    </button>
    <button v-else-if="$i18n.locale === 'en'" @click="setLocale('de')">
      <img
        src="/svg/flags/uk.svg"
        class="h-6 w-6 text-second-600 group-hover:text-second-500 dark:text-second-400"
        aria-hidden="true"
        alt="UK"
      />
    </button>
  </div>
</template>

<script lang="ts">
import {
  ComputerDesktopIcon,
  MoonIcon,
  SunIcon,
} from '@heroicons/vue/24/outline';

export default defineComponent({
  name: 'SettingLang',
  components: {
    ComputerDesktopIcon,
    MoonIcon,
    SunIcon,
  },
  setup() {
    return {
      setLocale: useI18n().setLocale,
    };
  },
});
</script>
