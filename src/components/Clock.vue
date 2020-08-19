<template>
  <div class="clock container d-flex justify-content-center">
    <div
      v-if="this.datetime"
      class="row bg-dark text-light-vue text-shadow-dark d-flex justify-content-center rounded-lg py-2 border-lg border-secondary shadow"
      style="min-width:320px;max-width:450px;"
    >
      <div class="col-12" style="max-width:400px;">
        <h5>{{time}}</h5>
        <br />
      </div>
      <div class="col-3 p-0 mr-2" style="color:#aaa">
        <div
          class="text-right"
          v-if="this.time"
        >Year {{this.time.getFullYear().toString()[0]}}{{this.time.getFullYear().toString()[1]}}</div>
        <div class="text-right">Month</div>
        <div class="text-right">Day</div>
        <div class="text-right">Hour</div>
        <div class="text-right">Minutes</div>
        <div class="text-right">Seconds</div>
      </div>
      <div class="col-3 p-0 m-0">
        <div class="d-flex justify-content-around">
          <span>{{this.datetime.y0010}}</span>
          <span class="text-left">{{this.datetime.y0001}}</span>
        </div>
        <div class="d-flex justify-content-around">
          <span>{{this.datetime.mo10}}</span>
          <span>{{this.datetime.mo01}}</span>
        </div>
        <div class="d-flex justify-content-around">
          <span>{{this.datetime.d10}}</span>
          <span>{{this.datetime.d01}}</span>
        </div>
        <div class="d-flex justify-content-around">
          <span>{{this.datetime.h10}}</span>
          <span>{{this.datetime.h01}}</span>
        </div>
        <div class="d-flex justify-content-around">
          <span>{{this.datetime.mn10}}</span>
          <span>{{this.datetime.mn01}}</span>
        </div>
        <div class="d-flex justify-content-around">
          <span>{{this.datetime.s10}}</span>
          <span>{{this.datetime.s01}}</span>
        </div>
      </div>
      <div class="col-3 p-0 ml-2" v-if="this.time" style="color:#aaa">
        <div
          class="text-left"
        >{{this.time.getFullYear().toString()[2]}}{{this.time.getFullYear().toString()[3]}}</div>
        <div class="text-left">{{"0"+(this.time.getMonth()+1)}}</div>
        <div class="text-left">{{("0"+this.time.getDate()).slice(-2)}}</div>
        <div class="text-left">{{this.meridiem}}</div>
        <div class="text-left">{{("0"+this.time.getMinutes()).slice(-2)}}</div>
        <div class="text-left">{{("0"+this.time.getSeconds()).slice(-2)}}</div>
      </div>
      <div class="col-12">
        <small>
          <br />I've always been fascintated with binary clocks. I find it satisfying watching and waiting for the digits to flip. Inspired by an LED desk-clock, I may one day extend this to include some CSS, converting those 1's and 0's to mimic LEDs.
        </small>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "clock",
  data() {
    return {
      datetime: {},
      ampm: false,
      meridiem: "24-hr",
      intervalId: null,
      // intervalId24hr: null,
      time: null,
    };
  },
  created() {
    this.runInterval();
  },
  mounted() {
    this.time = new Date();
  },
  beforeDestroy() {
    clearInterval(this.intervalId);
    // clearInterval(this.intervalId24hr);
  },
  computed: {},
  methods: {
    toggleMilitaryTime() {
      this.ampm = !this.ampm;
      if (!this.ampm) {
        this.meridiem = "24-hr";
      }
    },
    runInterval() {
      this.intervalId = setInterval(() => {
        this.resetTime();
        if (new Date().getSeconds() % 10 == 0) {
          this.toggleMilitaryTime();
        }
        this.binaryData();
      }, 1000);
    },
    resetTime() {
      this.time = new Date();
    },
    binaryData() {
      this.datetime.y1000 = (
        "000" + parseInt(this.time.getFullYear().toString()[0]).toString(2)
      ).slice(-4);
      this.datetime.y0100 = (
        "000" + parseInt(this.time.getFullYear().toString()[1]).toString(2)
      ).slice(-4);
      this.datetime.y0010 = (
        "000" + parseInt(this.time.getFullYear().toString()[2]).toString(2)
      ).slice(-4);
      this.datetime.y0001 = (
        "000" + parseInt(this.time.getFullYear().toString()[3]).toString(2)
      ).slice(-4);

      this.datetime.mo10 = (
        "000" +
        parseInt(("0" + (1 + this.time.getMonth())).slice(-2)[0]).toString(2)
      ).slice(-4);
      this.datetime.mo01 = (
        "000" +
        parseInt(("0" + (1 + this.time.getMonth())).slice(-2)[1]).toString(2)
      ).slice(-4);

      this.datetime.d10 = (
        "000" + parseInt(("0" + this.time.getDate()).slice(-2)[0]).toString(2)
      ).slice(-4);
      this.datetime.d01 = (
        "000" + parseInt(("0" + this.time.getDate()).slice(-2)[1]).toString(2)
      ).slice(-4);

      if (this.ampm == false) {
        this.datetime.h10 = (
          "000" +
          parseInt(("0" + this.time.getHours()).slice(-2)[0]).toString(2)
        ).slice(-4);
        this.datetime.h01 = (
          "000" +
          parseInt(("0" + this.time.getHours()).slice(-2)[1]).toString(2)
        ).slice(-4);
      } else {
        if (this.time.getHours() < 12) {
          this.meridiem = "am";
          this.datetime.h10 = (
            "000" +
            parseInt(("0" + this.time.getHours()).slice(-2)[0]).toString(2)
          ).slice(-4);
          this.datetime.h01 = (
            "000" +
            parseInt(("0" + this.time.getHours()).slice(-2)[1]).toString(2)
          ).slice(-4);
        } else if (this.ampm == true) {
          this.meridiem = "pm";
          this.datetime.h10 = (
            "000" +
            parseInt(("0" + (this.time.getHours() - 12)).slice(-2)[0]).toString(
              2
            )
          ).slice(-4);
          this.datetime.h01 = (
            "000" +
            parseInt(("0" + (this.time.getHours() - 12)).slice(-2)[1]).toString(
              2
            )
          ).slice(-4);
        }
      }

      this.datetime.mn10 = (
        "000" +
        parseInt(("0" + this.time.getMinutes()).slice(-2)[0]).toString(2)
      ).slice(-4);
      this.datetime.mn01 = (
        "000" +
        parseInt(("0" + this.time.getMinutes()).slice(-2)[1]).toString(2)
      ).slice(-4);
      this.datetime.s10 = (
        "000" +
        parseInt(("0" + this.time.getSeconds()).slice(-2)[0]).toString(2)
      ).slice(-4);
      this.datetime.s01 = (
        "000" +
        parseInt(("0" + this.time.getSeconds()).slice(-2)[1]).toString(2)
      ).slice(-4);

      // return time;
    },
  },
  components: {},
};
</script>


<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Courier+Prime:wght@400;700&display=swap");
* {
  font-family: "Courier Prime", monospace;
  /* color: black; */
  /* text-shadow: 1px 1px 5px white; */
  /* font-weight: 700; */
}
</style>