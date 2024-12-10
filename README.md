Dependencies JSON:
"dependencies": {
    "@chakra-ui/react": "^2.5.1",
    "@emotion/react": "^11.10.6",
    "@emotion/styled": "^11.10.6",
    "framer-motion": "^10.0.1",
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-icons": "^5.4.0"
  }

Terminal : 
npm create vite@4.1.0;
npm i react-icons@5.3.0;
npm i zod@3.20.6 -> we need zod to hold old errors at one place
npm i @hookform/resolvers@2.9.11
npm install @chakra-ui/react@3.0.0 


info: useForm, zod, httpSercise
    const ref = useRef<HTMLInputElement>(null) => That how ref created

    const EmojiMap: {[key: number]: ImageProps} =  {   {[key: number]: ImageProps} => index Singeture import to add becouse if not error come out
        3: {src: mehImg, alt: 'meh'},
        4: {src: thumbImg, alt: 'thumb'},
        5: {src: bullsEye, alt: 'bullish Eye'}
    }

export interface gameQuery {
  genresList: genresList | null,
  Platform: Platform | null
  selectore: string
  searchText: string
}                                                                  GameQuery Help to contain all Props in one plase and easly import one of those Props to other folder 

function App() {

// Crate useState where all our date will be safed
const [gameQuery, setGameQuery] = useState<gameQuery>({} as gameQuery)




    
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


import apiClient from "./api-client";

export interface Entity {
    id: number
}

class httpService {

    endPoint: string

    constructor(endPoint: string) {
        this.endPoint = endPoint
    }

    addAll<T>() {
        const controler = new AbortController
        const request = apiClient.get<T>(this.endPoint, {signal: controler.signal})
        return{request, cencel: () => controler.abort()}
    }
    create<T>(entity: T) {
        return apiClient.post(this.endPoint , entity)
    }
    delete(id: number) {
        return apiClient.delete(this.endPoint + '/' + id)
    }
    update<T extends Entity>(entity: T) {
        return apiClient.patch('/todos/' + entity.id, entity)
    }
}

const create = (endPoint: string) => new httpService(endPoint)
export default create


import create from "./http-service";

export interface ToDoList {
    userId: number;
    id: number;
    title: string;
    completed: boolean;
  }

  export interface toDoProp {
    title: string 
  }

export default create('/todos')
We can reset our value use reset() at useForm()

When we want to change size of pictures manualy we can use media/crop/size/size


To Sort we can use this object : 
  const sortOrder = [
        { value: "", label: "Relevance" },
        { value: "-added", label: "Date added" },
        { value: "name", label: "Name" },
        { value: "-released", label: "Release date" },
        { value: "-metacritic", label: "Popularity" },
        { value: "-rating", label: "Average rating" },
    ]



