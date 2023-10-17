<template>
  <div class="tokyo_tm_news">
    <div class="tokyo_tm_title">
      <div class="title_flex">
        <div class="left">
          <span>Favorites</span>
          <h3>Latest Favorites</h3>
        </div>
      </div>
    </div>

  <div style="margin:auto;">
    <iframe width="880" height="415" src="https://www.youtube.com/embed/2V910s3TJt0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>

    <ul class="tokyo_tm_news_inner">
      <li>
        <div class="list_inner">
          <div>
            <iframe src="https://www.omfgdogs.com/" name="myIFrame" width="500px" height="310px" style="border: solid #000000;"></iframe>
          </div>
          <!-- End .image -->
          <div class="details">
            <div class="extra">
              <p class="date">
                By <a href="#">OMFGDogs! </a><span> 25 October 2022</span>
              </p>
            </div>
            <!-- End meta info -->
            <h3 class="title" @click="showModal">
              123 Puppies
            </h3>
            <div class="tokyo_tm_read_more" @click="showModal">
              <a><span>Read More</span></a>
            </div>
          </div>
          <!-- End .details -->
        </div>

        <!-- Start first modal -->
        <transition name="fade">
          <!-- Modal -->
          <div
            :class="{ 'modal-mask': isActive }"
            id="modal"
            @click="closeModal"
            v-if="isVisible"
          >
            <div
              class="modal-dialog modal-dialog-centered modal-dialog-scrollable modal-user"
              @click.stop
            >
              <div class="modal-content">
                <div class="tokyo_tm_modalbox_news">
                  <div class="close" @click="closeModal">
                    <img
                      class="svg"
                      src="../assets/img/svg/cancel.svg"
                      alt="cancel-img"
                    />
                  </div>
                  <!-- END CLOSE ICON -->
                  <div class="image">
                    <iframe src="https://www.omfgdogs.com/" name="myIFrame" width="100%" height="310px" style="border: solid #000000;"></iframe>
                  </div>
                  <!-- END IMAGE-->
                  <div class="details">
                    <div class="extra">
                      <p class="date">
                        By <a href="#">RM</a>
                        <span>017 October 2023</span>
                      </p>
                    </div>
                    <h3 class="title">
                      What's more fun than this
                    </h3>
                  </div>
                  <!-- END DETAILS -->
                  <div class="main_content ">
                    <div class="descriptions">
                      <p class="bigger">
                        When the computer gets hard to look at and the brain gets foggy it's crutial to find things that make ya 3% happier.</p>
                      <div class="quotebox">

                      </div>
                      <!-- END QUOTEBOX -->
                    </div>
                    <!-- END DESCRIPTION -->
                    <div class="news_share">
                      <span>Share:</span>
                      <Social />
                      <!-- END SOCIAL SHARE -->
                    </div>
                    <!-- END NEWS SHARE -->
                  </div>
                </div>
                <!-- END MODALBOX NEWS -->
              </div>
            </div>
          </div>
        </transition>
        <!-- End second modal -->
      </li>
      <!-- End single blog -->

      <li>
        <div class="list_inner">
          <div class="image" @click="showModal2">
            <img src="../assets/img/thumbs/4-3.jpg" alt="thumb" />
            <div
              class="main"
              :style="{ backgroundImage: 'url(' + src2 + ')' }"
            ></div>
          </div>
          <!-- End .image -->
          <div class="details">
            <div class="extra">
              <p class="date">
                By <a href="#">Name </a><span> Date</span>
              </p>
            </div>
            <!-- End meta info -->
            <h3 class="title" @click="showModal2">
              XXX
            </h3>
            <div class="tokyo_tm_read_more" @click="showModal2">
              <a><span>Read More</span></a>
            </div>
          </div>
          <!-- End .details -->
        </div>

        <!-- Start second modal -->
        <transition name="fade">
          <!-- Modal -->
          <div
            :class="{ 'modal-mask': isActive2 }"
            id="modal"
            @click="closeModal2"
            v-if="isVisible2"
          >
            <div
              class="modal-dialog modal-dialog-centered modal-dialog-scrollable modal-user"
              @click.stop
            >
              <div class="modal-content">
                <div class="tokyo_tm_modalbox_news">
                  <div class="close" @click="closeModal2">
                    <img
                      class="svg"
                      src="../assets/img/svg/cancel.svg"
                      alt="cancel-img"
                    />
                  </div>
                  <!-- END CLOSE ICON -->
                  <div class="image">
                    <img src="../assets/img/thumbs/4-3.jpg" alt="tumb" />
                    <div
                      class="main"
                      :style="{ backgroundImage: 'url(' + popup2 + ')' }"
                    ></div>
                  </div>
                  <!-- END IMAGE-->
                  <div class="details">
                    <div class="extra">
                      <p class="date">
                        By <a href="#">XYZ</a
                        ><span>22 March 2021</span>
                      </p>
                    </div>
                    <h3 class="title">
                      Title
                    </h3>
                  </div>
                  <!-- END DETAILS -->
                  <div class="main_content ">
                    <div class="descriptions">
                      <p class="bigger">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                      <div class="quotebox">
                        <div class="icon">
                          <img
                            class="svg"
                            src="../assets/img/svg/quote.svg"
                            alt="tumb"
                          />
                        </div>
                        <p>
                          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                        </p>
                      </div>
                      <!-- END QUOTEBOX -->
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                    </div>
                    <!-- END DESCRIPTION -->
                    <div class="news_share">
                      <span>Share:</span>
                      <Social />
                      <!-- END SOCIAL SHARE -->
                    </div>
                    <!-- END NEWS SHARE -->
                  </div>
                </div>
                <!-- END MODALBOX NEWS -->
              </div>
            </div>
          </div>
        </transition>
        <!-- End Second Modal -->
      </li>
      <!-- End single blog -->

      <li>
        <div class="list_inner">
          <div class="image" @click="showModal3">
            <img src="../assets/img/thumbs/4-3.jpg" alt="thumb" />
            <div
              class="main"
              :style="{ backgroundImage: 'url(' + src3 + ')' }"
            ></div>
          </div>
          <!-- End .image -->
          <div class="details">
            <div class="extra">
              <p class="date">
                By <a href="#">Name </a><span> Date</span>
              </p>
            </div>
            <h3 class="title" @click="showModal3">
              OOO
            </h3>
            <div class="tokyo_tm_read_more" @click="showModal3">
              <a><span>Read More</span></a>
            </div>
          </div>
          <!-- End .details -->
        </div>

        <!-- Start third modal -->
        <transition name="fade">
          <!-- Modal -->
          <div
            :class="{ 'modal-mask': isActive3 }"
            id="modal"
            @click="closeModal3"
            v-if="isVisible3"
          >
            <div
              class="modal-dialog modal-dialog-centered modal-dialog-scrollable modal-user"
              @click.stop
            >
              <div class="modal-content">
                <div class="tokyo_tm_modalbox_news">
                  <div class="close" @click="closeModal3">
                    <img
                      class="svg"
                      src="../assets/img/svg/cancel.svg"
                      alt="cancel-img"
                    />
                  </div>
                  <!-- END CLOSE ICON -->
                  <div class="image">
                    <img src="../assets/img/thumbs/4-3.jpg" alt="tumb" />
                    <div
                      class="main"
                      :style="{ backgroundImage: 'url(' + popup3 + ')' }"
                    ></div>
                  </div>
                  <!-- END IMAGE-->
                  <div class="details">
                    <div class="extra">
                      <p class="date">
                        By <a href="#">Name </a><span> Date</span>
                      </p>
                    </div>
                    <h3 class="title">
                      XXX
                    </h3>
                  </div>
                  <!-- END DETAILS -->
                  <div class="main_content ">
                    <div class="descriptions">
                      <p class="bigger">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                      <div class="quotebox">
                        <div class="icon">
                          <img
                            class="svg"
                            src="../assets/img/svg/quote.svg"
                            alt="tumb"
                          />
                        </div>
                        <p>
                          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                        </p>
                      </div>
                      <!-- END QUOTEBOX -->
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                    </div>
                    <!-- END DESCRIPTION -->
                    <div class="news_share">
                      <span>Share:</span>
                      <Social />
                      <!-- END SOCIAL SHARE -->
                    </div>
                    <!-- END NEWS SHARE -->
                  </div>
                </div>
                <!-- END MODALBOX NEWS -->
              </div>
            </div>
          </div>
        </transition>
        <!-- End third modal -->
      </li>
      <!-- End single blog -->

      <li>
        <div class="list_inner">
          <div class="image" @click="showModal4">
            <img src="../assets/img/thumbs/4-3.jpg" alt="thumb" />
            <div
              class="main"
              :style="{ backgroundImage: 'url(' + src3 + ')' }"
            ></div>
          </div>
          <div class="details">
            <div class="extra">
              <p class="date">
                By <a href="#">Name </a><span> Date</span>
              </p>
            </div>
            <h3 class="title" @click="showModal4">
              XXX
            </h3>
            <div class="tokyo_tm_read_more" @click="showModal4">
              <a><span>Read More</span></a>
            </div>
          </div>
        </div>

        <!-- START FOURTH MODAL -->
        <transition name="fade">
          <!-- Modal -->
          <div
            :class="{ 'modal-mask': isActive4 }"
            id="modal"
            @click="closeModal4"
            v-if="isVisible4"
          >
            <div
              class="modal-dialog modal-dialog-centered modal-dialog-scrollable modal-user"
              @click.stop
            >
              <div class="modal-content">
                <div class="tokyo_tm_modalbox_news">
                  <div class="close" @click="closeModal4">
                    <img
                      class="svg"
                      src="../assets/img/svg/cancel.svg"
                      alt="cancel-img"
                    />
                  </div>
                  <!-- END CLOSE ICON -->
                  <div class="image">
                    <img src="../assets/img/thumbs/4-3.jpg" alt="tumb" />
                    <div
                      class="main"
                      :style="{ backgroundImage: 'url(' + popup4 + ')' }"
                    ></div>
                  </div>
                  <!-- END IMAGE-->
                  <div class="details">
                    <div class="extra">
                      <p class="date">
                        By <a href="#">XYZ</a><span>22 Jan 2021</span>
                      </p>
                    </div>
                    <h3 class="title">
                      Title
                    </h3>
                  </div>
                  <!-- END DETAILS -->
                  <div class="main_content ">
                    <div class="descriptions">
                      <p class="bigger">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                      <div class="quotebox">
                        <div class="icon">
                          <img
                            class="svg"
                            src="../assets/img/svg/quote.svg"
                            alt="tumb"
                          />
                        </div>
                        <p>
                          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                        </p>
                      </div>
                      <!-- END QUOTEBOX -->
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                      </p>
                    </div>
                    <!-- END DESCRIPTION -->
                    <div class="news_share">
                      <span>Share:</span>
                      <Social />
                      <!-- END SOCIAL SHARE -->
                    </div>
                    <!-- END NEWS SHARE -->
                  </div>
                </div>
                <!-- END MODALBOX NEWS -->
              </div>
            </div>
          </div>
        </transition>
        <!-- END SECOND MODAL -->
      </li>
      <!-- End single blog -->
    </ul>
  </div>
