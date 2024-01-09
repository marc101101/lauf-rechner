<script>
  import "../app.css";
</script>

<div class="h-screen flex items-center justify-center">
  <div class="w-full max-w-sm">
    <h1
      class="mb-4 text-4xl font-extrabold leading-none tracking-tight text-gray-900 md:text-5xl lg:text-6x"
    >
      Lauf Rechner 🏃
    </h1>

    <br />
    <form class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4">
      <div class="mb-4">
        <label
          class="block text-gray-700 text-sm font-bold mb-2"
          for="username"
        >
          Pace (1km/min)
        </label>
        <input
          class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          id="paste"
          type="text"
          placeholder="Durschnittliche Kilometerzeit"
        />
      </div>
      <div class="mb-4">
        <label
          class="block text-gray-700 text-sm font-bold mb-2"
          for="username"
        >
          Kilometer
        </label>
        <input
          class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          id="paste"
          type="text"
          placeholder="Kilometer"
        />
      </div>
      <div class="mb-6">
        <label
          class="block text-gray-700 text-sm font-bold mb-2"
          for="password"
        >
          Gesamt Zeit
        </label>

        <input
          class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          id="paste"
          type="text"
          placeholder="Deine Gesamt Zeit"
        />
      </div>
    </form>
    <a href="https://guder-service.com/impressum">
      <p class="text-center text-gray-500 text-xs">&copy;2024 Guder-Service</p>
    </a>
  </div>
</div>
