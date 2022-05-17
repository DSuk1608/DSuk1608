<template>
  <div class="mx-6 relative overflow-x-auto shadow-md sm:rounded-lg">
    <table class="  w-full text-sm text-left text-gray-500 dark:text-gray-400">
      <thead class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
      <tr>
        <th scope="col" class="px-6 py-3">Name</th>
        <th scope="col" class="px-6 py-3">Category</th>
        <th scope="col" class="px-6 py-3">Role</th>
        <th scope="col" class="px-6 py-3">E-Mail</th>
        <th scope="col" class=" text-right px-6 py-3">Edit
          <span class="sr-only">Edit</span>
        </th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="user in users" :key="user" class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
        <th scope="row" class="px-6 py-4 font-medium text-gray-900 dark:text-white whitespace-nowrap">
          {{user.firstName}} {{user.lastName}}
        </th>
        <td class="px-6 py-4">
          {{ user.department }}
        </td>
        <td class="px-6 py-4">
          {{ user.role }}
        </td>
        <td class="px-6 py-4">
          {{ user.email }}
        </td>
        <td class="px-6 py-4 text-right">
          <a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline">Edit</a>
        </td>
      </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Users",
  data(){
    return {
      users: [
        { firstName: 'Frank', lastName: 'Murphy', email: 'frank.murphy@test.com', role: 'User' , department:'-' },
        { firstName: 'Vic', lastName: 'Reynolds', email: 'vic.reynolds@test.com', role: 'Admin', department:'Developer' },
        { firstName: 'Gina', lastName: 'Jabowski', email: 'gina.jabowski@test.com', role: 'Admin' , department:'Developer'},
        { firstName: 'Jessi', lastName: 'Glaser', email: 'jessi.glaser@test.com', role: 'User', department:'Administration' },
        { firstName: 'Jay', lastName: 'Bilzerian', email: 'jay.bilzerian@test.com', role: 'User', department:'Stagiar' }
      ]
    };
  }

}
</script>

<style scoped>
tbody tr:nth-of-type(even) {
  background-color: rgba(236, 237, 237);
}

tbody tr:nth-of-type(odd) {
  background-color: rgb(250 ,250, 250);
}

</style>
