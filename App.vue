<template>
  <el-container>
    <el-header>
      <el-row style="display: flex; justify-content: space-between">
        <svg
          t="1653482435664"
          class="icon"
          viewBox="0 0 1109 1024"
          version="1.1"
          xmlns="http://www.w3.org/2000/svg"
          p-id="2385"
          width="30"
          height="30"
          style="margin-top: 15px; margin-right: 5px"
        >
          >
          <path
            d="M1066.666667 341.333333h-42.666667v405.333334a149.333333 149.333333 0 0 1-298.666667 0V298.666667a42.666667 42.666667 0 0 0-42.666666-42.666667v682.666667h85.333333v85.333333H0v-85.333333h85.333333V85.333333a85.333333 85.333333 0 0 1 85.333334-85.333333h426.666666a85.333333 85.333333 0 0 1 85.333334 85.333333v85.333334a128 128 0 0 1 128 128v448a64 64 0 0 0 128 0V341.333333h-42.666667a42.666667 42.666667 0 0 1-42.666667-42.666666V213.333333a42.666667 42.666667 0 0 1 42.666667-42.666666v-21.333334a21.333333 21.333333 0 0 1 42.666667 0V170.666667h85.333333v-21.333334a21.333333 21.333333 0 0 1 42.666667 0V170.666667a42.666667 42.666667 0 0 1 42.666666 42.666666v85.333334a42.666667 42.666667 0 0 1-42.666666 42.666666zM341.333333 810.666667l170.666667-170.666667H384v-128l-128 170.666667h128z m256-682.666667H170.666667v256h426.666666V128z m426.666667 85.333333h-85.333333a42.666667 42.666667 0 0 0 0 85.333334h85.333333a42.666667 42.666667 0 0 0 0-85.333334z"
            p-id="2386"
            fill="#ffffff"
          ></path>
        </svg>
        <div class="title">巴普特充电管理系统</div>
        <div class="user-icon" style="width: 20px">
          <svg
            t="1653485792064"
            class="icon"
            viewBox="0 0 1024 1024"
            version="1.1"
            xmlns="http://www.w3.org/2000/svg"
            p-id="3294"
            width="20"
            height="20"
            @click="logout"
            style="cursor: pointer"
            v-if="token != null && token != ''"
          >
            <path
              d="M1024 512l-100.937143 103.424-0.731428-0.768L768 770.596571l-103.497143-103.460571L746.422857 585.142857H329.142857v-146.285714h417.28l-81.92-82.029714L768 253.403429l154.331429 155.940571 0.731428-0.804571zM109.714286 182.857143v658.285714a73.142857 73.142857 0 0 0 73.142857 73.142857h365.714286v109.714286H146.285714a146.285714 146.285714 0 0 1-146.285714-146.285714V146.285714a146.285714 146.285714 0 0 1 146.285714-146.285714h402.285715v109.714286H182.857143a73.142857 73.142857 0 0 0-73.142857 73.142857z"
              p-id="3295"
              fill="#ffffff"
            ></path>
          </svg>
        </div>
      </el-row>
    </el-header>
    <el-main class="main" v-if="token != null && token != ''">
      <el-space wrap>
        <div v-loading="checkChargerButtonLoading">
          <el-button
            class="mainButton"
            type="primary"
            @click="checkCharger"
            size="large"
          >
            <el-col>
              <el-row style="place-content: center">
                <svg
                  t="1654600398695"
                  class="icon"
                  viewBox="0 0 1024 1024"
                  version="1.1"
                  xmlns="http://www.w3.org/2000/svg"
                  p-id="8213"
                  width="40"
                  height="40"
                  style="margin-bottom: 15px; margin-top: 6px"
                >
                  <path
                    d="M843.16672 756.52608H180.8384A99.328 99.328 0 0 1 81.92 657.04448v-429.568A99.328 99.328 0 0 1 180.8384 128h662.32832A99.328 99.328 0 0 1 942.08 227.47648v429.568a99.328 99.328 0 0 1-98.91328 99.4816zM180.8384 188.88704a38.528 38.528 0 0 0-38.4 38.58944v429.568a38.53312 38.53312 0 0 0 38.4 38.59456h662.32832a38.52288 38.52288 0 0 0 38.36928-38.59456v-429.568a38.52288 38.52288 0 0 0-38.36928-38.58944H180.8384zM911.8208 875.52H112.2048v-60.88704H911.8208V875.52z"
                    fill="#ffffff"
                    p-id="8214"
                  ></path>
                  <path
                    d="M338.24768 604.57472a36.7104 36.7104 0 0 1-34.51904-23.936l-30.46912-80.18944H176.36352v-60.928h113.11616a37.18656 37.18656 0 0 1 34.52928 23.92064l14.2592 37.55008 72.48384-190.52032a36.864 36.864 0 0 1 69.66784 1.75104l53.51936 165.16608 53.7088-154.624a36.864 36.864 0 0 1 67.43552-5.38112l62.32576 116.40832h130.2272v60.928h-144.29696a36.864 36.864 0 0 1-32.53248-19.55328l-43.65312-81.53088-59.08992 170.12736a36.992 36.992 0 0 1-34.89792 24.92928h-0.39424a36.98688 36.98688 0 0 1-34.75456-25.65632L443.4944 394.78272l-70.72768 185.88672a36.71552 36.71552 0 0 1-34.51904 23.90528z"
                    fill="#ffffff"
                    p-id="8215"
                  ></path>
                </svg>
              </el-row>
              <el-row>充电桩状态</el-row>
            </el-col>
          </el-button>
        </div>
        <div v-loading="showReportButtonLoading">
          <el-button
            class="mainButton"
            type="primary"
            @click="showReportFunc"
            size="large"
          >
            <el-col>
              <el-row style="place-content: center">
                <svg
                  t="1654600270583"
                  class="icon"
                  viewBox="0 0 1024 1024"
                  version="1.1"
                  xmlns="http://www.w3.org/2000/svg"
                  p-id="3242"
                  width="50"
                  height="50"
                  style="margin-bottom: 15px; margin-top: 6px"
                >
                  <path
                    d="M768 800H256a32 32 0 0 1-32-32V256a32 32 0 1 1 64 0v480h480a32 32 0 0 1 0 64z m-384-128a32 32 0 0 1-32-32v-160a32 32 0 1 1 64 0v160a32 32 0 0 1-32 32z m128 0a32 32 0 0 1-32-32v-64a32 32 0 0 1 64 0v64a32 32 0 0 1-32 32z m128 0a32 32 0 0 1-32-32v-160a32 32 0 0 1 64 0v160a32 32 0 0 1-32 32z m128 0a32 32 0 0 1-32-32v-128a32 32 0 0 1 64 0v128a32 32 0 0 1-32 32z m-256-224a32 32 0 0 1-22.72-9.28l-128-128A32 32 0 1 1 406.4 265.6l105.28 105.28 137.28-137.28a32 32 0 0 1 45.12 0l96 96a32 32 0 0 1-45.12 45.12L672 301.12l-137.28 137.28a32 32 0 0 1-22.72 9.6z"
                    p-id="3243"
                    fill="#ffffff"
                  ></path>
                </svg>
              </el-row>
              <el-row>查看报表</el-row>
            </el-col>
          </el-button>
        </div>
        <div v-loading="showQueueButtonLoading">
          <el-button
            class="mainButton"
            type="primary"
            @click="showQueueFunc"
            size="large"
          >
            <el-col>
              <el-row style="place-content: center">
                <svg
                  t="1654600566022"
                  class="icon"
                  viewBox="0 0 1024 1024"
                  version="1.1"
                  xmlns="http://www.w3.org/2000/svg"
                  p-id="9627"
                  width="40"
                  height="40"
                  style="margin-bottom: 15px; margin-top: 6px"
                >
                  <path
                    d="M380 704h264c4.4 0 8-3.6 8-8v-84c0-4.4-3.6-8-8-8h-40c-4.4 0-8 3.6-8 8v36H428v-36c0-4.4-3.6-8-8-8h-40c-4.4 0-8 3.6-8 8v84c0 4.4 3.6 8 8 8z"
                    p-id="9628"
                    fill="#ffffff"
                  ></path>
                  <path
                    d="M760 581m-40 0a40 40 0 1 0 80 0 40 40 0 1 0-80 0Z"
                    p-id="9629"
                    fill="#ffffff"
                  ></path>
                  <path
                    d="M959 413.4L935.3 372c-2.2-3.8-7.1-5.1-10.9-2.9l-50.7 29.6-78.3-216.2c-8.5-26.5-33.1-44.4-60.9-44.4H301.2c-34.7 0-65.5 22.4-76.2 55.5l-74.6 205.2-50.8-29.6c-3.8-2.2-8.7-0.9-10.9 2.9L65 413.4c-2.2 3.8-0.9 8.6 2.9 10.8l60.4 35.2-14.5 40c-1.2 3.2-1.8 6.6-1.8 10V857.6c0 15.7 11.8 28.4 26.3 28.4h67.6c12.3 0 23-9.3 25.6-22.3l7.7-37.7h545.6l7.7 37.7c2.7 13 13.3 22.3 25.6 22.3h67.6c14.5 0 26.3-12.7 26.3-28.4V509.4c0-3.4-0.6-6.8-1.8-10l-14.5-40 60.3-35.2c3.8-2.2 5.1-7 3-10.8zM840 517v237H184V517l15.6-43h624.8l15.6 43zM292.7 218.1l0.5-1.3 0.4-1.3c1.1-3.3 4.1-5.5 7.6-5.5h427.6l75.4 208H220l72.7-199.9z"
                    p-id="9630"
                    fill="#ffffff"
                  ></path>
                  <path
                    d="M264 581m-40 0a40 40 0 1 0 80 0 40 40 0 1 0-80 0Z"
                    p-id="9631"
                    fill="#ffffff"
                  ></path>
                </svg>
              </el-row>
              <el-row>排队信息</el-row>
            </el-col>
          </el-button>
        </div>
      </el-space>
    </el-main>
    <el-main class="main" v-if="!token || token == ''">
      <div class="card-header">
        <h1>登录</h1>
      </div>
      <el-form ref="loginForm" :model="loginForm" class="loginForm">
        <el-form-item>
          <el-input
            v-model="loginForm.username"
            placeholder="用户名"
          ></el-input>
        </el-form-item>
        <el-form-item>
          <el-input
            v-model="loginForm.password"
            type="password"
            show-password
            placeholder="密码"
          ></el-input>
        </el-form-item>
      </el-form>
      <el-button type="primary" @click="login" class="loginButton">
        <el-icon><ArrowRightBold /></el-icon>
      </el-button>
    </el-main>
  </el-container>
  <el-dialog
    v-model="showChargerStatus"
    title="查看充电桩状态"
    width="90%"
    center
  >
    <span>
      <el-table :data="piles_stat" stripe style="width: 100%">
        <el-table-column prop="chargePileId" label="id" width="60" />
        <el-table-column
          prop="status"
          label="状态"
          :filter-method="filterTag"
          :filters="[
            // { text: '运行中', value: 'RUNNING' },
            // { text: '已关闭', value: 'SHUTDOWN' },
            // { text: '故障', value: 'UNAVAILABLE' },
            { text: '充电中', value: 1 },
            { text: '空闲', value: 2 },
            { text: '关闭', value: 3 },
            { text: '故障', value: 0 },
          ]"
        >
          <template #default="scope">
            <el-tag
              disable-transitions
              :type="
                scope.row.status === 1
                  ? 'success'
                  : scope.row.status === 3
                  ? 'info'
                  : scope.row.status === 2
                  ? 'warning'
                  : 'danger'
              "
            >
              {{ statusMap[scope.row.status] }}
            </el-tag>
          </template>
        </el-table-column>
        <el-table-column prop="totalChargeNumber" label="使用次数" />
        <el-table-column
            prop="totalChargeTime"
            label="充电时间（h）"
            :formatter="formatTotalChargeTime"
        />
        <el-table-column
          prop="totalChargeVolume"
          label="充电电量（Wh）"
        />
        <el-table-column fixed="right" label="操作" width="60">
          <template #default="scope">
            <el-button
              text
              size="small"
              type="primary"
              style="padding: 0"
              @click="changeStatus(scope.row)"
              >设置</el-button
            >
          </template>
        </el-table-column>
      </el-table>
    </span>
    <template #footer>
      <span class="dialog-footer">
        <el-button @click="showChargerStatus = false">OK</el-button>
      </span>
    </template>
  </el-dialog>
  <el-dialog
    v-model="showReport"
    title="查看报表"
    width="100%"
    center
    @close="
      {
        selectedReport = null;
        selectedReportId = null;
      }
    "
  >
    <span>
      <div style="margin-bottom: 30px; text-align-last: center">
        <el-select
          v-model="selectedReportId"
          placeholder="选择充电桩"
          @change="handleReportChange"
        >
          <el-option
            v-for="item in reportsRaw"
            :key="'Pile ' + item.chargePileId"
            :label="'Pile ' + item.chargePileId"
            :value="'Pile ' + item.chargePileId"
          />
        </el-select>
      </div>
      <el-descriptions border :column="1" v-if="selectedReport">
        <el-descriptions-item label="充电桩编号" align="center">
          {{ selectedReport.chargePileId }}
        </el-descriptions-item>
        <el-descriptions-item label="日期" align="center">
          {{ selectedReport.date }}
        </el-descriptions-item>
        <el-descriptions-item label="累计充电次数" align="center">
          {{ selectedReport.totalChargeNumber }}
        </el-descriptions-item>
        <el-descriptions-item label="累计充电时长" align="center">
          {{ selectedReport.totalChargeTime }}
        </el-descriptions-item>
        <el-descriptions-item label="累计充电量" align="center">
          {{ selectedReport.totalChargeVolume }}
        </el-descriptions-item>
        <el-descriptions-item label="累计充电费用" align="center">
          {{ selectedReport.totalChargeElectricityFee }}
        </el-descriptions-item>
        <el-descriptions-item label="累计服务费用" align="center">
          {{ selectedReport.totalChargeServeFee }}
        </el-descriptions-item>
        <el-descriptions-item label="累计服务费用" align="center">
          {{ selectedReport.totalChargeFee }}
        </el-descriptions-item>
      </el-descriptions>

