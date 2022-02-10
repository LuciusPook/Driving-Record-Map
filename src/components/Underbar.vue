<template>
  <div class="container">
    <div class="main">
      <table class="main-table">
        <thead class="table-head">
          <tr class="table-header">
            <th class="check">檢視</th>
            <th class="id">#</th>
            <th class="time">時間</th>
            <th class="speed">時速</th>
            <th class="state">狀態</th>
            <th class="location">位置</th>
            <th class="kilometer">總里程(KM)</th>
          </tr>
        </thead>
        <tbody class="table-body">
          <tr class="table-content">
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td class="id">1</td>
            <td class="time">2022-01-31 08:30:32</td>
            <td class="speed">15</td>
            <td class="state">行駛中</td>
            <td class="location">新北市泰山區 貴鳳街</td>
            <td class="kilometer">3553.1</td>
          </tr>
          <tr class="table-content">
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td class="id">1</td>
            <td class="time">2022-01-31 08:30:32</td>
            <td class="speed">15</td>
            <td class="state">行駛中</td>
            <td class="location">新北市泰山區 貴鳳街</td>
            <td class="kilometer">3553.1</td>
          </tr>
          <tr class="table-content">
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td class="id">1</td>
            <td class="time">2022-01-31 08:30:32</td>
            <td class="speed">15</td>
            <td class="state">行駛中</td>
            <td class="location">新北市泰山區 貴鳳街</td>
            <td class="kilometer">3553.1</td>
          </tr>
          <tr class="table-content">
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td class="id">1</td>
            <td class="time">2022-01-31 08:30:32</td>
            <td class="speed">15</td>
            <td class="state">行駛中</td>
            <td class="location">新北市泰山區 貴鳳街</td>
            <td class="kilometer">3553.1</td>
          </tr>
          <tr class="table-content">
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td class="id">1</td>
            <td class="time">2022-01-31 08:30:32</td>
            <td class="speed">15</td>
            <td class="state">行駛中</td>
            <td class="location">新北市泰山區 貴鳳街</td>
            <td class="kilometer">3553.1</td>
          </tr>
          <tr class="table-content">
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td class="id">1</td>
            <td class="time">2022-01-31 08:30:32</td>
            <td class="speed">15</td>
            <td class="state">行駛中</td>
            <td class="location">新北市泰山區 貴鳳街</td>
            <td class="kilometer">3553.1</td>
          </tr>
          <tr class="table-content">
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td class="id">1</td>
            <td class="time">2022-01-31 08:30:32</td>
            <td class="speed">15</td>
            <td class="state">行駛中</td>
            <td class="location">新北市泰山區 貴鳳街</td>
            <td class="kilometer">3553.1</td>
          </tr>
          <tr class="table-content">
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td class="id">1</td>
            <td class="time">2022-01-31 08:30:32</td>
            <td class="speed">15</td>
            <td class="state">行駛中</td>
            <td class="location">新北市泰山區 貴鳳街</td>
            <td class="kilometer">3553.1</td>
          </tr>
          <tr class="table-content">
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td class="id">1</td>
            <td class="time">2022-01-31 08:30:32</td>
            <td class="speed">15</td>
            <td class="state">行駛中</td>
            <td class="location">新北市泰山區 貴鳳街</td>
            <td class="kilometer">3553.1</td>
          </tr>
          <tr class="table-content">
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td class="id">1</td>
            <td class="time">2022-01-31 08:30:32</td>
            <td class="speed">15</td>
            <td class="state">行駛中</td>
            <td class="location">新北市泰山區 貴鳳街</td>
            <td class="kilometer">3553.1</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style scoped>
.container {
  position: absolute;
  height: 250px;
  padding: 5px;
  background: grey;
  bottom: 0;
  z-index: 999;
}

.main {
  width: 100%;
  margin-top: 10px;
  background: #fff;
  overflow-y: overlay;
}

.main-table {
  width: 100%;
  padding: 2px;
  max-height: 230px;
}

.table-head {
  position: sticky;
  top: 0;
  z-index: 999;
  width: 100%;
  background: #000;
  color: #fff;
}

.table-body {
  width: 100%;
}

.table-header {
  width: 100%;
  display: flex;
  align-items: center;
}

.table-content {
  width: 100%;
  display: flex;
  align-items: center;
}

.check,
.id {
  min-width: 8%;
  text-align: center;
  border-right: 1px solid;
  border-bottom: 1px solid #000;
}

.check {
  border-left: 1px solid #000;
}

.time {
  min-width: 20%;
  text-align: center;
  border-right: 1px solid;
  border-bottom: 1px solid #000;
}

.speed,
.kilometer {
  min-width: 10%;
  text-align: center;
  border-bottom: 1px solid #000;
}

.speed {
  border-right: 1px solid;
}

.state {
  min-width: 15%;
  text-align: center;
  border-right: 1px solid;
  border-bottom: 1px solid #000;
}

.location {
  min-width: 28%;
  text-align: center;
  border-right: 1px solid;
  border-bottom: 1px solid #000;
}

tbody td.check,
tbody td.id,
tbody td.time,
tbody td.speed,
tbody td.kilometer {
  font-size: 18px;
}

tbody td.state {
  color: rgb(2, 172, 2);
  font-weight: bold;
  border-right-color: #000;
}
</style>
