# embracing subjectivity

mix

`@ye+QM09iPcDJD6YvQYjoQc7sLF/IFhmNbEqgdzQo3lQ=.ed25519`

???
A journey:
  - web imagined differently
    - MAKE THIS STRONGER
    - quantitative vs qualitative language
    - institutionally legible
    - issues on git repos, issues on people

setup check: 
  - display settings
  - sbot
  - patchbay
  - graph-viz:
    - server
    - chrome tab ready to load
  - git ssb web
    - repo loaded


---
## truth & code

???
- this is a story about truth
  - what is truth,
  - where does it come from 
  - who gets to make it

- a record of who or what is significant

---
## code as Truth

```js
var user = {
  userName: 'mixmix',
  email: 'mix@enspiral.com',
  password: 'IQcM8lFtQMA/UQX0JJZDt5I/',
  gender: 'male'
}
```

---
## code as Truth

```js
return knex.schema.createTable('users', function (table) {
  table.string('userName')
  table.string('email')
  table.string('password')
  table.boolean('gender')
})
```

???
- opinionated format
  - unique identifiers - last name 
- rules
- necessary simplifications to form coherent
- code lends itself to record keeping

---
## Truth for admin

![tenochtitlan](https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fquintessentialruminations.files.wordpress.com%2F2012%2F05%2Ftenochtitlan11.jpg&f=1)

???
- been going on a while
- civilisation takes admin
  - recording important things 

---
## Truth - transactions

![barley transaction](http://memory.loc.gov/service/amed/amcune/cf0032/0001ob.jpg)

???
- sumerians trading grains 5000 years ago
- taxes 
- identity?
- offline-first immutable log

---
## Truth - identity

![passport](https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.passport-photos-derby.co.uk%2Fimages%2Famerican-visa-photos.jpg&f=1)

???
- managing movement (have you paid your taxes)
- safe passage agreements
- notice my name is different according to the government

---
## Truth - rules

![moses](http://4.bp.blogspot.com/-IQcM8lFtQMA/UQX0JJZDt5I/AAAAAAAAFnY/lXrrjh2bag8/s1600/moses_breaking-tablets.jpg)


???
- great for easy coherence,
  - coordination tax
  - societal protocols
  - research aquaducts

---
## T is for Top-down

![moses](http://4.bp.blogspot.com/-IQcM8lFtQMA/UQX0JJZDt5I/AAAAAAAAFnY/lXrrjh2bag8/s1600/moses_breaking-tablets.jpg)
![passport](https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.passport-photos-derby.co.uk%2Fimages%2Famerican-visa-photos.jpg&f=1)
![barley transaction](http://memory.loc.gov/service/amed/amcune/cf0032/0001ob.jpg)

 _objectively True_

???
- objectivity
  - an idea Plato rolled out
  - Truth can exist outside of the subject, is trancendental, absolute

- (benefit)
  - great for coordination
  - clean, tidy, safe 
- (downside)
  - identity (passport mix / john)
  - gender (stats)

---
## Truth - problems

![massacring protestants](https://upload.wikimedia.org/wikipedia/commons/5/52/Francois_Dubois_001.jpg)

???
- (downside) can be over-applied + abused
  - I need to be rich, I'm gods rep on earth
- this is the french revolution against Monarchy
  - actually it's just a bunch of christians lynching some protestants
- ideology

---
## another kind of truth

![campfire](http://www.twistednether.net/wp-content/uploads/2009/10/campfire1.jpg)

???
- other important things to remember / record
  - stories
  - songs, music
  - recipes
  - relationships
  - useful lessons (kumara don't grow well in the south island)
- subjective perspectives + social graphs -> inter-subjective 
  - emergent
  - flexible
  - highly fertile (compared to accounting)

---
## emergent truth aggregators

![](https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.techandlife.com%2Fwp-content%2Fuploads%2F2009%2F09%2FFirst-Reddit-post2-ellipse.jpg&f=1)

???
skip?
- Reddit
- LinkeIn, Facebook

- hybrids: objective systems closing over emergent truth
  - efficiency of objective system
  - richness of emergent system
    - relational data (trust)
  - problems of the objective system 

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

flash patchbay

---

**scut•tle•butt (skŭtˈl-bŭtˌ)**

1. n. Slang Gossip; rumor.
2. n. _Nautical_ A drinking fountain on a ship.
3. n. _Nautical_ A cask on a ship used to hold the day's supply of drinking water.

???
- like stories, messages are gossiped
- remember the stories I've heard locally 

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
- plain ol' author names aren't that unique / verifiable

---
## public-private key tech

![](https://upload.wikimedia.org/wikipedia/commons/0/0c/Cylinder_seal_Shamash_Louvre_AO9132.jpg)

???
- mesopotamians
- private part 
  - related to the public part
  - hard to guess / make
- sign things with the private part
- people can compare with copies of your public key
- hanko!  https://images.duckduckgo.com/iu/?u=http%3A%2F%2F1.bp.blogspot.com%2F_xEZ4gcVkeIY%2FTCN3uJGn0GI%2FAAAAAAAABAk%2F9OHlcyQDUBA%2Fs1600%2FHanko.jpg&f=1

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
an  _about_  message

???
- patchbay
  - show @juliana
  - rename juliana
  - show mikey + opions

- this is a fireside story
  - plurality of opinions
  - emergent truth

---
## re-presention of truth

![patchwork-next](https://github.com/mmckegg/patchwork-next/raw/master/screenshot.jpg)

???
- how a story is told vs. recorded
  - social media reserves pretty much all of the rights
- patchbay (more dev-centric)
- patchwork (more social view of the data)
  - this interface has different opinions about how truth should emerge from subjective statements

---
## git on scuttlebutt

![dnsssb](https://www.scuttlebutt.nz/assets/git-ssb-repo.png)

???
- code is just messages
- github as a fire-side story (I don't have to hang out with a company)

---
## music on scuttlebutt

![ferment](ferment.png)

???
- anger driven development
  - creating music, paying for a service that is getting in the way
- ssb for discovery and messaging
- webtorrent for sharing music

---
## there & back again

???
- reverse culture shock

---
## border control

![logins](username_taken.png)

???

- username taken
  - proving identity at the border (papers please)
  - passport
  - why can't I just speak and the truth will emerge?

---
## top-down UI 

![kiwibank](kiwibank.png) 

???
- re-presenting data 
  - why can't I re-present my own data
- comic sans: article about accessibility of fonts

---
## connectivity 

![](island_replication.jpeg)

???
- is the internet down?
- island replication
  - islands
  - ships
  - space

- instant git-ssb
- instant search

---
## problems with current tech

- advertising
  - push-based
- access to your feed
- shaping your re-presentation

- global singletons

---
## embrace subjectivity

![sailing into the west](http://68.media.tumblr.com/23858ef00a47e7ee1255c1865ee2a319/tumblr_nd6hiqXZAy1sns9vwo1_1280.jpg)

???
It's just my opinion, but I'm investing in a more subjective web

