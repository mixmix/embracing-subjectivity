# embracing subjectivity

mix

`@ye+QM09iPcDJD6YvQYjoQc7sLF/IFhmNbEqgdzQo3lQ=.ed25519`

---
## truth

???

this is a story about truth
- how truth is made, who gets to make it
- how truth changes society 
- how code shapes truth

---
## truth grows/ is constructed

???

is built / synthesised

- it is memory / record
- how it's told /interpretted

Let's keep an eye on
- who keeps the record
- does the interpretting

---
## emergent truth

![campfire](http://www.twistednether.net/wp-content/uploads/2009/10/campfire1.jpg)

???

- stories
- grown
- subjective perspectives + social graphs -> inter-subjective 
- cohesions > complexity
- bottom up

---
## objective Truth

![moses](http://4.bp.blogspot.com/-IQcM8lFtQMA/UQX0JJZDt5I/AAAAAAAAFnY/lXrrjh2bag8/s1600/moses_breaking-tablets.jpg)

???

- calcified emergent truth? bold leader?
- Plato + objectivity
- trancendental, axiomatic
- capital T truth
- top down

---
## objective Truth - benefits

![civ3](http://www.civfanatics.com/images/civ3/tech%20tree/c3c_ancient.jpg)

???

- CIV > larger scale coordinations (nation-state, religions)

---
## objective Truth - benefits

![tenochtitlan](https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fquintessentialruminations.files.wordpress.com%2F2012%2F05%2Ftenochtitlan11.jpg&f=1)

???

- administration
  - identity (tax, passport)
  - authorisation (passport, drivers license)
  - auditable

---
## objective Truth - dangers

![massacring protestants](https://upload.wikimedia.org/wikipedia/commons/5/52/Francois_Dubois_001.jpg)

???

- brittleness (aztecs)

who is keeping the records, and why
  - revolt (french)
  - abuse and lies
who is interpretting the truth

---
## truth in code

```js
return knex.schema.createTable('users', function (table) {
  table.string('userName')
  table.string('email')
  table.string('password')
  table.boolean('gender')
})
```

???

- code lends itself to objective truth
- a lot of administrative sotware:
  - identities
  - transactions

- social media (hybrid)
  - companies rolling objective systems, directly capturing emergent value 
    - content
    - relational + reputational data
  - record-keeping and presentation is administered privately

---
## less objective code

build something where : 
  - anyone can speak (write)
  - anyone can interpret

???

- challenge
- i.e. a system that enable emergent inter-subjective truth
- build twitter without a central database 
- ADVENTURE YARRR
  - PATCHWORK

---

### Scuttlebutt ahoy!

???

spoilers:
 - it's written and running
 - it's generating, subjective truth 

flash patchwork

---

**scut•tle•butt (skŭtˈl-bŭtˌ)**

1. n. Slang Gossip; rumor.
2. n. _Nautical_ A drinking fountain on a ship.
3. n. _Nautical_ A cask on a ship used to hold the day's supply of drinking water.

---
## scuttlebutt 

```js
var message = {
  author: '@mixmix',
  content: {
    type: 'post',
    text: 'greetings hello nz.js'
  },
  timestamp: 1488613256922
}
```

???

- can share
- with no server how would I fetch this message:
  - timestamp?
  - timestamp + author?

---
## content addressable storage

```js
var message = {
  author: '@mixmix',
  content: {
    type: 'post',
    text: 'greetings hello nz.js'
  },
  timestamp: 1488613256922
}

var messageId = hash(message)
// => emva3qXR6+XtLKwxWIsVB/hO1i5PmV9v2AP5hjRNDKQ
```
hash function produces a unique, verifiable 'finger-print' of our message.

???

- you've seen with git commit ids

---
## identity through encryption

```js
var message = {
  author: '@ye+QM09iPcDJD6YvQYjoQc7sLF/IFhmNbEqgdzQo3lQ=.ed25519',
  content: {
    type: 'post',
    text: 'greetings hello nz.js'
  },
  timestamp: 1488613256922
}

var signedMessage = sign(message, privateKey)
```

we use a public/ private key-pair for our id and signing

---
## identity through encryption

```js
var message = {
  author: '@ye+QM09iPcDJD6YvQYjoQc7sLF/IFhmNbEqgdzQo3lQ=.ed25519',
  content: {
    type: 'post',
    text: 'greetings hello nz.js'
  },
  timestamp: 1488613256922
}

var signedMessage = sign(message, privateKey)
```

```js
// signedMessage
{
  author: '@ye+QM09iPcDJD6YvQYjoQc7sLF/IFhmNbEqgdzQo3lQ=.ed25519',
  content: {
    type: 'post',
    text: 'greetings hello nz.js'
  },
  timestamp: 1488613256922,
  signature: 'IBJXJC+DrwuX9iDwPUIJlSHs7BfENtx4D5fkCCT/+M42qhd6bHwQ==.sig.ed25519'
}
```

---
## identity

```js
{
  author: "@azsQJqrOazV1/VC2hF5rSylaN4A1lTXPIuer+PdCQ3M=.ed25519",
  timestamp: 1487904949711,
  content: {
    type: "about",
    about: "@azsQJqrOazV1/VC2hF5rSylaN4A1lTXPIuer+PdCQ3M=.ed25519",
    name: "juliana",
    image: {
      link: "&qgNK+27gf4Rquyh4T7w7wDU0HiUayS+y+1sDlNfI/2g=.sha256",
      size: 452153,
      type: "image/png",
      width: 512,
      height: 512
    }
  },
  signature: "ce+JOzOxNdCj7Vkdlgmpd+yKbw4qMpIZLm/54FJdGCMleGOS...."
}
```
an _about_ message


???

thoughts from watching video: 

- fireside > music, fiction, startups, meaning
- objective truth > uniform bean counting
  - more emphasis on the power and good of this
- objective top down systems slurping up the music, the magic of the data inbetween

- new zealand context for different truths? putting up flags = land ownership?

going back to the norm-web:
  - platforms asking me to prove who I am
  - logins ... so top-down ... it's border control (papers please)
  - comic sans accessability
  - kiwibank interface ... why can't I re-present my own data