<!--      <div v-for="(report, index) in reportsRaw" :key="index">-->
<!--        <el-descriptions border :column="1">-->
<!--          <el-descriptions-item label="充电桩编号" align="center">-->
<!--            {{ report.chargePileId }}-->
<!--          </el-descriptions-item>-->
<!--          <el-descriptions-item label="日期" align="center">-->
<!--            {{ report.date }}-->
<!--          </el-descriptions-item>-->
<!--          <el-descriptions-item label="累计充电次数" align="center">-->
<!--            {{ report.totalChargeNumber }}-->
<!--          </el-descriptions-item>-->
<!--          <el-descriptions-item label="累计充电时长" align="center">-->
<!--            {{ report.totalChargeTime }}-->
<!--          </el-descriptions-item>-->
<!--          <el-descriptions-item label="累计充电量" align="center">-->
<!--            {{ report.totalChargeVolume }}-->
<!--          </el-descriptions-item>-->
<!--          <el-descriptions-item label="累计充电费用" align="center">-->
<!--            {{ report.totalChargeElectricityFee }}-->
<!--          </el-descriptions-item>-->
<!--          <el-descriptions-item label="累计服务费用" align="center">-->
<!--            {{ report.totalChargeServeFee }}-->
<!--          </el-descriptions-item>-->
<!--          <el-descriptions-item label="累计服务费用" align="center">-->
<!--            {{ report.totalChargeFee }}-->
<!--          </el-descriptions-item>-->
<!--        </el-descriptions>-->
<!--        <div style="height: 30px;"></div>-->
<!--      </div>-->
    </span>
    <template #footer> </template>
  </el-dialog>
  <el-dialog
    v-model="showSelectChargerStatus"
    title="选择充电桩状态"
    width="300px"
    center
  >
    <span> 请选择需要修改的状态 </span>
    <template #footer>
      <span class="dialog-footer">
        <el-button
          :loading="selectChargerStatusButtonLoading[2]"
          @click="confirmChangeChargerStatus(2)"
          plain
          type="primary"
          >开启</el-button
        >
        <el-button
          :loading="selectChargerStatusButtonLoading[3]"
          @click="confirmChangeChargerStatus(3)"
          plain
          type="info"
          >关闭</el-button
        >
        <el-button
          :loading="selectChargerStatusButtonLoading[0]"
          @click="confirmChangeChargerStatus(0)"
          plain
          type="danger"
          >故障</el-button
        >
      </span>
    </template>
  </el-dialog>
  <el-dialog
    v-model="showQueue"
    title="查看排队信息"
    width="90%"
    center
    @close="
      {
        selectedQueue = null;
        selectedQueueId = null;
      }
    "
  >
    <span>
      <div style="margin-bottom: 30px; text-align-last: center">
        <el-cascader
          v-model="selectedQueueId"
          :options="queues"
          @change="handleQueueChange"
          placeholder="选择队列"
        />
      </div>
      <el-descriptions border :column="1" v-if="selectedQueue">
        <el-descriptions-item label="充电桩编号" align="center">
          {{ selectedQueue.chargePileId }}
        </el-descriptions-item>
        <el-descriptions-item label="用户编号" align="center">
          {{ selectedQueue.userId }}
        </el-descriptions-item>
        <el-descriptions-item label="电池容量（单位：Wh）" align="center">
          {{ selectedQueue.maxVolume  }}
        </el-descriptions-item>
        <el-descriptions-item label="请求充电量（单位：Wh）" align="center">
          {{ selectedQueue.volume  }}
        </el-descriptions-item>
        <el-descriptions-item label="已等待时间（单位：秒）" align="center">
          {{ selectedQueue.waitTime }}
        </el-descriptions-item>
      </el-descriptions>
    </span>
    <template #footer> </template>
  </el-dialog>
