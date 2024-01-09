<script>
  import "../app.css";
  let pace = "6:30";
  let km = 0;
  let time = splitPace() * km;
  let timeHour = time / 60;
  let speedKMH = 0;

  function splitPace() {
    const [min, sec] = pace.split(":");
    return parseInt(min) + parseInt(sec) / 60;
  }

  function setTimes() {
    time = splitPace() * km;
    timeHour = Math.round((time / 60) * 100) / 100;
  }

  function setSpeed() {
    speedKMH = Math.round((60 / splitPace()) * 100) / 100;
  }

  setSpeed();
</script>

<div class="h-screen flex items-center justify-center p-4">
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
          ⌀ Kilometerzeit / Pace (min)
        </label>
        <input
          class="text-3xl shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          bind:value={pace}
          on:input={() => (setTimes(), setSpeed())}
          type="float"
          placeholder="Pace (1km/min)"
        />
      </div>
      <div class="mb-4">
        <label
          class="block text-gray-700 text-sm font-bold mb-2"
          for="username"
        >
          ⌀ Geschw. (km/h)
        </label>
        <input
          class="text-3xl shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          bind:value={speedKMH}
          on:input={() => setTimes()}
          type="float"
          placeholder="Pace (1km/min)"
        />
      </div>
      <hr />
      <div class="mb-4">
        <label
          class="block text-gray-700 text-sm font-bold mb-2"
          for="username"
        >
          Strecke (km)
        </label>
        <input
          class="text-3xl shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          bind:value={km}
          on:input={() => setTimes()}
          type="float"
          placeholder="Kilometer"
        />
      </div>
      <button
        class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-1 px-2 text-xs rounded"
        on:click={() => ((km = 21), setTimes())}
      >
        Halbmarathon (21km)
      </button>
      <button
        class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-1 px-2 text-xs rounded"
        on:click={() => ((km = 42), setTimes())}
      >
        Marathon (42km)
      </button>
      <button
        class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-1 px-2 text-xs rounded mt-1"
        on:click={() => ((km = 10.5), setTimes())}
      >
        Viertel­marathon (10,5km)
      </button>

      <div class="flex flex-row mt-3">
        <div class="mb-6">
          <label
            class="block text-gray-700 text-sm font-bold mb-2"
            for="password"
          >
            Zeit (min:sec)
          </label>
          <input
            class="text-3xl shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
            bind:value={time}
            type="text"
            placeholder="Deine Gesamt Zeit"
          />
        </div>
        <div class="mb-6 ml-6">
          <label
            class="block text-gray-700 text-sm font-bold mb-2"
            for="password"
          >
            Zeit (h:min)
          </label>
          <input
            class="text-3xl shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
            bind:value={timeHour}
            type="text"
            placeholder="Deine Gesamt Zeit"
          />
        </div>
      </div>
    </form>
    <a href="https://guder-service.com/impressum">
      <p class="text-center text-gray-500 text-xs">
        &copy;2024 💚 Guder-Service
      </p>
    </a>
  </div>
</div>
