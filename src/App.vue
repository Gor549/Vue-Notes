<script setup>
import { ref, onMounted, computed } from 'vue';
import AddButton from './components/AddButton.vue';
import Card from './components/Card.vue';
import NoteForm from './components/NoteForm.vue';
import Search from './components/Search.vue';

let isOpen = ref(false);
let editable = ref(null)
let editableIndex = ref(null)
function toggleOpen() {
  if (isOpen.value === true) {
    isOpen.value = false
    editable.value = null
    editableIndex.value = null
  }
  else {
    isOpen.value = true
  }

}
let notes = ref([])
function addNote(title, content) {
  let today = new Date();
  const obj = {
    title: title,
    content: content,
    date: today.toLocaleString()
  }
 
  if (editableIndex.value !== null) {
    notes.value = notes.value.map((item, index) => {
      if (editableIndex.value === index) {
        return obj
      } else {
        return item
      }
    })
  } else {
    notes.value.push(obj)
  }

  isOpen.value = false
  editable.value = null
  editableIndex.value = null

  localStorage.setItem('notes', JSON.stringify(notes.value))
}
function deleteNote(index) {
  notes.value.splice(index, 1)
  localStorage.setItem('notes', JSON.stringify(notes.value))
}

onMounted(() => {
  let savednotes = localStorage.getItem('notes')
  if (savednotes) {
    console.log(savednotes)
    notes.value = JSON.parse(savednotes)
  }

})
let text = ref('')
function onSearch(t) {
  text.value = t
}
let filter = computed(() => notes.value.filter(
  (note) => note.title.includes(text.value)
))


function edit(index, note) {
  editableIndex.value = index
  editable.value = note
  isOpen.value = true
}
</script>
<template>
  <div class="container">
    <div class="header">
      <h1 class="title"> Заметки
      </h1>
      <Search @onSearch="onSearch" />
    </div>
    <AddButton @click="toggleOpen" />
    <NoteForm v-if="isOpen" @onClose="toggleOpen" @onSave="addNote" :note="editable" />
    <div class="pix">
      <Card v-for="(item, index) in filter" :title="item.title" :content="item.content" :date="item.date"
        @delate="deleteNote(index)" @click="edit(index, item)" />

    </div>
  </div>


</template>

<style scoped>
.title {
  color: rgb(217, 160, 102);
  justify-content: center;
  text-align: center;
  font-size: 60px;
  font-weight: 900;
}

.container {
  width: 100%;
  min-height: 100vh;
  background: linear-gradient(128deg, rgba(135, 246, 180, 0.84) 12.75%, rgba(50, 180, 187, 0.67) 83.4%);
  background-image: url("https://symposium.su/wp-content/uploads/2020/07/zametki-vorsatz-600x447.jpg");

}

.pix {
  display: flex;
  gap: 50px;
  justify-content: center;
  flex-wrap: wrap;


}

.header {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 32px;
}
</style>