</template>

<script>
import { ElMessage, ElLoading } from "element-plus";
import axios from "axios";
export default {
  name: "App",
  data() {
    return {
      loginForm: {
        username: "",
        password: "",
        passwordAgain: "",
      },
      token: localStorage.getItem("token"),
      checkChargerButtonLoading: false,
      showReportButtonLoading: false,
      showQueueButtonLoading: false,
      piles_stat: [],
      showChargerStatus: false,
      showReport: false,
      showQueue: false,
      showSelectChargerStatus: false,
      changeChargerId: "",
      reportsRaw: [],
      queues: [],
      queueRawF: [],
      queueRawT: [],

      selectChargerStatusButtonLoading: [false, false, false, false],
      statusMap: {
        0: '故障',
        1: '充电中',
        2: '空闲',
        3: '关闭'
      },
      props: {
        expandTrigger: "hover",
      },
      selectedReportId: null,
      selectedReport: null,
      selectedQueueId: null,
      selectedQueue: null,
    };
  },
  methods: {
    formatTotalChargeTime(value) {
      const totalChargeTimeInHours = (value.totalChargeTime / 3600).toFixed(2);
      return totalChargeTimeInHours;
    },
    login() {
      const loading = ElLoading.service({
        fullscreen: true,
        text: "登录中...",
        background: "rgba(255, 255, 255, 1)",
      });
      axios
        .post("/api/login", JSON.stringify({
          userId: this.loginForm.username,
          password: this.loginForm.password
        }), {
              headers: {
                'Content-Type': 'application/json'
              }
            }
        )
        .then((res) => {
          if (res.data.code === 200) {
            console.log(res)
            const token = res.data.data.token;
            if (1 || res.data.data.is_admin === true) {
              this.token = token;
              localStorage.setItem("token", token);
              loading.close();
              ElMessage({
                showClose: true,
                message: "登录成功",
                type: "success",
              });
            } else {
              ElMessage.error("您不是管理员");
              loading.close();
            }
          } else {
            ElMessage.error(res.data.message);
          }
        });
    },
    logout() {
      ElMessage({
        showClose: true,
        message: "退出成功",
        type: "success",
      });
      localStorage.removeItem("token");
      this.token = "";
      this.loginOrRegister = true;
      this.loginForm = {
        username: "",
        password: "",
        passwordAgain: "",
      };
    },
    checkCharger() {
      this.checkChargerButtonLoading = true;
      axios
        .post("/api/admin/query_all_piles_stat", JSON.stringify({
          token: this.token
        }), {
          headers: {
            'Content-Type': 'application/json'
          }
        })
        .then((res) => {
          console.log(res)
          if (res.data.code === 200) {
            this.piles_stat = res.data.data.pilesStat;
            this.showChargerStatus = true;
          } else {
            ElMessage.error(res.data.message);
          }
          this.checkChargerButtonLoading = false;
        })
        .catch((err) => {
          ElMessage.error(err);
          this.checkChargerButtonLoading = false;
        });
    },
    filterTag: (value, row) => {
      return row.status === value;
    },
    showReportFunc() {
      this.showReportButtonLoading = true;
      axios
        .get("/api/admin/query_report", {
          token: this.token
        })
        .then((res) => {
          if (res.data.code === 200) {
            this.reportsRaw = res.data.data.reportList;
            this.showReport = true;
            console.log(this.reportsRaw);
          } else {
            ElMessage.error(res.data.message);
          }
          this.showReportButtonLoading = false;
        });
      // .catch((err) => {
      //   ElMessage.error(err);
      //   this.showReportButtonLoading = false;
      // });
    },
    handleReportChange() {
      this.selectedReport = this.reportsRaw.find(
          (item) => item.chargePileId === this.selectedReportId.split(' ')[1]
      );
      console.log(this.reportsRaw);
      console.log(this.selectedReport);
    },
    changeStatus(row) {
      this.changeChargerId = row.chargePileId;
      this.showSelectChargerStatus = true;
    },
    confirmChangeChargerStatus(status) {
      this.selectChargerStatusButtonLoading[status] = true;
      console.log(this.changeChargerId)
      console.log(status)
      axios
        .post(
          "/api/admin/update_pile",
          {
            chargePileId: this.changeChargerId,
            status: status,
            token: this.token
          }
        )
        .then((res) => {
          console.log(res)
          if (res.data.code === 200) {
            ElMessage.success("修改成功");
            this.showSelectChargerStatus = false;
            this.showChargerStatus = false;
          } else {
            ElMessage.error(res.data.message);
          }
          this.selectChargerStatusButtonLoading[status] = false;
        })
        .catch((err) => {
          ElMessage.error(err);
        });
    },
    // handlePileChange() {
    //   this.selectedReport = this.reportsRaw.find(
    //     (item) => item.chargePileId === this.selectedReportId.split(' ')[1]
    //   );
    // },
    showQueueFunc() {
      this.showQueueButtonLoading = true;
      var queueTypes = [0, 1]
      for (var type of queueTypes) {
        axios
            .post("/api/admin/query_queue", {
              token: this.token,
              queueType: type
            })
            .then((res) => {
              if (res.data.code === 200) {
                const data = res.data.data;
                if (type === 0) {
                  this.queueRawF = data.queueList;
                } else {
                  this.queueRawT = data.queueList;
                }
                // const queues = [];
                // for (let i = 0; i < data.queueList.length; i++) {
                //   const userId = data.queueList[i].userId;
                //   queues[userId] = queues[userId] ?? {
                //     value: userId,
                //     label: userId + "用户",
                //     children: [],
                //   };
                //   queues[userId].children.push({
                //     value: data.queueList[i].volume,
                //     label: "请求充电量：" + data.queueList[i].volume,
                //   });
                // }
                // this.queues = [];
                // for (const key in queues) {
                //   this.queues.push(queues[key]);
                // }
                this.showQueue = true;
              } else {
                ElMessage.error(res.data.message);
              }
              this.showQueueButtonLoading = false;
            })
            .catch((err) => {
              ElMessage.error(err);
              this.showQueueButtonLoading = false;
            });
      }
    },
    handleQueueChange() {
      console.log(this.queueRaw);
      console.log(this.selectedQueueId);
      this.selectedQueue = this.queueRaw.find(
        (item) =>
          item.chargePileId === this.selectedQueueId[0] &&
          item.username === this.selectedQueueId[1]
      );
    },
  },
};
</script>

