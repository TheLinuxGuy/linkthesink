<script setup>
import { BloggerIcon, GitHubIcon, GmailIcon, MastodonIcon, TelegramIcon, XIcon } from 'vue3-simple-icons'

const { title, email, telegram, blog, twitter, mastodon, github } = useAppConfig()
</script>

<template>
  <section class="md:pt-6">
    <div class="container flex flex-col items-center py-8 mx-auto sm:flex-row">
      <a
        href="https://a.mazzeo.me"
        class="text-xl font-black leading-none text-gray-900 select-none dark:text-gray-100 logo"
        :title="title"
      >{{ title }}</a>
      <a
        class="mt-4 text-sm text-gray-500 sm:ml-4 sm:pl-4 sm:border-l sm:border-gray-200 sm:mt-0"
        href="https://mazzeo.me"
        target="_blank"
        title="Mazzeo"
      >
        &copy; {{ new Date().getFullYear() }} mazzeo.me
      </a>
      <span
        class="inline-flex justify-center mt-4 space-x-5 sm:ml-auto sm:mt-0 sm:justify-start"
      >
        <a
          v-if="email"
          :href="`mailto:${email}`"
          title="Email"
          class="text-gray-400 hover:text-gray-500"
        >
          <span class="sr-only">{{ $t('layouts.footer.social.email') }}</span>
          <GmailIcon
            class="w-6 h-6"
          />
        </a>
        <a
          v-if="telegram"
          :href="telegram"
          target="_blank"
          title="Telegram"
          class="text-gray-400 hover:text-gray-500"
        >
          <span class="sr-only">{{ $t('layouts.footer.social.telegram') }}</span>
          <TelegramIcon
            class="w-6 h-6"
          />
        </a>
        <a
          v-if="blog"
          :href="blog"
          target="_blank"
          title="Blog"
          class="text-gray-400 hover:text-gray-500"
        >
          <span class="sr-only">{{ $t('layouts.footer.social.blog') }}</span>
          <BloggerIcon
            class="w-6 h-6"
          />
        </a>

        <a
          v-if="twitter"
          :href="twitter"
          target="_blank"
          title="Twitter"
          class="text-gray-400 hover:text-gray-500"
        >
          <span class="sr-only">{{ $t('layouts.footer.social.twitter') }}</span>
          <XIcon
            class="w-6 h-6"
          />
        </a>

        <a
          v-if="mastodon"
          :href="mastodon"
          target="_blank"
          title="Mastodon"
          class="text-gray-400 hover:text-gray-500"
        >
          <span class="sr-only">{{ $t('layouts.footer.social.mastodon') }}</span>
          <MastodonIcon
            class="w-6 h-6"
          />
        </a>

        <a
          v-if="github"
          :href="github"
          target="_blank"
          title="GitHub"
          class="text-gray-400 hover:text-gray-500"
        >
          <span class="sr-only">{{ $t('layouts.footer.social.github') }}</span>
          <GitHubIcon
            class="w-6 h-6"
          />
        </a>
      </span>
    </div>
  </section>
</template>
