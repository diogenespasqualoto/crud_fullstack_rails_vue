:<template>
  <div>
    <h1>posts</h1>

    <!-- Cria o post -->
    <input
      type="text"
      v-model="title"
      placeholder="Title"
      class="title-input"
    />
    <input type="text" v-model="body" placeholder="Body" class="body-input" />

    <!-- apenas renderiza se estiver editando o post -->
    <button v-if="isEditing" @click="updatePost">Update</button>
    <button v-if="isEditing" @click="cenelEdit">Cancel</button>
  </div>
</template>

<script setup>
const updatePost = async () => {
  return true;
};
const cancelEdit = () => {
  return true;
};
</script>

<style scoped>
.title-input {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  box-sizing: border-box;
  border: 2px solid #ccc;
  background-color: #f8f8f8;
  color: #111;
  border-radius: 4px;
  resize: vertical;
}

.body-input {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  box-sizing: border-box;
  border: 2px solid #ccc;
  background-color: #f8f8f8;
  color: #111;
  border-radius: 4px;
  resize: vertical;
}
</style>