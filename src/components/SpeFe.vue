<template>
  <v-table>
    <thead>
      <tr>
        <th class="text-left">
          Code
        </th>
        <th class="text-left">
          Name
        </th>
        <th class="text-left">
          Quantity
        </th>
      </tr>
    </thead>
    <tbody>
      <tr
        v-for="data in datas"
        :key="data.name"
      >
        <td>{{ data.product.code }}</td>
        <td>{{ data.product.name }}</td>
        <td>{{ data.quantity }}</td>
      </tr>
    </tbody>
  </v-table>
</template>
<script>
  export default {
    data () {
      return {
        datas:{},
        desserts: [
          {
            name: 'Frozen Yogurt',
            calories: 159,
          },
          {
            name: 'Ice cream sandwich',
            calories: 237,
          },
          {
            name: 'Eclair',
            calories: 262,
          },
          {
            name: 'Cupcake',
            calories: 305,
          },
          {
            name: 'Gingerbread',
            calories: 356,
          },
          {
            name: 'Jelly bean',
            calories: 375,
          },
          {
            name: 'Lollipop',
            calories: 392,
          },
          {
            name: 'Honeycomb',
            calories: 408,
          },
          {
            name: 'Donut',
            calories: 452,
          },
          {
            name: 'KitKat',
            calories: 518,
          },
        ],
      }
    },
    methods: {
      getData(){
        const headers = { 
          "Content-Type": "application/json",
          "Authorization": "Bearer o7Ytbt9XQLI3PgtebJfKSXKEf0XHU74Y" 
        
        };
        fetch("https://spe-academy.spesolution.net/api/recruitment",{ headers })

        .then(res => res.json())
        .then(data => {
          this.datas = data
          console.log(this.datas);
        })
      }
    },
    mounted() {
      this.getData()
    },
  }
</script>