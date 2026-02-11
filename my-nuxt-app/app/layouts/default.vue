<template>
  <div>
    <header class="head1 bg-blue-200">
        <ul class="list">
            <li>home</li>
            <li>project</li>
            <li>about</li>
        </ul>
    </header>

    <main>
      <slot />
    </main>

    <footer>
        <p>this is about the footer</p>
        
        © 2026 Moges App</footer>
  </div>
</template>


<style>
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