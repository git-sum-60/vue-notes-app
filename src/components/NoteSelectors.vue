<template>
  <div class="note-selectors">
    <!-- note seelcor was here -->
    <note-selector v-for="note in notes" v-bind:key="note.id" v-bind:note="note" v-bind:selectedNoteId="selectedNoteId" v-on:selectNote="selectNote" />
  </div>
</template>

<script>
import NoteSelector from './NoteSelector'

export default {
  name: 'note-selectors',
  components: {
    NoteSelector
  },
  data: function() {
    return {
    }
  },
  props: [
    "notes", "selectedNoteId"
  ],
  methods: {
    selectNote: function(note) {
      console.log(note.id)
      this.$emit("selectNote", note)
      // this.selectedNoteId = note.id
    }
  }
}
</script>