![Navigation drawer](assets/navigation-drawer.gif)
# Our App
- Content management system (CMS)
- Three modules: customers, orders, and messages.
- Navigation drawer to switch between modules

# Do's of Navigation Drawers
- Make the placement noticeable
- Keep the links concise, such as "Home", "Orders"
- Organize links in order of importance
- Most visited on top
- Use icon when possible to convey meaning

# Don'ts of Navigation Drawers
- Mix navigation drawers with other site navigation metaphors, such as footer, navs, topnavs, etc.
- Put too much text on your destination links so you have to wrap or shrink your font
- Reuse icons for multiple purposes
- Put divers between each items; groups are ok
- Put branding as the header for your navigation drawer

# Three Kinds of Navigation Drawers
- Slide-over or modal
- Slide-in
- Always open

# Import Material modules

```ts
// app.module.ts
 imports: [
    Modules,
    // Material section
    BrowserAnimationsModule,
    MatButtonModule,
    MatIconModule,
    MatSidenavModule,
  ],
```

# CSS import
  
  ```css
  /* styles.scss */
  @import '~@angular/material/prebuilt-themes/deeppurple-amber.css';
  ```

# App.component.html
```html 
<mat-drawer-container class="container" autosize>
  <!-- #drawer is capture for the button to use the toggle method -->
  <mat-drawer #drawer class="sidenav" >
    <!-- everything inside mat-drawer is the content of the menu -->
    <p>Menu</p>
  </mat-drawer>
  <div class="sidenav-content">
    <!-- button opens the menu -->
      <button mat-icon-button (click)="drawer.toggle()" >
        <!-- gives the menu icon -->
        <mat-icon>menu</mat-icon>
      </button>
  </div>
</mat-drawer-container>
```

# app.component.scss
```scss
// makes the menu come from the side
.container{
  position:absolute;
  top:0;
  left:0;
  right:0;
  bottom:0;
}

// sets the side of the menu content
// .container is use to target the element and the .mat-drawer to target the general material class
.container .mat-drawer{
  padding-left: 20px;
  padding-right: 20px;
  min-width: 200px;
}
```
