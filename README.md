<! DOCTYPE html>
<html>
<cabeça>
  <title>Quadro de Tarefas Scrum</title>
 <estilo>
 corpo {
 família de fontes: Arial, sans-serif;
 cor de fundo: #f4f4f9;
 Cor: #333;
 margem: 0;
 preenchimento: 0;
 Display: Flex;
 flex-direção: coluna;
 altura: 100VH;
    }
 cabeçalho {
 Display: Flex;
 justify-content: espaço entre;
 alinhar itens: centro;
 cor de fundo: #4a90e2;
 cor: branco;
 preenchimento: 10px 20px;
    }
    .header-left {
 Display: Flex;
 alinhar itens: centro;
    }
    .header-left img {
 altura: 50px;
 margem direita: 10px;
    }
    .header-left h1 {
 margem: 0;
 tamanho da fonte: 24px;
    }
    .header-right {
 Display: Flex;
 alinhar itens: centro;
    }
    .header-right div {
 margem esquerda: 20px;
    }
 .header-right botão {
 cor de fundo: #fff;
 Cor: #4a90e2;
 borda: 1px sólido #4a90e2;
 raio da borda: 5px;
 preenchimento: 5px 10px;
 cursor: ponteiro;
    }
 .header-right botão:hover {
 cor de fundo: #e1e1e1;
    }
    .search-bar input {
 preenchimento: 5px;
 raio da borda: 5px;
 borda: 1px sólido #ddd;
    }
    .menu {
 Display: Flex;
 flex-direção: coluna;
 alinhar itens: flex-start;
 preenchimento: 10px;
 cor de fundo: #fff;
 borda direita: 1px sólido #ddd;
 Altura: Calc(100VH - 60px);
 largura: 200px;
    }
    .menu img {
 largura: 100px;
 margem inferior: 20px;
    }
 .item de menu {
 preenchimento: 10px;
      border-bottom: 1px solid #ddd;
      width: 100%;
    }
    .menu-item:last-child {
      border-bottom: none;
    }
    .menu-item:hover {
      background-color: #f4f4f4;
      cursor: pointer;
    }
    .content {
      display: flex;
      flex: 1;
      margin: 20px;
    }
    .column {
      flex: 1;
      margin: 10px;
      padding: 15px;
      border: 1px solid #ddd;
      border-radius: 8px;
      background-color: #fff;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    .column h2 {
      text-align: center;
      color: #4a90e2;
      border-bottom: 2px solid #4a90e2;
      padding-bottom: 10px;
      margin-bottom: 20px;
    }
    .task {
      margin-bottom: 15px;
      padding: 10px;
      border: 1px solid #e1e1e1;
      border-radius: 5px;
      background-color: #f9f9f9;
      box-shadow: 0 1px 3px rgba(0,0,0,0.1);
    }
    .task-buttons {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 10px;
    }
    .task-buttons button {
      background-color: #4a90e2;
      color: white;
      border: none;
      padding: 5px 10px;
      border-radius: 5px;
      cursor: pointer;
      font-size: 14px;
    }
    .task-buttons button:hover {
      background-color: #357abd;
    }
    .task-buttons input {
      border: 1px solid #ddd;
      padding: 5px;
      border-radius: 5px;
      font-size: 14px;
    }
    .timer {
      margin-left: 10px;
      font-weight: bold;
    }
    .task-info {
      margin-top: 10px;
      font-size: 14px;
      color: #666;
    }
    #backlog-input {
      width: calc(100% - 110px);
      padding: 10px;
      border-radius: 5px;
      border: 1px solid #ddd;
    }
    #add-backlog {
      padding: 10px 15px;
      border-radius: 5px;
      border: none;
      background-color: #4a90e2;
      color: white;
      cursor: pointer;
      font-size: 14px;
    }
    #add-backlog:hover {
      background-color: #357abd;
    }
    ul {
      list-style: none;
      padding: 0;
    }
    li {
      padding: 10px;
      border-bottom: 1px solid #e1e1e1;
    }
  </style>
</head>
<body>
  <header>
    <div class="header-left">
      <img src="botar.o.pikachu.png" alt="Logo"> 
      <h1>Scrum Master Pokemons</h1>
    </div>
    <div class="header-right">
      <button>Sobre</button>
      <button>Suporte</button> 

	<button id="suporteBtn">Suporte</button>

<div id="suporteModal" class="modal">
    <div class="modal-content">
        <span class="close">×</span>
        <h2>Suporte do Site</h2>
        <ul>

	    <li><a href="#faq">FAQ</a></li>
            <li><a href="#contato">Contato</a></li>
            <li><a href="#chat">Chat</a></li>
        </ul>
    </div>
</div>


