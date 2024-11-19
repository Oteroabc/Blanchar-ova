<template>
    <div>
      <NavBar />
      <section class="quiz-container">
        <h1>Quiz: Introducción al Desarrollo Web</h1>
        <p>
          Responde las siguientes preguntas y pon a prueba tus conocimientos sobre desarrollo web.
        </p>
        
        <div v-for="(question, index) in questions" :key="index" class="question-card">
          <h3>{{ index + 1 }}. {{ question.text }}</h3>
          <div class="options">
            <label
              v-for="(option, i) in question.options"
              :key="i"
              :class="{'selected': selectedAnswers[index] === i}"
            >
              <input 
                type="radio" 
                :name="'question-' + index" 
                :value="i" 
                v-model="selectedAnswers[index]" 
              />
              {{ option }}
            </label>
          </div>
        </div>
  
        <div class="quiz-actions">
          <button class="check-btn" @click="checkAnswers">Verificar Respuestas</button>
          <button class="reset-btn" @click="resetQuiz">Reiniciar Quiz</button>
        </div>
  
        <div v-if="showResults" class="results">
          <h2>Resultados</h2>
          <p>
            Respondiste correctamente {{ correctAnswersCount }} de {{ questions.length }} preguntas.
          </p>
          <ul>
            <li 
              v-for="(question, index) in questions" 
              :key="'result-' + index"
              :class="{'correct': isCorrect(index), 'incorrect': !isCorrect(index)}"
            >
              {{ index + 1 }}. {{ question.text }} - 
              <span>
                {{ isCorrect(index) ? 'Correcta' : 'Incorrecta (Correcta: ' + question.options[question.correctOption] + ')' }}
              </span>
            </li>
          </ul>
        </div>
      </section>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  import NavBar from '~/components/NavBar.vue'
  
  const questions = [
    {
      text: '¿Qué define la estructura de un sitio web?',
      options: ['CSS', 'HTML', 'JavaScript', 'PHP'],
      correctOption: 1,
    },
    {
      text: '¿Qué lenguaje se utiliza para estilizar una página web?',
      options: ['HTML', 'Python', 'CSS', 'SQL'],
      correctOption: 2,
    },
    {
      text: '¿Qué permite JavaScript en una página web?',
      options: ['Estructurar contenido', 'Estilizar elementos', 'Añadir interactividad', 'Crear servidores'],
      correctOption: 2,
    },
    {
      text: '¿Qué es el diseño responsivo?',
      options: [
        'Diseño para dispositivos móviles',
        'Diseño que se adapta a diferentes tamaños de pantalla',
        'Diseño avanzado de bases de datos',
        'Diseño exclusivo para escritorio',
      ],
      correctOption: 1,
    },
    {
      text: '¿Cuál de estas herramientas es un editor de código?',
      options: ['VS Code', 'MySQL', 'Apache', 'GitHub'],
      correctOption: 0,
    },
    {
      text: '¿Qué es el frontend en el desarrollo web?',
      options: [
        'La lógica del servidor',
        'El diseño y la interacción visible por el usuario',
        'El almacenamiento de datos',
        'La configuración del dominio',
      ],
      correctOption: 1,
    },
    {
      text: '¿Qué es una práctica recomendada en desarrollo web?',
      options: [
        'Ignorar la accesibilidad',
        'Optimizar para dispositivos móviles',
        'Evitar usar frameworks',
        'No usar control de versiones',
      ],
      correctOption: 1,
    },
    {
      text: '¿Qué framework es popular para desarrollo frontend?',
      options: ['Vue.js', 'Django', 'Node.js', 'Laravel'],
      correctOption: 0,
    },
    {
      text: '¿Qué es Git?',
      options: [
        'Un lenguaje de programación',
        'Un sistema de control de versiones',
        'Un servidor web',
        'Una base de datos',
      ],
      correctOption: 1,
    },
    {
      text: '¿Qué significa "Full-stack"?',
      options: [
        'Diseño de bases de datos',
        'Especialista en frontend',
        'Especialista en backend',
        'Combinación de frontend y backend',
      ],
      correctOption: 3,
    },
  ]
  
  const selectedAnswers = ref(Array(questions.length).fill(null))
  const showResults = ref(false)
  const correctAnswersCount = ref(0)
  
  const checkAnswers = () => {
    correctAnswersCount.value = selectedAnswers.value.reduce(
      (count, answer, index) => count + (answer === questions[index].correctOption ? 1 : 0),
      0
    )
    showResults.value = true
  }
  
  const resetQuiz = () => {
    selectedAnswers.value = Array(questions.length).fill(null)
    showResults.value = false
    correctAnswersCount.value = 0
  }
  
  const isCorrect = (index) => selectedAnswers.value[index] === questions[index].correctOption
  </script>
  
  <style scoped>
  .quiz-container {
    padding: 20px;
    max-width: 800px;
    margin: auto;
    background: #f9f9f9;
    border: 1px solid #ddd;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  h1 {
    text-align: center;
    color: #6a11cb;
    margin-bottom: 20px;
  }
  
  .question-card {
    margin-bottom: 20px;
    background: #fff;
    border: 1px solid #ddd;
    border-radius: 5px;
    padding: 15px;
  }
  
  .options label {
    display: block;
    margin: 5px 0;
    cursor: pointer;
  }
  
  .options input {
    margin-right: 10px;
  }
  
  .quiz-actions {
    display: flex;
    justify-content: space-between;
    margin: 20px 0;
  }
  
  .check-btn {
    background-color: #6a11cb;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .reset-btn {
    background-color: #ff5252;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .results {
    margin-top: 20px;
    background: #fff;
    border: 1px solid #ddd;
    padding: 15px;
    border-radius: 5px;
  }
  
  .results ul {
    list-style: none;
    padding: 0;
  }
  
  .results li {
    margin-bottom: 10px;
  }
  
  .results li.correct {
    color: green;
  }
  
  .results li.incorrect {
    color: red;
  }
  </style>
  
  