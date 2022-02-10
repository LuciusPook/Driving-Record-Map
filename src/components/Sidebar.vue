<template>
  <div class="sidebar">
    <div class="container">
      <p><i></i> 軌跡查詢</p>
      <div class="nav-item">
        <div class="nav-items">
          <div class="car-number">
            <label for="" class="number">車號：</label>
            <select name="" id="">
              <option value="" disabled selected>請選擇車號</option>
            </select>
          </div>
          <div class="start-time">
            <label for="">開始時間：</label>
            <input name="a-time-start" type="date" required />
            <div class="time">
              <select name="" id="">
                <option value="">00</option>
              </select>
              <span>時</span>
              <select name="" id="">
                <option value="">00</option>
              </select>
              <span>分</span>
            </div>
          </div>
          <div class="end-time">
            <label for="">結束時間：</label>
            <input name="a-time-start" type="date" required />
            <div class="time">
              <select name="" id="">
                <option value="">00</option>
              </select>
              <span>時</span>
              <select name="" id="">
                <option value="">00</option>
              </select>
              <span>分</span>
            </div>
          </div>
          <button class="searching">查詢</button>
          <div class="another-button">
            <button>播放軌跡</button>
            <button>兩點分析</button>
            <button>儲存路線</button>
            <select name="" id="">
              <option value="">1x</option>
            </select>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.sidebar {
  width: 30%;
  min-height: 100vh;
  background: grey;
}

p {
  margin: 8px 5px;
  font-size: 18px;
  font-weight: bold;
}

.nav-item {
  height: 90vh;
  background: #fff;
  border: 1px solid;
  margin: 0 15px 5px 5px;
}

.nav-items {
  padding: 10px;
}

.nav-items > div {
  margin-bottom: 10px;
}

.time {
  margin-left: 5em;
}

.time > select {
  margin-top: 5px;
}

.searching {
  margin-bottom: 10px;
}

.another-button > button {
  margin-right: 5px;
}
</style>