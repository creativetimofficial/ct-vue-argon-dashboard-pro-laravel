# [Vue Argon Dashboard Pro Laravel](https://vue-argon-dashboard-pro-laravel.creative-tim.com/?ref=vadpl-readme) [![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social&logo=twitter)](https://twitter.com/home?status=Vue%20Argon%20Dashboard%20Pro%20Laravel%E2%9D%A4%EF%B8%8F%0Ahttps%3A//vue-argon-dashboard-pro-laravel.creative-tim.com/%20%23%vue%20%23%argon%20%23design%20%23dashboard%20%23laravel%20%23pro%20via%20%40CreativeTim)

![version](https://img.shields.io/badge/version-1.0.0-blue.svg) [![GitHub issues open](https://img.shields.io/github/issues/creativetimofficial/ct-vue-argon-dashboard-pro-laravel.svg?maxAge=2592000)](https://github.com/creativetimofficial/ct-vue-argon-dashboard-pro-laravel/issues?q=is%3Aopen+is%3Aissue) [![GitHub issues closed](https://img.shields.io/github/issues-closed-raw/creativetimofficial/ct-vue-argon-dashboard-pro-laravel/ct-vue-argon-dashboard-pro-laravel.svg?maxAge=2592000)](https://github.com/creativetimofficial/ct-vue-argon-dashboard-pro-laravel/issues?q=is%3Aissue+is%3Aclosed)

_Frontend version_: Argon Dashboard v1.2.0. More info at https://www.creative-tim.com/product/argon-dashboard-pro

_Vue version_: Vue Argon Dashboard v1.2.2. More info at https://www.creative-tim.com/product/vue-argon-dashboard-pro

![Product Image](https://s3.amazonaws.com/creativetim_bucket/products/353/original/opt_adp_vue_laravel_thumbnail.jpg)

What if you could go from frontend to fullstack in an instant when building your app? We partnered with [UPDIVISION](https://updivision.com) to bring you Vue Argon Dashboard PRO Laravel , the ultimate fullstack resource. Vue Argon Dashboard PRO Laravel comes not only with a huge number of UI components and a Vue Argon frontend, but also with an API-powered Laravel backend.

# Download

For the PRO version of the project you will download the .zip file from the Creative Tim site and extract it.

You will get two project folders: one for the Laravel API project and one for the Vue frontend.

# Laravel API Setup

## Introduction

JSON:API is a specification for how a client should request that resources be fetched or modified, and how a server should respond to those requests. It is designed to minimize both the number of requests and the amount of data transmitted between clients and servers. This efficiency is achieved without compromising readability, flexibility, or discoverability.

[Click here to go to the JSON:API docs](https://explore.postman.com/api/6357/laravel-jsonapi)

## Prerequisites

### JSON:API backend
The Laravel JSON:API backend project requires a proper multi-threaded web server such as Apache/Nginx environment with PHP, Composer and MySQL.

**Do not use `php artisan serve` as it will result in stalled requests due to the single-threaded nature of the built-in PHP web server.** 

We strongly recommend using [Laradock](https://laradock.io/) for Linux and Mac or [Laragon](https://laragon.org/download/) for Windows if possible.

Other options for your local environment:
- Windows: [How to install WAMP on Windows](https://updivision.com/blog/post/beginner-s-guide-to-setting-up-your-local-development-environment-on-windows)
- Linux: [How to install LAMP on Linux](https://howtoubuntu.org/how-to-install-lamp-on-ubuntu)
- Mac: [How to install MAMP on MAC](https://wpshout.com/quick-guides/how-to-install-mamp-on-your-mac/)

You will also need to install Composer 2: [https://getcomposer.org/doc/00-intro.md](https://getcomposer.org/doc/00-intro.md)

### Vue Argon frontend
The Vue Argon frontend project requires a working local environment with NodeJS version 8.9 or above (8.11.0+ recommended), npm, VueCLI.

Install Node: https://nodejs.org/ (version 8.11.0+ recommended)

Install NPM: https://www.npmjs.com/get-npm

Install VueCLI: https://cli.vuejs.org/guide/installation.html

## Laravel API Project Installation

1. Navigate in your Laravel API project folder: `cd your-laravel-json-api-project`
2. Install project dependencies: `composer install`
3. Create a new .env file: `cp .env.example .env`
4. Add your own database credentials in the .env file in DB_DATABASE, DB_USERNAME, DB_PASSWORD
5. Create users table: `php artisan migrate --seed`
6. Generate application key: `php artisan key:generate`
7. Install Laravel Passport: `php artisan passport:install`
8. Add your own mailtrap.io credentials in MAIL_USERNAME and MAIL_PASSWORD in the .env file

## Vue Argon Dashboard Project Installation

1. Navigate to your Vue Argon Dashboard project folder: `cd your-vue-argon-dashbord-project`
2. Install project dependencies: `npm install`
3. Create a new .env file: `cp .env.example .env`
4. `VUE_APP_BASE_URL` should contain the URL of your Vue Argon Dashboard Project (eg. http://localhost:8080/)
5. `VUE_APP_API_BASE_URL` should contain the URL of your Laravel JSON:API Project. (eg. http://localhost:3000/api/v1)
6. Run `npm run dev` to start the application in a local development environment or `npm run build`  to build release distributables.

## Usage

To start testing the Pro theme, register as a user or log in using one of the default users:

- admin type - **admin@jsonapi.com** with the password **secret**
- creator type - **creator@jsonapi.com** with the password **secret**
- member type - **member@jsonapi.com** with the password **secret**

In addition to the features included in the free theme, the Pro theme also has a role management example with an updated user management, as well as tag management, category management and item management examples. All the necessary files are installed out of the box and all the needed routes are added to `src\router\routes.js`. Keep in mind that all the features can be viewed once you log in using the credentials provided above or by registering your own user.

Each role has a different privilege level and can perform a certain number of actions according to this level.

A **member type** user can log in, update his profile and view a list of added items.
A **creator type** user can log in, update his profile and perform actions on categories, tags and items.
A **admin type** user can log in, update his profile and perform actions on categories, tags, items, roles and users.

### Dashboard

You can access the dashboard either by using the "**Dashboards/Dashboard**" link in the left sidebar or by adding **/dashboard** in the URL.

### Login

The login functionality is fully implemented in our theme helping you to start your project in no time. To login into dashboard you just have to add **/login** in the URL and fill the login form with one of the credentials (user: **admin@jsonapi.com**, **creator@jsonapi.com**, **member@jsonapi.com** and password: **secret**).

The `src\views\Pages\Login.vue` is the Vue component which handles the login functinality. You can easily adapt it to your needs.

It uses the auth store located in `src\store\modules\auth.js`.

### Login Card

```
<div class="container mt--8 pb-5">
  <div class="row justify-content-center">
    <div class="col-lg-5 col-md-7">
      <div class="card bg-secondary border-0 mb-0">
        <div class="card-header bg-transparent pb-5">
          <div class="text-muted text-center mt-2 mb-3">
            <small>Sign in with</small>
          </div>
          <div class="btn-wrapper text-center">
            <a href="#" class="btn btn-neutral btn-icon">
              <span class="btn-inner--icon"
                ><img src="/img/icons/common/github.svg"
              /></span>
              <span class="btn-inner--text">Github</span>
            </a>
            <a href="#" class="btn btn-neutral btn-icon">
              <span class="btn-inner--icon"
                ><img src="/img/icons/common/google.svg"
              /></span>
              <span class="btn-inner--text">Google</span>
            </a>
          </div>
        </div>
        <div class="card-body px-lg-5 py-lg-5">
          <div class="text-center text-muted mb-4">
            <small>Or sign in with credentials</small>
          </div>
          <form role="form" @submit.prevent="handleSubmit()">
            <base-input
              alternative
              class="mb-3"
              name="Email"
              prepend-icon="ni ni-email-83"
              placeholder="Email"
              v-model="email"
            />
            <validation-error :errors="apiValidationErrors.email" />

            <base-input
              alternative
              class="mb-3"
              name="Password"
              :rules="{ required: true, min: 6 }"
              prepend-icon="ni ni-lock-circle-open"
              type="password"
              placeholder="Password"
              v-model="password"
            >
            </base-input>
            <validation-error :errors="apiValidationErrors.password" />

            <div class="text-center">
              <base-button type="primary" native-type="submit" class="my-4"
                >Sign in</base-button
              >
            </div>
          </form>
        </div>
      </div>
      <div class="row mt-3">
        <div class="col-6">
          <router-link to="/password/reset" class="text-light"
            ><small>Forgot password?</small></router-link
          >
        </div>
        <div class="col-6 text-right">
          <router-link to="/register" class="text-light"
            ><small>Create new account</small></router-link
          >
        </div>
      </div>
    </div>
  </div>
</div>
```

### Register

The register functionality is fully implemented in our theme helping you to start your project in no time. To register a new user you just have to add **/register** in the URL or click on register link from login page and fill the register form with user details.

The `src\views\pages\Register.vue` is the Vue component which handles the login functinality. You can easily extend it to your needs.

It uses the auth store located in `src\store\modules\auth.js`.

#### Register card

```
<div class="container mt--8 pb-5">
  <!-- Table -->
  <div class="row justify-content-center">
    <div class="col-lg-6 col-md-8">
      <div class="card bg-secondary border-0">
        <div class="card-header bg-transparent pb-5">
          <div class="text-muted text-center mt-2 mb-4">
            <small>Sign up with</small>
          </div>
          <div class="text-center">
            <a href="#" class="btn btn-neutral btn-icon mr-4">
              <span class="btn-inner--icon"
                ><img src="/img/icons/common/github.svg"
              /></span>
              <span class="btn-inner--text">Github</span>
            </a>
            <a href="#" class="btn btn-neutral btn-icon">
              <span class="btn-inner--icon"
                ><img src="/img/icons/common/google.svg"
              /></span>
              <span class="btn-inner--text">Google</span>
            </a>
          </div>
        </div>
        <div class="card-body px-lg-5 py-lg-5">
          <div class="text-center text-muted mb-4">
            <small>Or sign up with credentials</small>
          </div>
          <form role="form" @submit.prevent="handleSubmit()">
            <base-input
              alternative
              class="mb-3"
              prepend-icon="ni ni-hat-3"
              placeholder="Name"
              name="Name"
              v-model="name"
            >
            </base-input>
            <validation-error :errors="apiValidationErrors.name" />

            <base-input
              alternative
              class="mb-3"
              prepend-icon="ni ni-email-83"
              placeholder="Email"
              name="Email"
              v-model="email"
            >
            </base-input>
            <validation-error :errors="apiValidationErrors.email" />

            <base-input
              alternative
              class="mb-3"
              prepend-icon="ni ni-lock-circle-open"
              placeholder="Password"
              type="password"
              name="Password"
              v-model="password"
            >
            </base-input>
            <password
              class="mb-3"
              v-model="password"
              :strength-meter-only="true"
              @score="showScore"
              :showStrengthMeter="false"
            />

            <validation-error :errors="apiValidationErrors.password" />

            <base-input
              alternative
              class="mb-3"
              prepend-icon="ni ni-lock-circle-open"
              placeholder="Confirm Password"
              type="password"
              name="Password confirmation"
              v-model="password_confirmation"
            >
            </base-input>
            <validation-error
              :errors="apiValidationErrors.password_confirmation"
            />

            <div class="text-muted font-italic">
              <small
                >password strength:
                <template v-if="scors === 0">
                  <span class="text-danger font-weight-700">
                    very weak
                  </span>
                </template>

                <template v-if="scors === 1">
                  <span class="text-danger font-weight-700"> weak </span>
                </template>

                <template v-if="scors === 2">
                  <span class="text-warning font-weight-700"> medium </span>
                </template>

                <template v-if="scors === 3">
                  <span class="text-success font-weight-700"> strong </span>
                </template>

                <template v-if="scors === 4">
                  <span class="text-success font-weight-700">
                    very strong
                  </span>
                </template>
              </small>

            </div>
            <div class="row my-4">
              <div class="col-12">
                <base-input
                  :rules="{ required: { allowFalse: false } }"
                  name="Privacy"
                  Policy
                >
                  <base-checkbox v-model="boolean">
                    <span class="text-muted"
                      >I agree with the
                      <a href="#!">Terms and conditions</a></span
                    >
                  </base-checkbox>
                </base-input>
              </div>
            </div>
            <div class="text-center">
              <base-button type="primary" native-type="submit" class="my-4"
                >Create account</base-button
              >
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</div>
```

### Profile edit

You have the option to edit the current logged in user's profile information (name, email, profile picture) and password. To access this page, just click the "**Examples/Profile**" link in the left sidebar or add **/examples/user-profile** in the URL.

The `src\views\Examples\UserProfile` is the folder with Vue components that handle the update of the user information and password.

#### Edit profile component

```
<template>
    <div class="container-fluid mt-5">
        <div class="row">
            <div class="col-xl-6 order-xl-1" >
                <div>
                    <user-edit-card :user="user"/>
                </div>
                <div class="mt-5">
                    <user-password-card :user="user"/>
                </div>
            </div>
            <div class="col-xl-6 order-xl-2">
                <user-card />
            </div>
        </div>
    </div>
</template>
<script>
import UserEditCard from '@/views/Examples/UserProfile/UserEditCard.vue'
import UserPasswordCard from '@/views/Examples/UserProfile/UserPasswordCard.vue'
import UserCard from '@/views/Pages/UserProfile/UserCard.vue'

export default {
    layout: 'DashboardLayout',

    components: {
        UserEditCard,
        UserPasswordCard,
        UserCard
    },

    data() {
        return {
            user: {
                type: 'profile',
                name: null,
                email: null,
                profile_image: null,
            }
        }
    },
     created() {
      this.getProfile();
    },

    methods: {
      async getProfile() {
        await this.$store.dispatch("profile/me")
        this.user = await {...this.$store.getters["profile/me"]}
      }
    }
}
</script>
```

#### Edit password component

```
<template>
  <div class="card">
    <div class="card-header">
      <h1>Change Password</h1>
    </div>
    <div class="card-body">
      <form ref="password_form" @submit.prevent="handleChangePassword">
        <base-input
          v-model="password"
          type="password"
          name="new_password"
          autocomplete="on"
          class="mb-3"
          prepend-icon="fa fa-key"
          placeholder="New Password"
        />
        <validation-error :errors="apiValidationErrors.password" />

        <base-input
          v-model="password_confirmation"
          type="password"
          name="confirm_password"
          autocomplete="on"
          class="mb-3"
          prepend-icon="fa fa-key"
          placeholder="Confirm Password"
        />
        <validation-error :errors="apiValidationErrors.password_confirmation" />
        <div class="my-4">
          <base-button
            type="button"
            class="btn btn-sm btn-primary"
            native-type="submit"
          >
            Change Password
          </base-button>
        </div>
      </form>
    </div>
  </div>
</template>
<script>
import BaseInput from "@/components/Inputs/BaseInput.vue";
import BaseButton from "@/components/BaseButton.vue";
import formMixin from "@/mixins/form-mixin";
import ValidationError from "@/components/ValidationError.vue";

export default {
  name: "UserPasswordCard",

  components: {
    BaseInput,
    BaseButton,
    ValidationError,
  },

  mixins: [formMixin],

  props: {
    user: Object,
  },

  data() {
    return {
      password: null,
      password_confirmation: null,
    };
  },

  methods: {
    async handleChangePassword() {
      if (["1", "2", "3"].includes(this.user.id)) {
        this.$notify({
          type: "danger",
          message: "You are not allowed not change data of default users."
        });
        return;
      }
      this.user.password = this.password;
      this.user.password_confirmation = this.password_confirmation;

      try {
        await this.$store.dispatch("users/update", this.user);
        this.$refs["password_form"].reset();
        this.resetApiValidation();

        this.$notify({
          type: "success",
          message: "Password changed successfully.",
        });
      } catch (error) {
        this.$notify({
          type: "danger",
          message: "Oops, something went wrong!",
        });
        this.setApiValidation(error.response.data.errors);
      }
    },
  },
};
</script>
```

### Role management

The Pro theme allows you to add user roles. By default, the theme comes with **Admin**, **Creator** and **Member** roles. To access the role management example click the "**Examples/Role Management**" link in the left sidebar or add **/examples/role-management/list-roles** to the URL. Here you can add/edit new roles.
To add a new role, click the "**Add role**" button. To edit an existing role, click the dotted menu (available on every table row) and then click "**Edit**". In both cases, you will be directed to a form which allows you to modify the name and description of a role.

The store used for role functionality is found in `src\store\modules\roles-module.vue`

You can find the compoments for role functionality in `src\views\Examples\RoleManagement` folder.

#### List page

```
<div>
  <div
    class="col-12 d-flex justify-content-center justify-content-sm-between flex-wrap"
  >
    <el-select
      class="select-primary pagination-select"
      v-model="pagination.perPage"
      placeholder="Per page"
    >
      <el-option
        class="select-primary"
        v-for="item in pagination.perPageOptions"
        :key="item"
        :label="item"
        :value="item"
      >
      </el-option>
    </el-select>

    <div>
      <base-input
        v-model="query"
        type="search"
        prepend-icon="fas fa-search"
        placeholder="Search..."
        clearable
      />
    </div>
  </div>
  <el-table
    class="table-responsive align-items-center table-flush"
    header-row-class-name="thead-light"
    :data="roles"
    @sort-change="sortChange"
  >
    <div slot="empty" v-if="loading">
      <img src="/img/loading.gif" style="height: 100px; width: 100px" />
    </div>
    <el-table-column label="Name" prop="name" sortable="custom" />
    <el-table-column
      label="Created At"
      prop="created_at"
      sortable="custom"
    />
    <el-table-column align="center">
      <div slot-scope="{ row }" class="table-actions">
        <el-tooltip content="Edit" placement="top">
          <a
            type="text"
            @click="editRole(row)"
            class="table-action"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-user-edit" />
          </a>
        </el-tooltip>

        <el-tooltip content="Delete" placement="top">
          <a
            type="text"
            @click="deleteRole(row.id)"
            class="table-action table-action-delete"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-trash" />
          </a>
        </el-tooltip>
      </div>
    </el-table-column>
  </el-table>
</div>
```

#### Add/edit role

```
<div class="card-body">
  <form ref="profile_form" @submit.prevent="handleSubmit">
    <base-input
      label="Name"
      prepend-icon="fas fa-user"
      v-model="role.name"
    />
    <validation-error :errors="apiValidationErrors.name" />
    <div class="my-4">
      <base-button
        type="button"
        class="btn btn-sm btn-primary"
        native-type="submit"
      >
        Update Role
      </base-button>
    </div>
  </form>
</div>
```

### User management

The theme comes with an out of the box user management option. To access this option ,click the "**Examples/User Management**" link in the left sidebar or add **/examples/user-management/list-users** to the URL.
The first thing you will see is a list of existing users. You can add new ones by clicking the "**Add user**" button (above the table on the right). On the Add user page, you will find a form which allows you to fill out the user`s name, email, role and password.

The store used for role functionality is found in `src\store\modules\users-module.vue`

You can find the compoments for role functionality in `src\views\Examples\UserManagement` folder.

Once you add more users, the list will grow and for every user you will have edit and delete options (access these options by clicking the three dotted menu that appears at the end of every row).

```
<el-table
  class="table-responsive align-items-center table-flush"
  header-row-class-name="thead-light"
  :data="users"
  @sort-change="sortChange"
>
  <div slot="empty" v-if="loading">
    <img src="/img/loading.gif" style="height: 100px; width: 100px" />
  </div>
  <el-table-column label="Author" min-width="50px">
    <template v-slot="{ row }">
      <img
        v-if="row.profile_image"
        :src="row.profile_image"
        class="avatar rounded-circle mr-3"
      />
    </template>
  </el-table-column>

  <el-table-column
    label="Name"
    min-width="60px"
    prop="name"
    sortable="custom"
  />
  <el-table-column
    label="Email"
    min-width="90px"
    prop="email"
    sortable="custom"
  />
  <el-table-column
    label="Role"
    min-width="60px"
    prop="roles.name"
    sortable="custom"
  >
    <template v-slot="{ row }">
      <span>{{ row.roles[0].name }}</span>
    </template>
  </el-table-column>
  <el-table-column
    label="Created At"
    prop="created_at"
    min-width="100px"
    sortable="custom"
  />
  <el-table-column min-width="50px" align="center">
    <div slot-scope="{ row }" class="table-actions">
      <el-tooltip content="Edit" placement="top">
        <a
          type="text"
          @click="editUser(row)"
          class="table-action"
          data-toggle="tooltip"
          style="cursor: pointer"
        >
          <i class="fas fa-user-edit"></i>
        </a>
      </el-tooltip>

      <el-tooltip content="Delete" placement="top">
        <a
          type="text"
          @click="deleteUser(row.id)"
          class="table-action table-action-delete"
          data-toggle="tooltip"
          style="cursor: pointer"
        >
          <i class="fas fa-trash"></i>
        </a>
      </el-tooltip>
    </div>
  </el-table-column>
</el-table>
```

### Tag management

Out of the box you will have an example of tag management (for the cases in which you are developing a blog or a shop). To access this example, click the "**Examples/Tag Management**" link in the left sidebar or add **/examples/tag-management/list-tags** to the URL.
You can add and edit tags here, but you can only delete them if they are not attached to any items.

The store used for role functionality is found in `src\store\modules\tags-module.vue`

You can find the compoments for role functionality in `src\views\TagManagement` folder.

```
<div>
  <div
    class="col-12 d-flex justify-content-center justify-content-sm-between flex-wrap"
  >
    <el-select
      class="select-primary pagination-select"
      v-model="pagination.perPage"
      placeholder="Per page"
    >
      <el-option
        class="select-primary"
        v-for="item in pagination.perPageOptions"
        :key="item"
        :label="item"
        :value="item"
      >
      </el-option>
    </el-select>

    <div>
      <form>
        <base-input
          v-model="query"
          type="search"
          prepend-icon="fas fa-search"
          placeholder="Search..."
          clearable
        />
      </form>
    </div>
  </div>
  <el-table
    class="table-responsive align-items-center table-flush"
    header-row-class-name="thead-light"
    :data="tags"
    @sort-change="sortChange"
  >
    <div slot="empty" v-if="loading">
      <img src="/img/loading.gif" style="height: 100px; width: 100px" />
    </div>
    <el-table-column label="Name" prop="name" sortable="custom" />
    <el-table-column label="Color" prop="color" sortable="custom">
      <template slot-scope="{ row }">
        <span
          class="badge badge-default"
          :style="{ backgroundColor: row.color }"
          >{{ row.name }}</span
        >
      </template>
    </el-table-column>
    <el-table-column
      label="Created At"
      prop="created_at"
      sortable="custom"
    />
    <el-table-column align="center">
      <div slot-scope="{ row }" class="table-actions">
        <el-tooltip content="Edit" placement="top">
          <a
            type="text"
            @click="editTag(row)"
            class="table-action"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-user-edit"></i>
          </a>
        </el-tooltip>

        <el-tooltip content="Delete" placement="top">
          <a
            type="text"
            @click="deleteTag(row.id)"
            class="table-action table-action-delete"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-trash"></i>
          </a>
        </el-tooltip>
      </div>
    </el-table-column>
  </el-table>
</div>
```

### Category management

Out of the box you will have an example of category management (for the cases in which you are developing a blog or a shop). To access this example, click the "**Examples/Category Management**" link in the left sidebar or add **/examples/category-management/list-categories** to the URL.
You can add and edit categories here, but you can only delete them if they are not attached to any items.

The store used for category functionality is found in `src\store\modules\categories-module.vue`

You can find the compoments for category functionality in `src\views\Examples\CategoryManagement` folder.

```
<div>
  <div
    class="col-12 d-flex justify-content-center justify-content-sm-between flex-wrap"
  >
    <el-select
      class="select-primary pagination-select"
      v-model="pagination.perPage"
      placeholder="Per page"
    >
      <el-option
        class="select-primary"
        v-for="item in pagination.perPageOptions"
        :key="item"
        :label="item"
        :value="item"
      >
      </el-option>
    </el-select>

    <div>
      <form>
        <base-input
          v-model="query"
          type="search"
          prepend-icon="fas fa-search"
          placeholder="Search..."
          clearable
        />
      </form>
    </div>
  </div>
  <el-table
    class="table-responsive align-items-center table-flush"
    header-row-class-name="thead-light"
    :data="categories"
    @sort-change="sortChange"
  >
    <el-table-column label="Name" prop="name" sortable />
    <el-table-column label="Description" prop="description" sortable />
    <el-table-column label="Created At" prop="created_at" sortable />
    <el-table-column align="center">
      <div slot-scope="{ row }" class="table-actions">
        <el-tooltip content="Edit" placement="top">
          <a
            type="text"
            @click="editCategory(row)"
            class="table-action"
            data-toggle="tooltip"
          >
            <i class="fas fa-user-edit"></i>
          </a>
        </el-tooltip>

        <el-tooltip content="Delete" placement="top">
          <a
            type="text"
            @click="deleteCategory(row.id)"
            class="table-action table-action-delete"
            data-toggle="tooltip"
          >
            <i class="fas fa-trash"></i>
          </a>
        </el-tooltip>
      </div>
    </el-table-column>
  </el-table>
</div>
```

### Item management

Item management is the most advanced example included in the Pro theme, because every item has a picture, belongs to a category and has multiple tags. To access this example click the "**Examples/Item Management**" link in the left sidebar or add **/examples/item-management/list-items** to the URL.
Here you can manage the items. A list of items will appear once you start adding them (to access the add page click "**Add item**").
On the add page, besides the Name and Description fields (which are present in most of the CRUD examples) you can see a category dropdown, which contains the categories you added, a file input and a tag multi select. If you did not add any categories or tags, please go to the corresponding sections (category management, tag management) and add some.

The store used for roles functionality is found in `src\store\modules\items-module.vue`

You can find the compoments for items functionality in `src\views\Examples\ItemManagement` folder.

#### List Items

```
<div>
  <div
    class="col-12 d-flex justify-content-center justify-content-sm-between flex-wrap"
  >
    <el-select
      class="select-primary pagination-select"
      v-model="pagination.perPage"
      placeholder="Per page"
    >
      <el-option
        class="select-primary"
        v-for="item in pagination.perPageOptions"
        :key="item"
        :label="item"
        :value="item"
      >
      </el-option>
    </el-select>
    <div>
      <base-input
        v-model="query"
        type="search"
        prepend-icon="fas fa-search"
        placeholder="Search..."
        clearable
      />
    </div>
  </div>
  <el-table
    class="table-responsive align-items-center table-flush"
    header-row-class-name="thead-light"
    :data="items"
    @sort-change="sortChange"
  >
    <div slot="empty" v-if="loading">
      <img src="/img/loading.gif" style="height: 100px; width: 100px" />
    </div>
    <el-table-column
      label="Name"
      min-width="240px"
      prop="name"
      sortable="custom"
    />
    <el-table-column
      label="Category"
      min-width="140px"
      prop="category.name"
      sortable="custom"
    />

    <el-table-column label="Picture" min-width="150px">
      <template v-slot="{ row }">
        <img
          v-if="row.image"
          :src="row.image"
          style="width: 100px; height: auto"
          alt="avatar"
        />
      </template>
    </el-table-column>

    <el-table-column
      label="Tags"
      min-width="170px"
      max-width="400px"
      prop="tags.name"
      sortable="custom"
    >
      <template slot-scope="{ row }">
        <span
          v-for="(tag, index) in row.tags"
          :key="'tag' + index"
          class="badge badge-default"
          :style="{ backgroundColor: tag.color, margin: '.1rem' }"
          >{{ tag.name }}</span
        >
      </template>
    </el-table-column>
    <el-table-column
      label="Created At"
      prop="created_at"
      min-width="190px"
      sortable="custom"
    />
    <el-table-column min-width="120px" align="center">
      <div slot-scope="{ row }" class="table-actions">
        <el-tooltip content="Edit" placement="top">
          <a
            type="text"
            @click="editItem(row)"
            class="table-action"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-user-edit"></i>
          </a>
        </el-tooltip>
        <el-tooltip content="Delete" placement="top">
          <a
            type="text"
            @click="deleteItem(row.id)"
            class="table-action table-action-delete"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-trash"></i>
          </a>
        </el-tooltip>
      </div>
    </el-table-column>
  </el-table>
</div>
```

#### Add/Edit Item

```
<card>
  <div slot="header" class="row align-items-center">
    <div class="col-8">
      <h3 class="mb-0">Edit Item</h3>
    </div>
    <div class="col-4 text-right">
      <base-button
        @click="goBack"
        type="button"
        class="btn btn-sm btn-primary"
        >Back to list</base-button
      >
    </div>
  </div>
  <div class="card-body">
    <form ref="profile_form" @submit.prevent="handleSubmit">
      <div class="form-group">
        <label class="form-control-label"> Picture </label>
        <div v-if="file" class="profile-image card-img pb-4">
          <img
            :src="`${item.image}`"
            class="profile-image argon-image"
          />
        </div>
        <div v-else class="profile-image">
          <img src="/img/placeholder.jpg" class="argon-image" />
        </div>
        <div class="image-upload">
          <base-button
            v-if="file"
            type="button"
            class="btn btn-sm btn-danger"
            @click="removeImage"
          >
            <span>
              <i class="fa fa-times" />
              Remove
            </span>
          </base-button>
          <base-button type="button" class="btn btn-sm btn-primary">
            <label v-if="!file" for="imageInput" class="mb-0"
              >Select image</label
            >
            <label v-else for="imageInput" class="mb-0">Change</label>
            <input
              id="imageInput"
              ref="imageInput"
              accept="image/*"
              type="file"
              style="display: none"
              @change="onSelectFile"
            />
          </base-button>
        </div>
      </div>
      <validation-error :errors="apiValidationErrors.attachment" />

      <base-input
        label="Name"
        prepend-icon="fas fa-user"
        v-model="item.name"
      />
      <validation-error :errors="apiValidationErrors.name" />

      <base-input label="Description">
        <html-editor v-model="item.description" name="editor" />
      </base-input>
      <validation-error :errors="apiValidationErrors.description" />

      <base-input label="Category">
        <el-select
          name="category"
          v-model="item.category.id"
          prepend-icon="fas fa-user"
        >
          <el-option
            v-for="single_category in all_categories"
            :key="single_category.id"
            :value="single_category.id"
            :label="single_category.name"
          >
          </el-option>
        </el-select>
      </base-input>

      <base-input label="Tags">
        <el-select v-model="tags" multiple placeholder="Select...">
          <el-option
            v-for="single_tag in all_tags"
            :key="single_tag.id"
            :value="single_tag.id"
            :label="single_tag.name"
          >
          </el-option>
        </el-select>
      </base-input>

      <base-input label="Status">
        <base-radio v-model="item.status" name="published" class="mb-3">
          Published
        </base-radio>
        <base-radio v-model="item.status" name="draft" class="mb-3">
          Draft
        </base-radio>
        <base-radio v-model="item.status" name="archive" class="mb-3">
          Archive
        </base-radio>
      </base-input>

      <base-input label="Show on homepage?">
        <base-switch
          class="mr-1"
          v-model="item.is_on_homepage"
        ></base-switch>
      </base-input>

      <base-input label="Date">
        <flat-picker
          slot-scope="{ focus, blur }"
          @on-open="focus"
          @on-close="blur"
          :config="{ allowInput: true }"
          class="form-control datepicker"
          v-model="item.date_at"
        >
        </flat-picker>
      </base-input>
      <validation-error :errors="apiValidationErrors.date_at" />

      <div class="my-4">
        <base-button
          type="button"
          class="btn btn-sm btn-primary"
          native-type="submit"
        >
          Update Item
        </base-button>
      </div>
    </form>
  </div>
</card>
```

## Table of Contents

- [Versions](#versions)
- [Demo](#demo)
- [Documentation](#documentation)
- [File Structure](#file-structure)
- [Browser Support](#browser-support)
- [Resources](#resources)
- [Reporting Issues](#reporting-issues)
- [Licensing](#licensing)
- [Useful Links](#useful-links)

## Versions

[<img src="https://github.com/creativetimofficial/public-assets/blob/master/logos/html-logo.jpg" height="80" />](#)
[<img src="https://github.com/creativetimofficial/public-assets/blob/master/logos/laravel_logo.png" height="80" />](#)
[<img src="https://github.com/creativetimofficial/public-assets/blob/master/logos/vue.jpg" height="80" />](#)
[<img src="https://github.com/creativetimofficial/public-assets/blob/master/logos/json-api.png" height="75" />](#)

| HTML                                                                                                                                                                                           | Laravel                                                                                                                                                                                                           |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [![Argon Dashboard Pro HTML](https://s3.amazonaws.com/creativetim_bucket/products/137/thumb/opt_adp_thumbnail.jpg)](https://www.creative-tim.com/product/argon-dashboard-pro?ref=vadpl-readme) | [![Argon Dashboard Pro Laravel](https://s3.amazonaws.com/creativetim_bucket/products/146/thumb/opt_adp_laravel_thumbnail.jpg)](https://www.creative-tim.com/product/argon-dashboard-pro-laravel?ref=vadpl-readme) |

| Vue                                                                                                                                                                                                        | Vue & Laravel                                                                                                                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [![Vue Argon Dashboard Pro HTML](https://s3.amazonaws.com/creativetim_bucket/products/159/thumb/opt_adp_vue_thumbnail.jpg)](https://www.creative-tim.com/product/vue-argon-dashboard-pro?ref=vadpl-readme) | [![Vue Argon Dashboard Pro Laravel ](https://s3.amazonaws.com/creativetim_bucket/products/353/thumb/opt_adp_vue_laravel_thumbnail.jpg)](https://www.creative-tim.com/product/vue-argon-dashboard-pro-laravel?ref=vadpl-readme) |

## Demo

| Register                                                                                                                                                                                                                   | Login                                                                                                                                                                                                             | Dashboard                                                                                                                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [![Register](https://raw.githubusercontent.com/creativetimofficial/public-assets/master/vue-argon-dashboard-laravel-pro/register.png)](https://vue-argon-dashboard-pro-laravel.creative-tim.com/register?ref=vadpl-readme) | [![Login](https://raw.githubusercontent.com/creativetimofficial/public-assets/master/vue-argon-dashboard-laravel-pro/login.png)](https://vue-argon-dashboard-pro-laravel.creative-tim.com/login?ref=vadpl-readme) | [![Dashboard](https://raw.githubusercontent.com/creativetimofficial/public-assets/master/vue-argon-dashboard-laravel-pro/dashboard.png)](https://vue-argon-dashboard-pro-laravel.creative-tim.com/?ref=vadpl-readme) |

| Profile Page                                                                                                                                                                                                                               | Users Page                                                                                                                                                                                                                                           | Tables Page                                                                                                                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [![Profile Page](https://raw.githubusercontent.com/creativetimofficial/public-assets/master/vue-argon-dashboard-laravel-pro/profile.png)](https://vue-argon-dashboard-pro-laravel.creative-tim.com/examples/user-profile?ref=vadpl-readme) | [![Users Page](https://raw.githubusercontent.com/creativetimofficial/public-assets/master/vue-argon-dashboard-laravel-pro/users.png)](https://vue-argon-dashboard-pro-laravel.creative-tim.com/examples/user-management/list-users?ref=vadpl-readme) | [![Tables Page](https://raw.githubusercontent.com/creativetimofficial/public-assets/master/vue-argon-dashboard-laravel-pro/table.png)](https://vue-argon-dashboard-pro-laravel.creative-tim.com/tables/paginated?ref=vadpl-readme) |

[View More](https://vue-argon-dashboard-pro-laravel.creative-tim.com/?ref=vadpl-readme)

## Documentation

The documentation for the Vue Argon Dashboard PRO Laravel is hosted at our [website](https://demos.creative-tim.com/vue-argon-dashboard-pro-laravel/documentation?ref=vadpl-github-readme).

## File Structure

Within the download you'll find the following directories and files:

```
├───vue-argon-dashboard-pro
│   App.vue
│   main.js
│   polyfills.js
│
├───assets
│   ├───css
│   │   │   style.css
│   │   │
│   │   └───nucleo
│   └───sass
│       │   argon.scss
│       │
│       ├───core
│       └───custom
├───axios
│       index.js
│
├───components
│   │   Badge.vue
│   │   BaseAlert.vue
│   │   BaseButton.vue
│   │   BaseDropdown.vue
│   │   BaseHeader.vue
│   │   BasePagination.vue
│   │   BaseProgress.vue
│   │   BaseSlider.vue
│   │   BaseSwitch.vue
│   │   BaseTable.vue
│   │   ButtonCheckbox.vue
│   │   ButtonRadioGroup.vue
│   │   CloseButton.vue
│   │   index.js
│   │   LoadingPanel.vue
│   │   Modal.vue
│   │   NavbarToggleButton.vue
│   │   ValidationError.vue
│   │
│   ├───Breadcrumb
│   │       Breadcrumb.vue
│   │       BreadcrumbItem.vue
│   │       RouteBreadcrumb.vue
│   │
│   ├───Cards
│   │       Card.vue
│   │       StatsCard.vue
│   │
│   ├───Charts
│   │       BarChart.js
│   │       config.js
│   │       DoughnutChart.js
│   │       globalOptionsMixin.js
│   │       LineChart.js
│   │       optionHelpers.js
│   │       PieChart.js
│   │       roundedCornersExtension.js
│   │
│   ├───Collapse
│   │       Collapse.vue
│   │       CollapseItem.vue
│   │
│   ├───Feed
│   │       Comment.vue
│   │
│   ├───Inputs
│   │       BaseCheckbox.vue
│   │       BaseInput.vue
│   │       BaseRadio.vue
│   │       DropzoneFileUpload.vue
│   │       FileInput.vue
│   │       HtmlEditor.vue
│   │       IconCheckbox.vue
│   │       TagsInput.vue
│   │
│   ├───Navbar
│   │       BaseNav.vue
│   │       NavbarToggleButton.vue
│   │
│   ├───NotificationPlugin
│   │       index.js
│   │       Notification.vue
│   │       Notifications.vue
│   │
│   ├───SidebarPlugin
│   │       index.js
│   │       SideBar.vue
│   │       SidebarItem.vue
│   │
│   ├───Tabs
│   │       Tab.vue
│   │       Tabs.vue
│   │
│   ├───Timeline
│   │       TimeLine.vue
│   │       TimeLineItem.vue
│   │
│   └───WorldMap
│           AsyncWorldMap.vue
│           WorldMap.vue
│
├───directives
│       click-ouside.js
│
├───middleware
│       admin.js
│       admin_creator.js
│       auth.js
│       guest.js
│
├───mixins
│       form-mixin.js
│
├───plugins
│       dashboard-plugin.js
│       globalComponents.js
│       globalDirectives.js
│
├───router
│       index.js
│       routes.js
│       starterRouter.js
│
├───store
│   │   index.js
│   │
│   ├───modules
│   │       auth.js
│   │       categories-module.js
│   │       items-module.js
│   │       profile-module.js
│   │       reset.js
│   │       roles-module.js
│   │       tags-module.js
│   │       users-module.js
│   │
│   └───services
│           categories-service.js
│           items-service.js
│           profile-service.js
│           roles-service.js
│           tags-service.js
│           users-service.js
│
├───util
│       throttle.js
│
└───views
    │   Charts.vue
    │   Widgets.vue
    │
    ├───Calendar
    │       Calendar.vue
    │
    ├───Components
    │       Buttons.vue
    │       Cards.vue
    │       GridSystem.vue
    │       Icons.vue
    │       Notifications.vue
    │       Typography.vue
    │
    ├───Dashboard
    │       ActivityFeed.vue
    │       AlternativeDashboard.vue
    │       Dashboard.vue
    │       LightTable.vue
    │       PageVisitsTable.vue
    │       ProgressTrackList.vue
    │       SocialTrafficTable.vue
    │       TaskList.vue
    │       UserList.vue
    │
    ├───Examples
    │   │   UserProfile.vue
    │   │
    │   ├───CategoryManagement
    │   │       AddCategoryPage.vue
    │   │       EditCategoryPage.vue
    │   │       ListCategoryPage.vue
    │   │
    │   ├───ItemManagement
    │   │       AddItemPage.vue
    │   │       EditItemPage.vue
    │   │       ListItemPage.vue
    │   │
    │   ├───RoleManagement
    │   │       AddRolePage.vue
    │   │       EditRolePage.vue
    │   │       ListRolePage.vue
    │   │
    │   ├───TagManagement
    │   │       AddTagPage.vue
    │   │       EditTagPage.vue
    │   │       ListTagPage.vue
    │   │
    │   ├───UserManagement
    │   │       AddUserPage.vue
    │   │       EditUserPage.vue
    │   │       ListUserPage.vue
    │   │
    │   └───UserProfile
    │           UserEditCard.vue
    │           UserPasswordCard.vue
    │
    ├───Forms
    │   │   FormComponents.vue
    │   │   FormElements.vue
    │   │   FormValidation.vue
    │   │
    │   └───FormValidation
    │           BrowserDefaultsValidation.vue
    │           CustomStylesValidation.vue
    │           ServerSideValidation.vue
    │
    ├───GeneralViews
    │       NotFoundPage.vue
    │
    ├───Layout
    │       Content.vue
    │       ContentFooter.vue
    │       DashboardLayout.vue
    │       DashboardNavbar.vue
    │
    ├───Maps
    │       API_KEY.js
    │       GoogleMaps.vue
    │       VectorMaps.vue
    │
    ├───Pages
    │   │   AuthLayout.vue
    │   │   Home.vue
    │   │   Lock.vue
    │   │   Login.vue
    │   │   Pricing.vue
    │   │   Register.vue
    │   │   TimeLinePage.vue
    │   │   UserProfile.vue
    │   │
    │   └───UserProfile
    │           EditProfileForm.vue
    │           UserCard.vue
    │
    ├───Password
    │       Email.vue
    │       Reset.vue
    │
    ├───Starter
    │       SampleFooter.vue
    │       SampleLayout.vue
    │       SampleNavbar.vue
    │       SamplePage.vue
    │
    ├───Tables
    │   │   PaginatedTables.vue
    │   │   projects.js
    │   │   RegularTables.vue
    │   │   SortableTables.vue
    │   │   users.js
    │   │   users2.js
    │   │
    │   ├───PaginatedTables
    │   │       clientPaginationMixin.js
    │   │
    │   └───RegularTables
    │           CheckboxColoredTable.vue
    │           CheckboxTable.vue
    │           DarkTable.vue
    │           InlineActionsTable.vue
    │           LightTable.vue
    │           StripedTable.vue
    │           TranslucentTable.vue
    │
    └───Widgets
            CalendarWidget.vue
            CreditCard.vue
            MembersCard.vue
            PaypalCard.vue
            ProgressTrackList.vue
            StatsCards.vue
            TaskList.vue
            TimelineCard.vue
            VectorMapCard.vue
            VisaCard.vue
```

## Browser Support

At present, we officially aim to support the last two versions of the following browsers:

<img src="https://github.com/creativetimofficial/public-assets/blob/master/logos/chrome-logo.png?raw=true" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/firefox-logo.png" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/edge-logo.png" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/safari-logo.png" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/opera-logo.png" width="64" height="64">

## Resources

- Demo: <https://vue-argon-dashboard-pro-laravel.creative-tim.com/?ref=vadpl-readme>
- Download Page: <https://www.creative-tim.com/product/vue-argon-dashboard-pro-laravel?ref=vadpl-readme>
- Documentation: <https://vue-argon-dashboard-pro-laravel.creative-tim.com/documentation?ref=vadpl-readme>
- License Agreement: <https://www.creative-tim.com/license>
- Support: <https://www.creative-tim.com/contact-us>
- Issues: [Github Issues Page](https://github.com/creativetimofficial/ct-vue-argon-dashboard-pro-laravel/issues)
- **Dashboards:**

| HTML                                                                                                                                                                                           | Laravel                                                                                                                                                                                                           |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [![Argon Dashboard Pro HTML](https://s3.amazonaws.com/creativetim_bucket/products/137/thumb/opt_adp_thumbnail.jpg)](https://www.creative-tim.com/product/argon-dashboard-pro?ref=vadpl-readme) | [![Argon Dashboard Pro Laravel](https://s3.amazonaws.com/creativetim_bucket/products/146/thumb/opt_adp_laravel_thumbnail.jpg)](https://www.creative-tim.com/product/argon-dashboard-pro-laravel?ref=vadpl-readme) |

| Vue                                                                                                                                                                                                        | Vue & Laravel                                                                                                                                                                                                                 |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [![Vue Argon Dashboard Pro HTML](https://s3.amazonaws.com/creativetim_bucket/products/159/thumb/opt_adp_vue_thumbnail.jpg)](https://www.creative-tim.com/product/vue-argon-dashboard-pro?ref=vadpl-readme) | [![Vue Argon Dashboard Pro Laravel](https://s3.amazonaws.com/creativetim_bucket/products/353/thumb/opt_adp_vue_laravel_thumbnail.jpg)](https://www.creative-tim.com/product/vue-argon-dashboard-pro-laravel?ref=vadpl-readme) |

## Change log

Please see the [changelog](CHANGELOG.md) for more information on what has changed recently.

## Credits

- [Creative Tim](https://creative-tim.com/?ref=vadpl-readme)
- [UPDIVISION](https://updivision.com)

## Reporting Issues

We use GitHub Issues as the official bug tracker for the Argon Kit. Here are some advices for our users that want to report an issue:

1. Make sure that you are using the latest version of the Argon Kit. Check the CHANGELOG from your dashboard on our [website](https://www.creative-tim.com/?ref=vadpl-readme).
2. Providing us reproducible steps for the issue will shorten the time it takes for it to be fixed.
3. Some issues may be browser specific, so specifying in what browser you encountered the issue might help.

## Licensing

- Copyright Creative Tim (https://www.creative-tim.com/?ref=vadpl-readme)
- Creative Tim License (https://www.creative-tim.com/license).

## Useful Links

- [Tutorials](https://www.youtube.com/channel/UCVyTG4sCw-rOvB9oHkzZD1w?ref=vadpl-readme)
- [Affiliate Program](https://www.creative-tim.com/affiliates/new?ref=vadpl-readme) (earn money)
- [Blog Creative Tim](http://blog.creative-tim.com/?ref=vadpl-readme)
- [Free Products](https://www.creative-tim.com/bootstrap-themes/free?ref=vadpl-readme) from Creative Tim
- [Premium Products](https://www.creative-tim.com/bootstrap-themes/premium?ref=vadpl-readme) from Creative Tim
- [React Products](https://www.creative-tim.com/bootstrap-themes/react-themes?ref=vadpl-readme) from Creative Tim
- [Angular Products](https://www.creative-tim.com/bootstrap-themes/angular-themes?ref=vadpl-readme) from Creative Tim
- [VueJS Products](https://www.creative-tim.com/bootstrap-themes/vuejs-themes?ref=vadpl-readme) from Creative Tim
- [More products](https://www.creative-tim.com/bootstrap-themes?ref=vadpl-readme) from Creative Tim
- Check our Bundles [here](https://www.creative-tim.com/bundles?ref=vadpl-readme)

## Social Media

### Creative Tim:

Twitter: <https://twitter.com/CreativeTim?ref=vadpl-readme>

Facebook: <https://www.facebook.com/CreativeTim?ref=vadpl-readme>

Dribbble: <https://dribbble.com/creativetim?ref=vadpl-readme>

Instagram: <https://www.instagram.com/CreativeTimOfficial?ref=vadpl-readme>

### Updivision:

Twitter: <https://twitter.com/updivision?ref=vadpl-readme>

Facebook: <https://www.facebook.com/updivision?ref=vadpl-readme>

Linkedin: <https://www.linkedin.com/company/updivision?ref=vadpl-readme>

Updivision Blog: <https://updivision.com/blog/?ref=vadpl-readme>

## Credits

- [Creative Tim](https://creative-tim.com/?ref=vadpl-readme)
- [UPDIVISION](https://updivision.com)
