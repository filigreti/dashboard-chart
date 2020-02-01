<template>
  <main class="home">
    <div class="d-flex justify-content-between align-items-center">
      <h3 class="dashboard">Dashboard</h3>
      <div class="date">20 Dec 2019, Friday</div>
    </div>
    <div class="d-flex head-count">
      <div class="budget ">
        <div class="first-budget card-shadow">
          <div class="budget-header d-flex justify-content-between">
            <div class="d-flex align-items-center">
              <img src="@/assets/purple.svg" alt="" />
              <div class="status-heading">
                Total Annual CAPEX Budget
              </div>

              <b-button class="ml-3 purp p-1 px-3" size="sm"
                >N50,000,000</b-button
              >
            </div>
            <b-dropdown
              size="sm"
              variant="success"
              class="mr-3 annual"
              id="dropdown-right"
              right
              text="Annual"
            >
              <b-dropdown-item-button>Action</b-dropdown-item-button>
              <b-dropdown-item-button>Another action</b-dropdown-item-button>
              <b-dropdown-item-button
                >Something else here...</b-dropdown-item-button
              >
            </b-dropdown>
          </div>
          <div class=" budget-body d-flex align-items-center ">
            <div class="w-50 justify-content-center d-flex">
              <CircleRadial
                :Diameter="130"
                :color="'#6915cf'"
                :colorTwo="'#6915cf'"
                :completedSteps="64"
                :background="'#e5e5e5'"
                :width="8"
              />
            </div>

            <div class="w-50">
              <div class="d-flex align-item-center mb-3">
                <img src="@/assets/GreenMoney.svg" alt="" />
                <div class="spacing">
                  <div style="font-size:14px">Total <b>CAPEX</b> Spent</div>
                  <div class="text-black-one">N 18,000,000</div>
                </div>
              </div>
              <div class="d-flex align-item-center mt-2">
                <img src="@/assets/Redmoney.svg" alt="" />
                <div class="spacing">
                  <div style="font-size:14px">Total <b>CAPEX</b> Balance</div>
                  <div class="text-black-one">N 32,000,000</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="second-budget card-shadow ">
          <div class="budget-header d-flex justify-content-between">
            <div class=" d-flex align-items-center">
              <img src="@/assets/green-chart.svg" alt="" />
              <div class="status-heading">
                Total Annual OPEX Budget
              </div>
              <b-button class="ml-3 green p-1 px-3" size="sm"
                >N20,000,000</b-button
              >
            </div>
            <b-dropdown
              size="sm"
              variant="success"
              class="mr-3 annual"
              id="dropdown-right"
              right
              text="Annual"
            >
              <b-dropdown-item-button>Action</b-dropdown-item-button>
              <b-dropdown-item-button>Another action</b-dropdown-item-button>
              <b-dropdown-item-button
                >Something else here...</b-dropdown-item-button
              >
            </b-dropdown>
          </div>
          <div class=" budget-body d-flex align-items-center ">
            <div class="w-50 justify-content-center d-flex">
              <CircleRadial
                :Diameter="130"
                :color="'#fb0091'"
                :colorTwo="'#fb0091'"
                :completedSteps="50"
                :background="'#e5e5e5'"
                :width="8"
              />
            </div>

            <div class="w-50">
              <div class="d-flex align-item-center mb-3">
                <img src="@/assets/PurpleMoney.svg" alt="" />
                <div class="spacing">
                  <div style="font-size:14px">
                    Total <b>OPEX</b> Budget Spent
                  </div>
                  <div class="text-black-one">N 10,000,000</div>
                </div>
              </div>
              <div class="d-flex align-item-center mt-2">
                <img src="@/assets/YellowMoney.svg" alt="" />
                <div class="spacing">
                  <div style="font-size:14px">Total <b>OPEX</b> Balance</div>
                  <div class="text-black-one">N 10,000,000</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class=" status">
        <div class="status-one card-shadow ">
          <div class="status-header">
            <img src="@/assets/yellow-chart.svg" alt="" />
            <div class="status-heading">Pending Budget Reassignment Status</div>
          </div>
          <div class="status-data">
            <div class="grey">200</div>
          </div>
        </div>
        <div class="status-two card-shadow">
          <div class="status-header">
            <img src="@/assets/green-chart.svg" alt="" />
            <div class="status-heading">
              Approved Budget Reassignment Status
            </div>
          </div>
          <div class="status-data">
            <div class="grey">373</div>
          </div>
        </div>
        <div class="status-three card-shadow">
          <div class="status-header">
            <img src="@/assets/red-chart.svg" alt="" />
            <div class="status-heading">
              Declined Budget Reassignment Status
            </div>
          </div>
          <div class="status-data">
            <div class="grey">372</div>
          </div>
        </div>
      </div>
    </div>
    <div class="ml-1 bar-area">
      <div class="chart-one card-shadow">
        <div class="status-heading p-0">Total Opex Budget Statistics</div>
        <div style="font-size:14px">
          Total Budget Spent vs Total Budget Balance
        </div>
        <div style="font-size:13px" class="d-flex align-items-center mt-1">
          <div>Total Spent</div>
          <div class="rectangle">N 8,282,289</div>
          <div class="ml-2">Total Balance</div>
          <div style="color:#c00202" class="rectangle">N 8,282,289</div>
        </div>
        <Barchart class="mt-3" />
      </div>
      <div class="chart-two card-shadow">
        <div class="status-heading p-0">Total Opex Budget Statistics</div>
        <div style="font-size:13px">
          Total Budget Spent vs Total Budget Balance
        </div>
        <div style="font-size:13px" class="d-flex align-items-center mt-1">
          <div>Total Spent</div>
          <div class="rectangle">N 8,282,289</div>
          <div class="ml-2">Total Balance</div>
          <div style="color:#c00202" class="rectangle">N 8,282,289</div>
        </div>
        <Barchart class="mt-3" />
      </div>
    </div>
  </main>
