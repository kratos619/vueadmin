<template>
  <div class="container">
    <h3 class="m-4">Profile</h3>
    <div class="row">
      <div class="col-md-3">
        <!-- Profile Image -->
        <div class="card card-primary card-outline">
          <div class="card-body box-profile">
            <div class="text-center">
              <img
                class="profile-user-img img-fluid img-circle"
                src="'./img/user.png'"
                alt="User profile picture"
              >
            </div>

            <h3 class="profile-username text-center">Nina Mcintire</h3>

            <p class="text-muted text-center">Software Engineer</p>

            <ul class="list-group list-group-unbordered mb-3">
              <li class="list-group-item">
                <b>Followers</b>
                <a class="float-right">1,322</a>
              </li>
              <li class="list-group-item">
                <b>Following</b>
                <a class="float-right">543</a>
              </li>
              <li class="list-group-item">
                <b>Friends</b>
                <a class="float-right">13,287</a>
              </li>
            </ul>

            <a href="#" class="btn btn-primary btn-block">
              <b>Follow</b>
            </a>
          </div>
          <!-- /.card-body -->
        </div>
        <!-- /.card -->
        <!-- About Me Box -->
        <div class="card card-primary">
          <div class="card-header">
            <h3 class="card-title">About Me</h3>
          </div>
          <!-- /.card-header -->
          <div class="card-body">
            <strong>
              <i class="fa fa-book mr-1"></i> Education
            </strong>

            <p
              class="text-muted"
            >B.S. in Computer Science from the University of Tennessee at Knoxville</p>

            <hr>

            <strong>
              <i class="fa fa-map-marker mr-1"></i> Location
            </strong>

            <p class="text-muted">Malibu, California</p>

            <hr>

            <strong>
              <i class="fa fa-pencil mr-1"></i> Skills
            </strong>

            <p class="text-muted">
              <span class="tag tag-danger">UI Design</span>
              <span class="tag tag-success">Coding</span>
              <span class="tag tag-info">Javascript</span>
              <span class="tag tag-warning">PHP</span>
              <span class="tag tag-primary">Node.js</span>
            </p>

            <hr>

            <strong>
              <i class="fa fa-file-text-o mr-1"></i> Notes
            </strong>

            <p
              class="text-muted"
            >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam fermentum enim neque.</p>
          </div>
          <!-- /.card-body -->
        </div>
        <!-- /.card -->
      </div>
      <div class="col-md-9">
        <div class="card">
          <div class="card-header p-4">
            <ul class="nav nav-pills">
              <li class="nav-item">
                <a class="nav-link active show" href="#timeline" data-toggle="tab">Timeline</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#settings" data-toggle="tab">Settings</a>
              </li>
            </ul>
          </div>
          <div class="card-body m-3">
            <div class="tab-content">
              <div class="tab-pane" id="timeline">
                <!-- The timeline -->
                <ul class="timeline timeline-inverse">
                  <!-- timeline time label -->
                  <li class="time-label">
                    <span class="bg-danger">10 Feb. 2014</span>
                  </li>
                  <!-- /.timeline-label -->
                  <!-- timeline item -->
                  <li>
                    <i class="fa fa-envelope bg-primary"></i>

                    <div class="timeline-item">
                      <span class="time">
                        <i class="fa fa-clock-o"></i> 12:05
                      </span>

                      <h3 class="timeline-header">
                        <a href="#">Support Team</a> sent you an email
                      </h3>

                      <div class="timeline-body">
                        Etsy doostang zoodles disqus groupon greplin oooj voxy zoodles,
                        weebly ning heekya handango imeem plugg dopplr jibjab, movity
                        jajah plickers sifteo edmodo ifttt zimbra. Babblely odeo kaboodle
                        quora plaxo ideeli hulu weebly balihoo...
                      </div>
                      <div class="timeline-footer">
                        <a href="#" class="btn btn-primary btn-sm">Read more</a>
                        <a href="#" class="btn btn-danger btn-sm">Delete</a>
                      </div>
                    </div>
                  </li>
                  <!-- END timeline item -->
                  <!-- timeline item -->
                  <li>
                    <i class="fa fa-user bg-info"></i>

                    <div class="timeline-item">
                      <span class="time">
                        <i class="fa fa-clock-o"></i> 5 mins ago
                      </span>

                      <h3 class="timeline-header no-border">
                        <a href="#">Sarah Young</a> accepted your friend request
                      </h3>
                    </div>
                  </li>
                  <!-- END timeline item -->
                  <!-- timeline item -->
                  <li>
                    <i class="fa fa-comments bg-warning"></i>

                    <div class="timeline-item">
                      <span class="time">
                        <i class="fa fa-clock-o"></i> 27 mins ago
                      </span>

                      <h3 class="timeline-header">
                        <a href="#">Jay White</a> commented on your post
                      </h3>

                      <div class="timeline-body">
                        Take me to your leader!
                        Switzerland is small and neutral!
                        We are more like Germany, ambitious and misunderstood!
                      </div>
                      <div class="timeline-footer">
                        <a href="#" class="btn btn-warning btn-flat btn-sm">View comment</a>
                      </div>
                    </div>
                  </li>
                  <!-- END timeline item -->
                  <!-- timeline time label -->
                  <li class="time-label">
                    <span class="bg-success">3 Jan. 2014</span>
                  </li>
                  <!-- /.timeline-label -->
                  <!-- timeline item -->
                  <li>
                    <i class="fa fa-camera bg-purple"></i>

                    <div class="timeline-item">
                      <span class="time">
                        <i class="fa fa-clock-o"></i> 2 days ago
                      </span>

                      <h3 class="timeline-header">
                        <a href="#">Mina Lee</a> uploaded new photos
                      </h3>

                      <div class="timeline-body">
                        <img src="http://placehold.it/150x100" alt="..." class="margin">
                        <img src="http://placehold.it/150x100" alt="..." class="margin">
                        <img src="http://placehold.it/150x100" alt="..." class="margin">
                        <img src="http://placehold.it/150x100" alt="..." class="margin">
                      </div>
                    </div>
                  </li>
                  <!-- END timeline item -->
                  <li>
                    <i class="fa fa-clock-o bg-gray"></i>
                  </li>
                </ul>
              </div>
              <!-- /.tab-pane -->
              <div class="tab-pane active show" id="settings">
                <form class="form-horizontal">
                  <div class="form-group">
                    <label for="inputName" class="col-sm-2 control-label">Name</label>

                    <div class="col-sm-10">
                      <input
                        v-model="form.name"
                        type="email"
                        class="form-control"
                        id="inputName"
                        placeholder="Name"
                      >
                    </div>
                  </div>
                  <div class="form-group">
                    <label for="inputEmail" class="col-sm-2 control-label">Email</label>

                    <div class="col-sm-10">
                      <input
                        v-model="form.email"
                        type="email"
                        class="form-control"
                        id="inputEmail"
                        placeholder="Email"
                      >
                    </div>
                  </div>
                  <div class="form-group">
                    <label for="inputName2" class="col-sm-2 control-label">Type</label>

                    <div class="col-sm-10">
                      <input
                        v-model="form.type"
                        type="text"
                        class="form-control"
                        
                      >
                    </div>
                  </div>
                  <div class="form-group">
                    <label  class="col-sm-2 control-label">About</label>
                    <div class="col-sm-10">
                      <textarea
                        class="form-control"
                        v-model="form.about"
                      ></textarea>
                    </div>
                  </div>
                  <div class="form-group">
                    <label for="inputSkills" class="col-sm-2 control-label">Image</label>

                    <div class="col-sm-10">
                      <input type="file" class="form-control" >
                    </div>
                  </div>
                  
                  <div class="form-group">
                    <div class="col-sm-offset-2 col-sm-10">
                      <button type="submit" class="btn btn-danger">Submit</button>
                    </div>
                  </div>
                </form>
              </div>
              <!-- /.tab-pane -->
            </div>
            <!-- /.tab-content -->
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: new Form({
        id: "",
        name: "",
        email: "",
        password: "",
        about: "",
        type: "",
        photo: ""
      })
    };
  },
  mounted() {
    console.log("Component mounted.");
  },
  created() {
    axios.get("api/profile").then(({ data }) => this.form.fill(data));
  }
};
</script>
