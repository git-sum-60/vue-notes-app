<template>
  <div class="note-container">
    
    <note-selectors v-bind:notes="notes" v-on:selectNote="selectNote" v-bind:selectedNoteId="selectedNoteId"/>
    <!-- note editor was here -->
    <note-editor />
  </div>
</template>


<script>
import NoteSelectors from "@/components/NoteSelectors"
// import NoteSelectors from "./NoteSelectors"
import NoteEditor from "./NoteEditor"

export default {
  name: 'note-container',
  components: {
    NoteSelectors,
    NoteEditor
  },
  props: [
    "notes",
    "selectedNoteId"
  ],
  methods: {
    selectNote: function(note) {
      this.$emit("selectNote", note)
    }
  }
}
</script>