</template>

<script>
import CircleRadial from '../components/progress-bar/Circle';
import Barchart from '../components/bar-chart/BarChart';
export default {
  name: 'home',
  components: {
    CircleRadial,
    Barchart
  }
};
</script>

<style scoped>
.home {
  font-family: 'Source Sans Pro', sans-serif;
  box-sizing: border-box;
}
.dashboard {
  font-family: 'Abril Fatface', cursive;
  color: #13244e;
  font-size: 1.375rem;
}
.date {
  font-size: 13px;
  font-size: 100;
}

.budget {
  flex: 6;
  margin-right: 20px;
  margin-left: 3px;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: repeat(4, 1fr);
  grid-row-gap: 20px;
}
.status {
  flex: 3.2;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: repeat(6, 1fr);
  grid-row-gap: 0.75rem;
  /* height: 67vh; */
}

.first-budget {
  grid-area: 1 / 1 / 3 / 2;
}
.second-budget {
  grid-area: 3 / 1 / 5 / 2;
}
.status-one {
  grid-area: 1 / 1 / 3 / 2;
}
.status-two {
  grid-area: 3 / 1 / 5 / 2;
}
.status-three {
  grid-area: 5 / 1 / 7 / 2;
}
.card-shadow {
  border-radius: 6px;
  box-shadow: 0 7px 64px 0 rgba(19, 36, 78, 0.07);
  background-color: #ffffff;
}
.head-count {
  margin-top: 8px;
  box-sizing: border-box;
  height: 460px;
}
.status-header {
  height: 31%;
  width: 100%;
  border-bottom: 1px solid #f0f3f7;
  display: flex;
  align-items: center;
  padding-left: 14px;
}
.status-heading {
  font-size: 0.875rem;
  color: #13244e;
  font-weight: 600;
  padding-left: 0.75rem;
}
.status-data {
  padding: 0.75rem 20px 25px;
  height: 69%;
}
.grey {
  border-radius: 8px;
  background-color: #f0f3f9;
  height: 100%;
  font-size: 2.1875rem;
  font-weight: bold;
  display: flex;
  justify-content: center;
  align-items: center;
}
.budget-header {
  height: 20%;
  width: 100%;
  border-bottom: 1px solid #f0f3f7;
  display: flex;
  align-items: center;
  padding-left: 14px;
}
.amount {
  border-radius: 6px;
  margin-left: 8px;
  padding: 4px 10px;
  font-weight: 600;
}
.purp {
  background-color: rgba(81, 44, 98, 0.2);
  font-weight: bold;
  font-size: 14px;
  border-radius: 6px;
  color: #512c62 !important;
  border: none;
}
.purp:hover,
.purp:focus,
.purp:active {
  background-color: rgba(81, 44, 98, 0.2) !important;
  font-weight: 600;
  border-radius: 6px;
  color: #512c62 !important;
  outline: none !important;
  box-shadow: none;
}
.green {
  background-color: rgba(31, 171, 137, 0.2);
  font-weight: bold;
  font-size: 14px;
  border-radius: 6px;
  color: #1fab89 !important;
  border: none;
}
.green:hover,
.green:focus,
.green:active {
  background-color: rgba(31, 171, 137, 0.2) !important;
  font-weight: 600;
  border-radius: 6px;
  color: #512c62 !important;
  outline: none !important;
  box-shadow: none;
}
.annual {
  color: #4dd599 !important;
  border-radius: 6px;
  background: rgba(77, 213, 153, 0.2) !important;
}
.spacing {
  padding-left: 1rem;
}
.budget-body {
  width: 100%;
  height: 80%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.bar-area {
  display: grid;
  width: 100%;
  height: 400px;
  margin-top: 15px;
  margin-bottom: 20px;
  grid-template-columns: 1fr 1fr;
  grid-column-gap: 10px;
}
.chart-one {
  padding: 20px 35px;
}
.rectangle {
  border-radius: 8.5px;
  background-color: #f2f2f2;
  margin-left: 6px;
  padding: 0px 9px;
  color: #4abba4;
}
.chart-two {
  padding: 20px 35px;
}
</style>
<style>
.btn-success {
  color: #4dd599 !important;
  border-radius: none;
  background: none !important;
  border: none !important;
}
.btn-success:hover,
.btn-success:focus,
.btn-success:active {
  color: #4dd599 !important;
  border-radius: none;
  background: none !important;
}
.dropdown-menu {
  top: 7px !important;
}
</style>
