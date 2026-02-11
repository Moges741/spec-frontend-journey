<template>
  <div>
    <header class="head1 bg-blue-200">
        <ul class="list">
            <NuxtLink to="/">home</NuxtLink>
            <NuxtLink to="/dashboard">dashboard</NuxtLink>
            <NuxtLink to="/about">about</NuxtLink>
            <NuxtLink to="/quotes">Quotes</NuxtLink>
        </ul>
    </header>

    <main>
      <slot />
    </main>
      </div>
<!-- i wanna make its margin bottom 0 to the page it needs to be 0 , just take footer's place needs to be last page ....  -->
  <div class="flex flex-col min-h-screen">
    <!-- Page content -->
    <main class="flex-grow text-center">
      <p>Some content here...</p>
    </main>


    <footer class="bg-gray-800 text-white p-4 text-center">
      Footer Content.....................
    </footer>
  </div>


</template>


<style>
footer{
    margin-bottom: 0;

}
.head1{
    padding: 5px;
    margin: 0;
 
}
.list{
       display: flex;
    justify-content: end;
    gap: 20px;
}
.list li{
    list-style: none;
    cursor: pointer;
}

</style>