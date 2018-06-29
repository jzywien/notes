# Create new angular app
`ng new ${app name}`

# Create new app with routing & scss enabled by default
`yarn ng new client --routing --style=scss`

# Generate new component
ng generate component ${component name}

# Enable routing
ng generate module app-routing

app-routing.module.ts
```
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { DashboardComponent } from '../dashboard/dashboard.component'

const routes: Routes = [
    {
        path: '', component: DashboardComponent,
    },
];

@NgModule({
    imports: [
        RouterModule.forRoot(routes)
    ],
    exports: [
        RouterModule
    ],
    declarations: []
})
export class AppRoutingModule { }
```

Add AppRoutingModule to app.module.ts

# Lazy Loading

