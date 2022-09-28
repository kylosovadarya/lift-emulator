<template>
  <div class="main-page">
    <div class="lift">
      <div v-for="floor in floors" :key="`${{floor}}th + floor`" class="floor">
        <div class="cabin">
          <div class="indicator"></div>
        </div>
        <button class="floor-btn">{{floor}}</button>
      </div>
      <button class="remove-lift-btn">Remove this lift</button>
    </div>
    <div class="settings">
      <label for="floors-count">Floors count: </label>
      <select>
        <option v-for="floor in floors">{{floor}}</option>
      </select>
      <button class="add-lift-btn">+ Add lift</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      floors: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
    }
  }
}
</script>

<style>
html,
body {
  margin: 0;
  padding: 0;
}

.main-page {
  display: flex;
  align-items: center;
  gap: 80px;
}

.lift {
  display: flex;
  flex-direction: column-reverse;
  justify-content: space-between;
  height: 90vh;
  margin: 40px;
}

.floor {
  display: flex;
  align-items: center;
  flex-grow: 1;
  gap: 32px;
}

.cabin {
  border: 1px solid #9a9a9a;
  width: 80px;
  height: 100%;
}

.indicator {
  border: 1px solid #9a9a9a;
  width: 80%;
  height: 60%;
  margin: auto;
  margin-top: 10%;
  border-radius: 8px;

}

button {
  border: 1px solid;
  display: block;
}

.settings {
  margin: 40px;
}

.remove-lift-btn {
  margin-bottom: 15px;
  padding: 8px;
  border-radius: 8px;
}

.add-lift-btn {
  padding: 8px;
  border-radius: 8px;
  margin-top: 8px;
}
</style>
