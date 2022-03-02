<template>
  <div class="container">
    <div class="row navv">
      <div class="col-md-12">
        <nav
          class="navbar navbar-expand-lg navbar-dark bg-danger"
          style="height: 150%"
        >
          <button
            class="navbar-toggler"
            type="button"
            data-toggle="collapse"
            data-target="#navbarTogglerDemo01"
            aria-controls="navbarTogglerDemo01"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarTogglerDemo01">
            <ul class="navbar-nav mt-2 mt-lg-0" style="margin-right: 45em">
              <li class="nav-item active">
                <NuxtLink class="ml-2 mr-4 text-white ml-4" to="/"
                  >Home</NuxtLink
                >
              </li>
              <li class="nav-item active">
                <NuxtLink class="ml-2 mr-4 text-white" to="Menu">Menu</NuxtLink>
              </li>
              <li class="nav-item active">
                <NuxtLink class="ml-2 mr-4 text-white" to="Contact"
                  >Contact</NuxtLink
                >
              </li>
            </ul>
            <a href="https://api.whatsapp.com/send?phone=6282116442464"
              ><Iconw
            /></a>
          </div>
        </nav>
      </div>
    </div>
  </div>
</template>


  // <div class="container">
  //   <div class="row navv">
  //     <div class="col-md-12">
  //       <nav class="navbar bg-danger responsive" style="height: 150%">
  //         <div class="nav justify-content">
  //           <NuxtLink class="ml-2 mr-4 text-white" to="/">Home</NuxtLink>
  //           <NuxtLink class="mr-4 text-white" to="Menu">Menu</NuxtLink>
  //           <NuxtLink class="text-white" to="Contact" style="margin-right: 50em"
  //             >Contact</NuxtLink
  //           >
  //           <a href="https://api.whatsapp.com/send?phone=6282116442464"
  //             ><Iconw
  //           /></a>

  //           <!-- <a href="" class="mr-3"><Iconf /></a>
  //           <a href="" class="mr-3"><Icontele /></a> -->
  //         </div>
  //       </nav>
  //     </div>
  //   </div>
  // </div>