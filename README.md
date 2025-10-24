# Lernol
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Lernol – The Ultimate Learning Platform</title>

  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Inter', sans-serif;
      background: linear-gradient(to bottom right, #1e1b4b, #312e81);
      color: white;
      min-height: 100vh;
      overflow-x: hidden;
    }
    .hidden { display: none; }
    .card {
      @apply bg-white/10 backdrop-blur-md p-6 rounded-2xl shadow-xl border border-white/20;
    }
    button {
      @apply bg-indigo-500 hover:bg-indigo-600 text-white font-semibold py-2 px-5 rounded-lg transition-all duration-200;
    }
    .disabled {
      @apply opacity-50 cursor-not-allowed;
    }
  </style>
</head>

<body class="flex flex-col items-center">
  <header class="w-full text-center py-6 bg-indigo-700/40 backdrop-blur-lg shadow-lg">
    <h1 class="text-4xl font-extrabold tracking-tight">🌟 Lernol</h1>
    <p class="text-lg opacity-80">Interactive Learning for Everyone</p>
  </header>

  <!-- Onboarding -->
  <section id="onboarding" class="w-full max-w-md mt-10 card text-center">
    <h2 class="text-2xl font-bold mb-4">Welcome to Lernol!</h2>
    <p class="text-gray-200 mb-6">Let’s personalize your learning journey.</p>
    <label class="block mb-3">
      <span class="block mb-1 font-semibold">Your Age</span>
      <input id="user-age" type="number" class="w-full p-2 rounded-md text-black" placeholder="Enter your age">
    </label>
    <label class="block mb-3">
      <span class="block mb-1 font-semibold">Daily Goal (Minutes)</span>
      <input id="user-goal" type="number" class="w-full p-2 rounded-md text-black" placeholder="e.g. 20">
    </label>
    <label class="block mb-6">
      <span class="block mb-1 font-semibold">Main Interest</span>
      <select id="user-interest" class="w-full p-2 rounded-md text-black">
        <option value="">Select one</option>
        <option value="math">Math</option>
        <option value="science">Science</option>
        <option value="coding">Coding</option>
        <option value="languages">Languages</option>
        <option value="chess">Chess</option>
      </select>
    </label>
    <button id="start-btn">Start Learning</button>
  </section>

  <!-- Dashboard -->
  <section id="dashboard" class="hidden w-full max-w-5xl mt-10 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
    <div class="card text-center">
      <div class="text-6xl mb-3">🧮</div>
      <h3 class="text-xl font-bold mb-2">Math</h3>
      <p class="opacity-80 mb-4">Sharpen your logic and numbers.</p>
      <button onclick="startLesson('math')">Start</button>
    </div>

    <div class="card text-center">
      <div class="text-6xl mb-3">🔬</div>
      <h3 class="text-xl font-bold mb-2">Science</h3>
      <p class="opacity-80 mb-4">Explore the universe.</p>
      <button onclick="startLesson('science')">Start</button>
    </div>

    <div class="card text-center">
      <div class="text-6xl mb-3">💻</div>
      <h3 class="text-xl font-bold mb-2">Coding</h3>
      <p class="opacity-80 mb-4">Build the future with code.</p>
      <button onclick="startLesson('coding')">Start</button>
    </div>

    <div class="card text-center">
      <div class="text-6xl mb-3">🌍</div>
      <h3 class="text-xl font-bold mb-2">Languages</h3>
      <p class="opacity-80 mb-4">Speak, listen, and connect.</p>
      <button onclick="startLesson('languages')">Start</button>
    </div>

    <div class="card text-center">
      <div class="text-6xl mb-3">♟️</div>
      <h3 class="text-xl font-bold mb-2">Chess</h3>
      <p class="opacity-80 mb-4">Train your strategic mind.</p>
      <button onclick="startLesson('chess')">Start</button>
    </div>
  </section>

  <!-- Lesson View -->
  <section id="lesson-view" class="hidden w-full max-w-3xl mt-10 card text-center">
    <button onclick="showDashboard()" class="text-sm underline mb-4">&larr; Back</button>
    <h2 id="lesson-title" class="text-2xl font-bold mb-2"></h2>
    <p id="lesson-question" class="text-lg mb-4"></p>
    <div id="lesson-options" class="space-y-3 mb-4"></div>
    <div id="lesson-feedback" class="text-lg font-semibold mb-4 hidden"></div>
    <button id="next-btn" class="hidden">Next Question</button>
  </section>

  <footer class="mt-auto py-6 text-center text-sm opacity-70">
    &copy; 2025 Lernol. All Rights Reserved.
  </footer>

  <!-- JS -->
  <script src="lernol_frontend_v64.js"></script>
</body>
</html>
