<template>
  <h2>Форма для добавления элементов массива в Vue</h2>
  <input type="text" v-model="newItem">
  <button @click="addTask">добавить дело</button>
  <ul>
    <li v-for="(item, index) in items" :key="index">
      {{ item }}
      <button @click="removeTask">delete</button>
    </li>
  </ul>

  <div>
    <h2>Кнопка для удаления из массива объектов в Vue</h2>
    <ul>
      <li v-for="user in users" :key="user.id">
        {{ user.name }}
        {{ user.surn }}
        <button @click="removeItem(user.id)">remove</button>
      </li>
    </ul>
  </div>

  <div>
    <h2>Форма для редактирования массива объектов в Vue</h2>
    <ul>
      <li v-for="user in users" :key="user.id">
        <template v-if="!user.isEdit">
          {{ user.name }}
          {{ user.surn }}
          <button @click="edit(user)">
            edit
          </button>
        </template>
        <template v-else>
          <input v-model="user.name">
          <input v-model="user.surn">
          <button @click="save(user)">
            save
          </button>
        </template>
		  </li>
	</ul>
  </div>

</template>

<script>
  export default {
    data() {
      return {
        newItem: '',
        items: ['abc', 'cde', 'fgh'],
        users: [
          {
            id: 1,
            name: 'name1',
            surn: 'surn1',
          },
          {
            id: 2,
            name: 'name2',
            surn: 'surn2',
          },
          {
            id: 3,
            name: 'name3',
            surn: 'surn3',
          },
        ],
        users2: [
          {
            id: 1,
            name: 'name1',
            surn: 'surn1',
            isEdit: false,
          },
          {
            id: 2,
            name: 'name2',
            surn: 'surn2',
            isEdit: false,
          },
          {
            id: 3,
            name: 'name3',
            surn: 'surn3',
            isEdit: false,
          },
        ]
      }
    },
    methods: {
      addTask: function() {
        this.items.unshift(this.newItem);
      },
      removeTask: function(index) {
        this.items.splice(index, 1);
      },
      removeItem: function(id) {
        this.users = this.users.filter((user) => {
          return user.id !== id;
        })
      },
      edit(user) {
        user.isEdit = true;
      },
      save(user) {
        user.isEdit = false;
      },
    }
  }
</script>