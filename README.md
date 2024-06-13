# Prueba
Prueba.jsx-----------------------------------------------
import './App.css'
function Examen(props) {
    return (
        <div className="principal">
            <div className='caja2'>
                <img className="fotos22" src={props.imagen} />
            </div>
            <div className='caja3'>
                <h1>{props.titulo}</h1>
                <p>{props.parrafo}</p>
            </div>
            <div className='caja4'>
                <img className="fotos44" src={props.imagen2} />
            </div>
            <div className='tabla'>
                <table className="tablas">
                    <thead>
                        <tr>
                            <th>Header 1</th>
                            <th>Header 2</th>
                            <th>Header 3</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>Row 1, Cell 1</td>
                            <td>Row 1, Cell 2</td>
                            <td>Row 1, Cell 3</td>
                        </tr>
                        <tr>
                            <td>Row 2, Cell 1</td>
                            <td>Row 2, Cell 2</td>
                            <td>Row 2, Cell 3</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    );
}

export default Examen;


App.css--------------------------------------------------
.principal{
  display: flex;
  justify-content: space-between;
  padding: 20px;
  background-color: rgb(223, 172, 223);
  border-style: dotted;
  border-color: black;
}

.caja2{
  flex: 1;
  margin: 0 10px;
  padding: 20px;
  background-color: #71ddbd;
  border: 1px;
}

.caja3{
  flex: 1;
  margin: 0 10px;
  padding: 20px;
  background-color: #71ddbd;
  border: 1px;
  text-align: center;
}

.caja4{
  flex: 1;
  margin: 0 10px;
  padding: 20px;
  background-color: #71ddbd;
  border: 1px;
}

.fotos22{
  width: 200px;
  height: 200px;
}

.fotos44{
  width: 200px;
  height: 200px;
}

.tablas {
  width: 100%; 
  border-collapse: collapse;
  margin: 20px 0; 
}

.tablas th {
  border: 1px solid #ddd; 
  padding: 8px; 
  text-align: center; 
  background-color: #f4f4f4; 
  font-weight: bold;
}

.tablas td {
  border: 1px solid #ddd; 
  padding: 8px; 
  text-align: center; 
}


Index.jsx-------------------------------------------------------
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';
import Hola from './Saludo.jsx';
import Examen from './Prueba.jsx';
import reportWebVitals from './reportWebVitals';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <Examen imagen="danza1.png" titulo="HOLA" parrafo="este es un parrafo para el examen de programacion web 2" imagen2="danza3.png"></Examen>
    <Examen imagen="danza2.png" titulo="COLA" parrafo="este es un parrafo para el examen de programacion web 3" imagen2="danza1.png"></Examen>
    <Hola danza="BALLET" pais="BOLIVIA" academia="BOLIVIAMAR" imagen="danza1.png"></Hola>
    <Hola danza="CUECA" pais="ESPAÑA" academia="ESPCUE" imagen="danza2.png"></Hola>
    <Hola danza="CUMBIA" pais="COLOMBIA" academia="CUMCOLOM" imagen="danza3.png"></Hola>
  </React.StrictMode>
);

