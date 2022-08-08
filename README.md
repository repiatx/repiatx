### Hi there 👋
🔭 I’m currently working on Helorobo


My code Speaks for itself 😊

```typescript

const backend_skills = [
    'Node.js',
    'Javascript',
    'Typescript',
    'Express',
    'Fastify'
    'REST-API',
    'Docker',
    'Socket.io',
    'TCP/IP',
    'NGINX',
    'RabbitMQ',
    'Mongoose'
    'Kafka',
    'Redis(Pub/Sub,Stream)',
]

const mobile_skills = [
    'Flutter'
]

const frontend_skills = [
    'HTML',
    'Javascript',
    'Vue.js',
    'Bootstrap',
    'Vuex',
]

const database_skills = [
    'MongoDB',
    'PostgreSQL',
    'MySQL',
    'MSSQL'
]

const game_development_skills = [
    '2D Unity C#',
    'DragonBones', // 2D Animation !! Mesh Animation
    'TexturePacker',
    'Level Design',
    'Has various game concept'
]

const other_skills = [
    'Figma',
    'Illustrator',
    'Photoshop',
    '3DS Max', // Old... Very old
    'Premiere Pro',
    'Prezzi',
    'Good Communication',
    'Always Smiley Face' // 😊
]



const human: Human = new Human({
    fullname: 'Hayrettin GÖK',
    email: 'hayrettingk46@gmail.com',
    phone: '', //Secret for now 😊
    languages: [
        new Language({name:'Turkish',level:LanguageLevel.Native}),
        new Language({name:'English',level:LanguageLevel.Advanced}),
        new Language({name:'Japanase',level:LanguageLevel.Beginner}) // Hobby Level
    ],
    hobbies:[
        'Reading Book',
        'Swimming',
        'Playing Games' //Espacially online competitive games
    ]

})

const worker: Worker = new Worker({
    expected_salary: 4000 // $$$ ofc 😊
    available_work_types: [WorkType.Remote,WorkType.Office,WorkType,Hybird] // I prefer more salary if you want me in the office 😊
    skills: [
        ...backend_skills,
        ...mobile_skills,
        ...frontend_skills,
        ...database_skills,
        ...game_development_skills,
        ...other_skills
    ]
},human)


class Worker extends Human implements IHireable, IContactable {

    skills: List<string>
    expected_salary: number
    available_work_types: List<WorkType>
    linked_in: string

    constructor({
            skills: List<string>,
            expected_salary: number,
            available_work_types: List<WorkType>,
            linked_in: string
        },
        humanity: Human
    )
    {
        super(humanity)
    }

    function hire({salary: number, work_type: WorkType}){

        if(salary < this.expected_salary){
            throw new Error(`I'm not that cheap :) `)
        }

        if( ! available_work_types.includes(work_type) ){
            throw new Error(`Guess we are not on the same ship. :) `)
        }

        contact()
        

    }
    function contact(){
        // go to LinkedIn URL
    }

}

class Human {
    fullname: string
    email: string
    phone: string
    languages: List<Language> = []
    hobbies: List<string> = []

    constructor({
        fullname: string,
        email: string,
        phone: string,
        languages: List<Language>,
        hobbies: List<string>
        })
    {
        this.fullname = fullname
        this.email = email
        this.phone = phone
        this.languages = languages
        this.hobbies = hobbies
    }

    async function eat(){}

    function sleep(){}

    async function code(){}

}

class Language {
    name: string
    level: LanguageLevel
    constructor({name: string,level: LanguageLevel}){
        this.name = name
        this.level = level
    }
}

interface IHireable {
    hire({salary: number, work_type: WorkType}): void
}

interface IContactable {
    contact(): void
}

Enum LanguageLevel {
    Starter,
    Beginner,
    Intermediate,
    Advanced,
    Native
}

Enum WorkType {
    Remote = 'remote',
    Hybird = 'hybird',
    Office = 'office',
    Freelance = 'freelance'
}

```
