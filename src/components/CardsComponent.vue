<script setup>
import { Edit, Comment, Setting } from '@element-plus/icons-vue'
import { useRouter } from 'vue-router'

const router = useRouter()

const customers = [
  {
    name: 'Kimberly Hall',
    value: 'Operator'
  },
  {
    name: 'Kimberly Hall',
    value: 'Operator'
  },
  {
    name: 'Kimberly Hall',
    value: 'Operator'
  },
  {
    name: 'Kimberly Hall',
    value: 'Operator'
  }
]
const items = [
  {
    name: 'Andrey',
    value: 'Player'
  },
  {
    name: 'Ivan',
    value: 'Player'
  }
]
const actions = [
  {
    name: 'Andrey',
    value: '+795165681515'
  }
]
</script>

<template>
<div class="cards">
  <el-card class="card">
    <template #header>
      <div class="card-header">
        <strong>Card name</strong>
        <el-icon :size="23">
          <Edit />
        </el-icon>
      </div>
    </template>
    <div >
      <el-row>
        <el-col class="item" v-for="(item, index) in customers" :key="index" :span="12">
          <span class="name">{{item.name}}</span>
          <span class="value">{{item.value}}</span>
        </el-col>
      </el-row>
    </div>
  </el-card>
  <el-card class="card">
    <template #header>
      <div class="card-header">
        <strong>Card name</strong>
        <el-icon :size="23">
          <Comment />
        </el-icon>
      </div>
    </template>
    <div >
      <el-row>
        <el-col class="item" v-for="(item, index) in items" :key="index" :span="12">
          <span class="name">{{item.name}}</span>
          <span class="value">{{item.value}}</span>
        </el-col>
      </el-row>
    </div>
  </el-card>
  <el-card class="card">
    <template #header>
      <div class="card-header">
        <strong>Card name</strong>
        <el-icon :size="23">
          <Setting />
        </el-icon>
      </div>
    </template>
    <div >
      <el-row>
        <el-col class="item" v-for="(item, index) in actions" :key="index" :span="12">
          <span class="name">{{item.name}}</span>
          <span class="value">{{item.value}}</span>
        </el-col>
      </el-row>
    </div>
    <template #footer>
      <div class="card-footer">
        <el-button type="warning" @click="router.push({name: 'some.actions'})">Go to actions</el-button>
      </div>
    </template>
  </el-card>
</div>
</template>

<style scoped>
.cards {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  column-gap: 30px;
}
.card {
  width: 500px;
  margin-bottom: 20px;
}
.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.item {
  display: grid;
  margin: 15px 0;
  text-align: start;
}
.name {
  font-size: 18px;
}
.value {
  color: #646262FF;
  font-weight: bold;
  font-size: 18px;
}
</style>