.modal {
    display: none;
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgb(0,0,0);
    background-color: rgba(0,0,0,0.4);
}

.modal-content {
    background-color: #fefefe;
    margin: 15% auto;
    padding: 20px;
    border: 1px solid #888;
    width: 80%;
    max-width: 500px;
    text-align: center;
}

.close {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
}

.close:hover,
.close:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
} 

// Get the modal
var modal = document.getElementById("suporteModal");

// Get the button that opens the modal
var btn = document.getElementById("suporteBtn");

// Get the <span> element that closes the modal
var span = document.getElementsByClassName("close")[0];

// When the user clicks the button, open the modal 
btn.onclick = function() {
    modal.style.display = "block";
}

// When the user clicks on <span> (x), close the modal
span.onclick = function() {
    modal.style.display = "none";
}

// When the user clicks anywhere outside of the modal, close it
window.onclick = function(event) {
    if (event.target == modal) {
        modal.style.display = "none";
    }
}

      <button>Iniciar Sessão</button>
      <button>Idioma</button>
      <div class="search-bar">
        <input type="text" placeholder="Pesquisar...">
      </div>
    </div>
  </header>
  <div class="content">
    <nav class="menu">
      <img src="imagens/cachau.png" alt="Menu Image"> 
      <div class="menu-item">Importante</div>
      <div class="menu-item">Atribuído a Mim</div>
      <div class="menu-item">Tarefas</div>
      <div class="menu-item">Planejamentos</div>
      <div class="menu-item">Salvos</div>
      <div class="menu-item">Simulação</div>
      <div class="menu-item">Biblioteca</div>
    </nav>
    <div class="column">
      <h2>Backlog</h2>
      <input type="text" id="backlog-input" placeholder="Nova Tarefa" />
      <button id="add-backlog">Adicionar</button>
      <ul id="backlog-list"></ul>
    </div>
    <div class="column">
      <h2>Em Progresso</h2>
      <ul id="in-progress-list"></ul>
    </div>
    <div class="column">
      <h2>Concluído</h2>
      <ul id="completed-list"></ul>
    </div>
  </div>

  <script>
    let backlogTasks = [];
    let inProgressTasks = [];
    let completedTasks = [];

    document.getElementById("add-backlog").addEventListener("click", () => {
      let taskText = document.getElementById("backlog-input").value;
      if (taskText) {
        let task = {
          text: taskText,
          assignee: "",
          timer: null,
          elapsedTime: 0
        };
        backlogTasks.push(task);
        document.getElementById("backlog-input").value = "";
        updateList("backlog-list", backlogTasks, "backlog");
      }
    });

    function updateList(listId, tasks, type) {
      let list = document.getElementById(listId);
      list.innerHTML = "";
      tasks.forEach((task, index) => {
        let listItem = document.createElement("li");
        listItem.className = "task";
        listItem.innerHTML = `
          ${task.text}
          <div class="task-buttons">
            ${type === "backlog" ? `<button onclick="moveToInProgress(${index})">Atribuir</button>` : ""}
            ${type === "inProgress" ? `
              <input type="text" placeholder="Responsável" onchange="updateAssignee(${index}, this.value)" />
              <button onclick="startTimer(${index})">Iniciar Timer</button>
              <span class="timer" id="timer-${index}">${task.elapsedTime}s</span>
              <button onclick="moveToCompleted(${index})">Finalizar</button>
            ` : ""}
          </div>
          ${type === "completed" ? `
            <div class="task-info">
              Tempo Total: ${task.elapsedTime}s<br />
              Responsável: ${task.assignee}
            </div>
          ` : ""}
        `;
        list.appendChild(listItem);
      });
    }

    function moveToInProgress(index) {
      let task = backlogTasks.splice(index, 1)[0];
      inProgressTasks.push(task);
      updateList("backlog-list", backlogTasks, "backlog");
      updateList("in-progress-list", inProgressTasks, "inProgress");
    }

    function moveToCompleted(index) {
 let tarefa = inProgressTasks.splice(índice, 1)[0];
 completedTasks.push(tarefa);
 updateList("lista-em-andamento", emProgressTasks, "inProgress");
 updateList("lista concluída", completedTasks, "concluído");
    }

    function updateAssignee(index, assignee) {
 inProgressTasks[índice].assignee = assignee;
 updateList("lista-em-andamento", emProgressTasks, "inProgress");
    }

 function startTimer(índice) {
 let tarefa = inProgressTasks[índice];
 if (task.timer) retornar;
      task.timer = setInterval(() => {
        task.elapsedTime++;
 document.getElementById('timer-${index}').innerText = '${task.elapsedTime}s';
      }, 1000);
    }
  </script>
</corpo>
</html>
