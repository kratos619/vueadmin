<template>
  <div class="container">
    <div class="row mt-3">
      <div class="col-md-12">
        <div class="card">
          <div class="card-header">
            <h3 class="card-title">Responsive Hover Table</h3>

            <div class="card-tools">
              <span>
                <button class="btn btn-primary btn-outline">
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
                  <th></th>
                  <th>Modify</th>
                  <th></th>
                </tr>
                <tr>
                  <td>183</td>
                  <td>John Doe</td>
                  <td>11-7-2014</td>
                  <td>
                    <span class="tag tag-success">Approved</span>
                  </td>
                  <td>
                    <a class="btn btn-warning btn-sm btn-block" href>
                      <i class="fas fa-pencil-alt"></i> Edit
                    </a>
                  </td>
                  <td></td>
                  <td>
                    <a class="btn btn-danger btn-sm btn-block" href>
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
  </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
