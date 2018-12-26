<template>
  <div class="hello">
  </div>
</template>
<script>
import axios from 'axios'
export default {
  name: 'HelloWorld',
  data () {
    return {
    }
  },
  mounted () {
    axios.post('http://checklister-api.herokuapp.com/item/create/ ',
      { headers: {'Content-Type': 'application/json'},
        'name': 'gfds',
        'description': '',
        'description_html': ',',
        'details': {
          'address': '',
          'gender': '',
          'mobile': ';'
        },
        'is_complete': 'true',
        'priority': 'H',
        'user': '1'
      })
      .then(response => {
        console.log(response)
      })
      .catch(error => {
        console.log(error.response)
      })
  }
}
</script>
