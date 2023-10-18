<template>
  <div class="tokyo_tm_about">
    <div class="about_image">
      <img src="../assets/img/slider/almafi-1.jpg" alt="about" />
    </div>
    <!-- End .about_image -->

    <div class="description">
      <div class="description_inner">
        <div class="left">
          <h3 class="name">Rachel Martinez</h3>
          <p>
            I'm an experienced full-stack developer with a demonstrated history of working in the computer software industry. 
            I'm skilled in Python, JavaScript, MySQL, and HTML/CSS and various web frameworks. 
            I'm a strong engineering professional with a Bachelor of Science (B.S.) focused in Computer Science from Weber State University.
            I work well with teams and have strong communication skills.
            Let's talk.
          </p>
        </div>
        <!-- End .left -->

        <div class="right">
          <ul>
            <li>
              <p><span>Address</span>Greater Salt Lake Area</p>
            </li>
            <li>
              <p>
                <span>Email</span
                ><a href="mailto:mail@gmail.com">RachelMartinez101@gmail.com</a>
              </p>
            </li>
            <li>
              <p><span>Study</span>Computer Science</p>
            </li>
          </ul>
          <div class="tokyo_tm_button">
            <button class="ib-button" @click="showModal">My Stats</button>
          </div>
          <!-- End ul -->
        </div>
        <!-- End .right -->
      </div>
    </div>

    <!-- Start Modalbox -->
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
            <div class="tokyo_tm_modalbox_about">
              <div class="close" @click="closeModal">
                <img
                  class="svg"
                  src="../assets/img/svg/cancel.svg"
                  alt="cancel-img"
                />
              </div>
              <!-- End .close -->
              <div class="my_box">
                <div class="left">
                  <div class="about_title">
                    <h3>Technical Skills</h3>
                  </div>
                  <!-- End .abut_title -->
                  <div class="tokyo_progress">
                    <div class="progress_inner">
                      <span
                        ><span class="label">MySQL</span
                        ><span class="number">80%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width:80%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                    <div class="progress_inner">
                      <span
                        ><span class="label">Python</span
                        ><span class="number">70%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width:70%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                    <div class="progress_inner">
                      <span
                        ><span class="label">JavaScript</span
                        ><span class="number">75%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width:75%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                    <div class="progress_inner">
                      <span
                        ><span class="label">VueJS</span
                        ><span class="number">70%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width:70%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                    <div class="progress_inner">
                      <span
                        ><span class="label">AWS Cloud Computing</span
                        ><span class="number">60%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width:60%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                    <div class="progress_inner">
                      <span
                        ><span class="label">Git</span
                        ><span class="number">85%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width:85%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                  </div>
                  <!-- End .tokyo_progress -->
                </div>
                <!-- End .left -->
                <div class="right">
                  <div class="about_title">
                    <h3>Non-Technical Skills</h3>
                  </div>
                  <div class="tokyo_progress">
                    <div class="progress_inner">
                      <span
                        ><span class="label">Social (Teamwork, Leadership, Communication)</span
                        ><span class="number">85%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width:85%"></div>
                        </div>
                      </div>
                    </div>
                    <div class="progress_inner">
                      <span
                        ><span class="label">Personal Management</span
                        ><span class="number">90%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width:90%"></div>
                        </div>
                      </div>
                    </div>
                    <div class="progress_inner">
                      <span
                        ><span class="label">Cognitive (Decision-making, Cognitive Readiness, Task Management)</span
                        ><span class="number">85%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width:85%"></div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <!-- End .right -->
              </div>
            </div>
            <!-- End .tokyo_tm_modalbox_about -->
          </div>
        </div>
      </div>
    </transition>
    <!-- End Modalbox -->
  </div>
</template>

<script>
export default {
  components: {
    
  },
  data() {
    return {
      isActive: false,
      isVisible: false,
    };
  },
  methods: {
    showModal: function() {
      this.isActive = true;
      this.isVisible = true;
    },
    closeModal: function() {
      this.isActive = false;
      this.isVisible = false;
    },
  },
};
</script>

<style lang="scss"></style>
