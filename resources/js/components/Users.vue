<template>
  <div class="container">
    <div class="row mt-3">
      <div class="col-md-12">
        <div class="card">
          <div class="card-header">
            <h3 class="card-title">Responsive Hover Table</h3>

            <div class="card-tools">
              <span>
                <button
                  data-toggle="modal"
                  data-target="#exampleModal"
                  class="btn btn-primary btn-outline"
                >
                  <i class="fas fa-plus-circle"></i> Add New
                </button>
              </span>
            </div>
          </div>
          <!-- /.card-header -->
          <div class="card-body table-responsive p-0">
            <table class="table table-hover">
              <tbody>
                <tr>
                  <th>ID</th>
                  <th>Name</th>
                  <th>Email</th>
                  <th>Type</th>
                  <th>Date | Time</th>
                  <th></th>
                  <th>Modify</th>
                  <th></th>
                </tr>
                <tr v-for="user in users" :key="user.id">
                  <td>{{user.id}}</td>
                  <td>{{user.name}}</td>
                  <td>{{user.email}}</td>
                  <td>{{user.create_at | newDate}}</td>
                  <td>
                    <span class="tag tag-success">{{user.type}}</span>
                  </td>
                  <td>
                    <a class="btn btn-warning btn-sm btn-block" href>
                      <i class="fas fa-pencil-alt"></i> Edit
                    </a>
                  </td>
                  <td></td>
                  <td>
                    <a
                      href="#"
                      class="btn btn-danger btn-sm btn-block"
                      v-on:click="deleteUser(user.id)"
                    >
                      <i class="fas fa-trash-alt"></i> Delete
                    </a>
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
          <!-- /.card-body -->
        </div>
        <!-- /.card -->
      </div>
    </div>
    <div
      class="modal fade"
      id="exampleModal"
      tabindex="-1"
      role="dialog"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="exampleModalLabel">Modal title</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <form @submit.prevent="createUser">
            <div class="modal-body">
              <div class="form-group">
                <label>Name</label>
                <input
                  v-model="form.name"
                  type="text"
                  name="name"
                  class="form-control"
                  :class="{ 'is-invalid': form.errors.has('name') }"
                >
                <has-error :form="form" field="name"></has-error>
              </div>

              <div class="form-group">
                <label>Email</label>
                <input
                  v-model="form.email"
                  type="email"
                  name="email"
                  class="form-control"
                  :class="{ 'is-invalid': form.errors.has('email') }"
                >
                <has-error :form="form" field="email"></has-error>
              </div>

              <div class="form-group">
                <label>Select Role</label>
                <select class="form-control" name="type" v-model="form.type">
                  <option>select choice....</option>
                  <option value="admin">admin</option>
                  <option value="user">user</option>
                  <option value="subscriber">subscriber</option>
                </select>
                <has-error :form="form" field="type"></has-error>
              </div>

              <div class="form-group">
                <label for>About</label>
                <textarea
                  name="about"
                  v-model="form.about"
                  placeholder="about (optional)"
                  class="form-control"
                ></textarea>
                <has-error :form="form" field="about"></has-error>
              </div>
              <div class="form-group">
                <label>Password</label>
                <input
                  v-model="form.password"
                  type="password"
                  name="password"
                  class="form-control"
                  :class="{ 'is-invalid': form.errors.has('password') }"
                >
                <has-error :form="form" field="password"></has-error>
              </div>
            </div>
            <div class="modal-footer">
              <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
              <button type="submit" class="btn btn-primary">Save changes</button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: {},
      form: new Form({
        name: "",
        email: "",
        password: "",
        about: "",
        type: "",
        photo: ""
      })
    };
  },
  methods: {
    deleteUser(id) {
      swal({
        title: "Are you sure?",
        text: "You won't be able to revert this!",
        type: "warning",
        showCancelButton: true,
        confirmButtonColor: "#3085d6",
        cancelButtonColor: "#d33",
        confirmButtonText: "Yes, delete it!"
      }).then(result => {
        if (result.value) {
          this.form
            .delete("api/user/" + id)
            .then(() => {
              swal("Deleted!", "Your file has been deleted.", "success");
              // This is relode page after event perform
              Fire.$emit("after_created");
            })
            .catch(e => {
              swal("Failed!", "Something went Wrong..", "warning");
            });
        }
      });
    },
    loadUser() {
      axios.get("api/user").then(({ data }) => {
        this.users = data.data;
      });
    },
    createUser() {
      this.$Progress.start();

      this.form
        .post("api/user")
        .then(() => {
          Fire.$emit("after_created");
          $("#exampleModal").modal("hide");
          toast({
            type: "success",
            title: "User Created successfully"
          });
          this.$Progress.finish();
        })
        .catch(e => {
          console.log(e);
        });
    }
  },
  created() {
    this.loadUser();
    Fire.$on("after_created", () => {
      this.loadUser();
    });
    // Fire.$refs('dom-element' , () => {
    //   this.loadUser();
    // })
    // setInterval(() => {
    //   this.loadUser()
    // },2000)

    //console.log(this.loadUser());
  }
};
</script>
