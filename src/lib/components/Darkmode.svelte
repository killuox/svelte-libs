<script>
    let isDarkMode = false;
  
    function toggleDarkMode() {
      isDarkMode = !isDarkMode;
      // add dark mode class to the body
        document.body.classList.toggle('dark');
    }
  </script>
  
  <div class="dark-mode-switcher">
    <input
      type="checkbox"
      id="darkModeToggle"
      bind:checked={isDarkMode}
      on:change={toggleDarkMode}
    />
    <label for="darkModeToggle">Dark Mode</label>
  </div>
  
  <style>
    /* Add your CSS styles for the dark mode switcher here */
    .dark-mode-switcher {
      display: flex;
      align-items: center;
      margin: 1rem;
    }
  
    /* You can style the label and input to create a visually appealing switcher */
    label {
      margin-left: 0.5rem;
    }
  </style>
  