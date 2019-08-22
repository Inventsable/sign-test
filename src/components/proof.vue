 <template>
  <span class="proof-text">Hello world</span>
</template>
 
<script>
const fs = require("fs");
import untildify from "untildify";
import recorder from "mic-recorder-to-mp3";
// import download from "download";

export default {
  mounted() {
    console.log(untildify);
    console.log(recorder);
    console.log(fs);

    // console.log(download);
    // Throws errors:
    //   1) Claims electron is missing as npm dependency and prompts for install
    //   2)  warning in ./node_modules/keyv/src/index.js
    //       Critical dependency: the request of a dependency is an expression
    //
    // Uncaught TypeError: Path must be a string. Received undefined
    //     at assertPath (path.js:28:11)
    //     at Object.resolve (path.js:221:7)
    //     at eval (webpack-internal:///./node_modules/npm-conf/lib/defaults.js:31:21)
    //     at Object../node_modules/npm-conf/lib/defaults.js (http://localhost:8080/app.js:2572:1)
    //     at __webpack_require__ (http://localhost:8080/app.js:724:30)
    //     at fn (http://localhost:8080/app.js:101:20)
    //     at eval (webpack-internal:///./node_modules/npm-conf/index.js:4:18)
    //     at Object../node_modules/npm-conf/index.js (http://localhost:8080/app.js:2548:1)
    //     at __webpack_require__ (http://localhost:8080/app.js:724:30)
    //     at fn (http://localhost:8080/app.js:101:20)
  }
};
</script>

<style>
.proof-text {
  font-size: 30px;
  display: grid;
  justify-content: center;
}
</style>