<template>
  <div class="course">
    <h1>{{ msg }}</h1>
    <h3>Index</h3>
    <div class="course-descr">
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium possimus, quam eum laudantium autem explicabo mollitia rerum voluptate quaerat quas! Incidunt voluptatibus repudiandae modi pariatur expedita ipsam enim consectetur aliquid!
        Repudiandae tempore necessitatibus enim itaque quidem rerum, in a earum libero eveniet porro doloremque! Corrupti provident, eius obcaecati quod ut aut cumque repellendus commodi quidem? Earum ab voluptatibus asperiores a!
        Voluptates libero odio eius optio minima, consectetur at dolorem, accusantium vitae sunt nam sed cumque culpa quia dolor corrupti eaque, architecto sint itaque veniam nobis illum aliquid voluptate! Autem, ratione.
        Inventore dolor quidem ipsam voluptate deleniti velit minus, fuga explicabo, magnam suscipit officiis eius atque quisquam alias ipsum laboriosam eligendi illum numquam porro aut repellat nulla esse, illo fugiat. 
        Possimus.
      </p>
      <p>
        Velit sequi dolore accusantium a consequuntur voluptas dolorem excepturi ad fuga id facilis quod alias amet iusto numquam aspernatur ducimus sint aliquam minus quisquam vitae, repellat temporibus aut molestias? Veniam.
        Tempora impedit esse corporis ipsum rem fugit quas autem ut? Ab minus voluptatum deleniti, optio cum consequatur harum dolores, unde itaque, beatae est hic! Asperiores blanditiis quidem vitae incidunt expedita?
        Blanditiis id consequatur numquam ullam voluptatum odio cupiditate. Neque provident adipisci, fugiat pariatur nihil facere rerum, tempore natus magnam illo error perspiciatis labore voluptates quae! Dignissimos odit quia officiis aut!
        Quos non, quam sint illum nihil commodi quae saepe esse fuga dolorum quasi. In voluptatum, quasi nemo iusto neque explicabo totam sit fugit tempora veritatis pariatur sint repellendus optio fugiat.
      </p>
    </div>
    <div class="course-lessons">
      <div class="course-lessons-list">
        <ul v-for="lesson in course.listLessons" v-bind:key="lesson.name" :course="course">
          <li> {{ lesson.name }}</li>
        </ul>
      </div>
      <div class="course-lesson-vp">
        <div class="b-hcenter b-vcenter">
          <video
            id="my-video"
            class="video-js"
            controls
            preload="auto"
            width="640"
            height="264"
            poster="../../public/video/v-1.jpg"
            data-setup="{}"
          >
            <source src="../../public/video/v-1.mp4" type="video/mp4" />
            <!--<source src="MY_VIDEO.webm" type="video/webm" /> -->
            <p class="vjs-no-js">
              To view this video please enable JavaScript, and consider upgrading to a
              web browser that
              <a href="https://videojs.com/html5-video-support/" target="_blank"
                >supports HTML5 video</a
              >
            </p>
          </video>
        </div>
      </div>
    </div>
  </div>


</template>

<script>
export default {
  name: 'VideoCourse',
  props: {
    msg: String,
    course: Object
  }
}
</script>

<style scoped>
  @import "video.js";
  .course {
    min-width: 600px;
  }

  .course-descr {
    font-style: italic;
    text-align: justify;
  }

  .course-lessons {
    min-height: 300px;
  }

  .course-lessons-list {
    text-align: left;
    width: 20%;
    height: 100%;
    display: inline-block;
    
  }

  .course-lesson-vp {
    width: 80%;
    display: inline-block;
  }

  .b-hcenter {
    margin-left: auto;
    margin-right: auto;
    /*width: 6em*/
  }
  .b-vcenter {
    /*min-height: 10em;*/
    display: table-cell;
    vertical-align: middle 
  }
</style>
