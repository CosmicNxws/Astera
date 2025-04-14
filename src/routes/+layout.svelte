<script>
    import Header from '../lib/components/Header.svelte';
    import Footer from '../lib/components/Footer.svelte';
  </script>
  
  <div class="layout">
   
    
    <main>
      <slot /> <!-- This renders your page content -->
    </main>
    <Header />
    <Footer />
  </div>
  
  <style>
    .layout {
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }
    
    main {
      flex: 1;
      padding-top: 80px; /* Adjust if your header has different height */
    }
  </style>