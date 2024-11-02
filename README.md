Terminal : 
npm create vite@5.3.10;
npm i react-icons@5.3.0;
npm i zod@3.20.6 -> we need zod to hold old errors at one place
npm i @hookform/resolvers@2.9.11


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


   type typeForm = z.infer<typeof schema>

useForm: 
register to handle text | number ; formState to acces errors
const {
  register, 
  handleSubmit, 
  formState: { errors , isValid }} = useForm<typeDate>({resolver: zodResolver(schema)});

in that case when we use z and we have input as nubmer but with "register" this turn to string we can use 
'{...register('age', {valueAsNumber: true})}'