</template>

<script>
import Social from "../components/Social";
export default {
  components: {
    Social,
  },
  data() {
    return {
      isActive: false,
      isActive2: false,
      isActive3: false,
      isActive4: false,
      src1: require("../assets/img/news/1.jpg"),
      src2: require("../assets/img/news/2.jpg"),
      src3: require("../assets/img/news/3.jpg"),
      src4: require("../assets/img/news/4.jpg"),
      // popup1: require("../assets/img/news/1.jpg"),
      popup2: require("../assets/img/news/2.jpg"),
      popup3: require("../assets/img/news/3.jpg"),
      popup4: require("../assets/img/news/4.jpg"),

      isVisible: false,
      isVisible2: false,
      isVisible3: false,
      isVisible4: false,
    };
  },
  methods: {
    showModal: function() {
      this.isActive = true;
      this.isVisible = true;
    },
    showModal2: function() {
      this.isActive2 = true;
      this.isVisible2 = true;
    },
    showModal3: function() {
      this.isActive3 = true;
      this.isVisible3 = true;
    },
    showModal4: function() {
      this.isActive4 = true;
      this.isVisible4 = true;
    },
    closeModal: function() {
      this.isActive = false;
      this.isVisible = false;
    },
    closeModal2: function() {
      this.isActive2 = false;
      this.isVisible2 = false;
    },
    closeModal3: function() {
      this.isActive3 = false;
      this.isVisible3 = false;
    },
    closeModal4: function() {
      this.isActive4 = false;
      this.isVisible4 = false;
    },
  },
};
</script>
  body {
    background: black;
  }
<style lang="scss" scoped></style>