<style> 
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
html {
  background-image: url("cdz.png");
  background-size:100%,100%;
  background-position: center;
  background-repeat: no-repeat;
  
}
.el-header {
  background: #ff8940;
  color: white;
  width: 100%;
}
.title {
  height: 90%;
  line-height: 60px;
  text-align: center;
  font-size: 20px;
}
.main {
  text-align: -webkit-center;
}
.el-form el-form--default loginForm{
  border: 1px solid #ccc; 
  padding: 10px; 
  background-color: #f7f7f7; 
}
.loginForm {
  max-width: 300px;

}
.user-icon {
  padding-top: 20px;
  text-align: right;
}
tr.el-table__row {
  text-align-last: center;
}
table.el-table__header {
  text-align-last: center;
}
.el-dialog {
  max-width: 600px;
  width: 90%;
}
.mainButton {
  width: 120px;
  margin-top: 20px;
  height: 120px;
}

.el-button.is-primary {
  background-color: #ff8940; /* 设置按钮背景颜色 */
  color: #fff; /* 设置按钮文字颜色 */
  font-size: 14px; /* 设置按钮文字大小 */
}
.el-button.is-primary {
  border: 1px solid #ffffff; /* 设置按钮边框 */
  border-radius: 4px; /* 设置按钮圆角 */
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* 设置按钮阴影 */
}
.el-button.is-primary:hover {
  background-color: #da7531; /* 设置按钮 hover 状态下的背景颜色 */
  color: #fff; /* 设置按钮 hover 状态下的文字颜色 */
}

.el-button.is-primary:active {
  background-color: #9f4a19; /* 设置按钮 active 状态下的背景颜色 */
  color: #fff; /* 设置按钮 active 状态下的文字颜色 */
}
.loginButton {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  margin-top: 20px;
}

.card-header {
  margin-bottom: 20px;
}
</style>
