Terminal : 
npm create vite@5.3.10;
npm i react-icons@5.3.0;

Step 2 
cd react-app
npm i

to open vsCode :' code . '
=================
Create comonent of styles:
npm install styled-components 


const [array, setArray] = useState(['happy', 'wonderful']);
const changeArray = () => {
   setArray(array.filter(tag => tag !== 'wonderful' )) remove

   setArray(array.map(tag => tag === 'wonderful' ? 'fun' : tag))
}

To change useState array and to remove tag

When we have object like in useState() exercise :
   const [bags, setBags] = useState([
     {}
   ])
