<template>
  <v-container fluid>
    <v-card>
      <v-toolbar dense flat>
        <v-toolbar-title>문서편집기</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn icon>
          <v-icon>mdi-eye</v-icon>
        </v-btn>
      </v-toolbar>
      <v-card-text>
        <v-textarea v-model="text"></v-textarea>
      </v-card-text>
      <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn @click="read">read</v-btn>
        <v-btn @click="write">write</v-btn>
      </v-card-actions>
    </v-card>
  </v-container>
</template>
<script>
const { dialog } = require('electron')
export default {
  data () {
    return {
      text: ''
    }
  },
  mothods: {
    read () {
      const r = dialog.showOpenDialogSync()
      console.log(r)
    },
    write () {

    }
  }
}
</script>
