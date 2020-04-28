<template>
  <div class="note-container">
    
    <note-selectors />
    <!-- note editor was here -->
    <note-editor />
  </div>
</template>


<script>
import NoteSelectors from "@/components/NoteSelectors"
import NoteEditor from "@/components/NoteEditor"

export default {
  name: 'note-container',
  components: {
    NoteSelectors,
    NoteEditor
  }
}
</script>