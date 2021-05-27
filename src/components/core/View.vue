<template>
  <div>
    <welcome />

    <about-me />

    <services />

    <recent-projects />

    <get-in-touch />
  </div>
</template>

<script>
  export default {
    name: 'CoreView',
    components: {
      AboutMe: () => import('@/components/AboutMe'),
      GetInTouch: () => import('@/components/GetInTouch'),
      RecentProjects: () => import('@/components/RecentProjects'),
      Services: () => import('@/components/Services'),
      Welcome: () => import('@/components/Welcome'),
    },
  }
</script>
