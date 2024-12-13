<div align="center">
  <a href="https://vitejs.dev/">
    <img width="200" height="200" hspace="10" src="https://vitejs.dev/logo.svg" alt="vite logo" />
  </a>
  <h1>What is ddev-wordpress-vite?</h1>
  <p>
This add-on simply adds a yaml config that exposes and routes the ports necessary to load up the Vite dev server ande make use of their HMR features inside DDEV.

You can read more about ViteJS on [vitejs.dev](https://vitejs.dev)
</p>
</div>

## Getting started

Install the DDEV add-on:

For DDEV v1.23.5 or above run

```shell
ddev add-on get mrOttoW/ddev-wordpress-vite
```

For earlier versions of DDEV run

```shell
ddev get mrOttoW/ddev-wordpress-vite
```

Then restart your project

```shell
ddev restart
```

Or simply bootstrap a new WP project with these combined commands using this add-on: (make sure to change title & URL inside `wp core install` command accordingly)

For DDEV v1.23.5 or above run
```shell
mkdir wordpress 
ddev config --docroot=wordpress --project-type=wordpress
ddev add-on get mrOttoW/ddev-wordpress-vite
ddev start
ddev exec wp core download --path="wordpress"
ddev exec wp core install --path="wordpress" --title="WPVitePlayground" --admin_name="admin" --admin_password="password" --admin_email="admin@local.ddev" --url="https://wp-vite-playground.ddev.site"
```
For earlier versions of DDEV run

```shell
mkdir wordpress 
ddev config --docroot=wordpress --project-type=wordpress
ddev get mrOttoW/ddev-wordpress-vite
ddev start
ddev exec wp core download --path="wordpress"
ddev exec wp core install --path="wordpress" --title="WPVitePlayground" --admin_name="admin" --admin_password="password" --admin_email="admin@local.ddev" --url="https://wp-vite-playground.ddev.site"
```
