<h1> Creando el sorteo de amigos</h1>
-Estado del sorteo: TERMINADO






// El principal objetivo de este desafío es fortalecer tus habilidades en lógica de programación. Aquí deberás desarrollar la lógica para resolver el problema.
let nombreDeAmigos = []

function agregarAmigo() {
    let input = document.getElementById("amigo");
    let nombre = input.value
    if(nombre == "") {
        alert("Por favor, inserte un nombre");
        return;
    }
    nombreDeAmigos.push(nombre)
    console.log(nombreDeAmigos)
    mostrarAmigos()
    input.value = "";
}


function mostrarAmigos() {
    let lista = document.getElementById ("listaAmigos");
    lista.innerHTML = ""
    for (let i = 0; i < nombreDeAmigos.length; i++) {
        lista.innerHTML += `<li>${nombreDeAmigos[i]}</li>`;

    }
}

function sortearAmigos() {
    if(nombreDeAmigos.length === 0)
    alert("No hay amigos para sortear")
    return;

    let indiceAleatorio = Math.floor(Math.random()* nombreDeAmigos.length);
    let amigoSorteado = nombreDeAmigos[indiceAleatorio];   

    document.getElementById("resultado").innerHTML = `<li>${amigoSorteado}</li>`;
}
