# Page Structure

## **../src/index.html**

```markup
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Mintone - Angular 8+ Admin Template</title>
  <base href="/">

  <!--IE11-->
  <!-- HTML5 Shim and Respond.js IE11 support of HTML5 elements and media queries -->
  <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
  <!--[if lt IE 11]>
  <script src="https://oss.maxcdn.com/libs/html5shiv/3.7.0/html5shiv.js"></script>
  <script src="https://oss.maxcdn.com/libs/respond.js/1.4.2/respond.min.js"></script>
  <![endif]-->

  <!-- Meta -->
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=0, minimal-ui">
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="description" content="" />
  <meta name="keywords" content="">
  <meta name="author" content="Phoenixcoded" />

  <!-- Favicon icon -->
  <link rel="icon" type="image/x-icon" href="favicon.ico">
</head>
<body>
  <app-root></app-root>
</body>
</html>
```

## **../src/app/app.component.html**

```markup
<router-outlet>
    <!-- loadChildren from app-routing.module.ts with admin.component.html or auth.component.html -->
</router-outlet>
```

## **../src/app/app-routing.module.ts**

```typescript
import { AdminComponent } from './theme/layout/admin/admin.component';
import { AuthComponent } from './theme/layout/auth/auth.component';

const routes: Routes = [
  {
    path: '',
    component: AdminComponent,
    children: [
      // load children modules with lazy load routing for header, side nav common structure, like, dashboard, blank page, widget, etc..
    ]
  },
  {
    path: '',
    component: AuthComponent,
    children: [
      // load children modules with lazy load routing for without common structure, like login, signup, reset password, lock screen, etc..
    ]
  }
];
```

## **../src/app/theme/layout/admin/admin.component.html**

```markup
<app-navigation></app-navigation> <!-- for side nav - navigation.component.html -->
<app-nav-bar></app-nav-bar> <!-- for header - nav-bar.component.html -->
<div class="pcoded-main-container">
    <div class="pcoded-content">
        <div class="main-body">
          <div class="page-wrapper">
            <router-outlet>
                <!-- page main body - loadChildren as main page body from src/app/demo/... -->
            </router-outlet>
          </div>
        </div>
    </div>
</div>
```

## **../src/app/theme/layout/auth/auth.component.html**

```markup
<router-outlet>
    <!-- loadChildren component for auth.component at app-routing.module.ts for authentication blank pages without nav, header, etc. -->
</router-outlet>
```

