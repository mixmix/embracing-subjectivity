# embracing subjectivity

mix

`@ye+QM09iPcDJD6YvQYjoQc7sLF/IFhmNbEqgdzQo3lQ=.ed25519`

???
## CHECKLIST

- display
- servers
  - views enlarged
  - patchbay
  - git ssb

## what is this talk about?

- understanding the web today
- an experiment + a journey
- a new hope
- some useful primitives for decent tech

---
## organising civilisation

![tenochtitlan](https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fquintessentialruminations.files.wordpress.com%2F2012%2F05%2Ftenochtitlan11.jpg&f=1)

???
## how did humans get where we got?


- recording things that matter

## basically, admin

---
## transactions

![barley transaction](http://memory.loc.gov/service/amed/amcune/cf0032/0001ob.jpg)

???
## how long?

A clay tablet
- sumerians trading grains 5000 years ago
- table

---
## some tax documentation

![rosetta](https://upload.wikimedia.org/wikipedia/commons/2/23/Rosetta_Stone.JPG)

???
## Rosetta stone

tax edict from 2000 year ago

---
## military org

![mainframe](http://bitsavers.trailing-edge.com/pdf/univac/1100/photos/1106.jpg)

???
## NATO 

- 45 years ago
- supply logistics + payroll

## amazon

---
## identity

![passport](passport.jpg)

???
## to what degree is defintion of identity linked to instutions?

- checking taxes
- communicating with other orgs 
  - kingdoms backing safe passage 
  - we'll revist this

## notice the imperfections

- name
- gender

## why is this passport the way it is?

---
## institutional legibility

![name change](institutional_legibility.png)
![name change passport](institutional_legibility_passport.png)

???
- name change: 9 pages + supplementary
- passport name change: 12 pages + supplementary

---
## institutional legibility

![name change passport](institutional_legibility_passport_closeup.png)

???
## photo job > no-one looks good (inaccurate rep)

## what's wrong with this?

- homogeneous
- legible (but not human)

---
## opinions baked in

```js
return knex.schema.createTable('users', function (table) {
  table.string('userName')
  table.string('email')
  table.string('password')
  table.boolean('gender')
})
```

???
## code plays an important part of trend

- records
- rules

## what's wrong with opinions?

- opinions are great
  - cohesion
  - learning
  - great things 

- code enables even more more of the same
  - some table
  - plus built in rules + logic
  - extends

---
## plato

![plato](http://3.bp.blogspot.com/-4tLynuYBkhQ/TqcL1B3lDVI/AAAAAAAAAB0/DqucJFRCgxo/s1600/Plato.jpg)

???
## I blame this guy

## objectivity

- holy wars
- medicine

---
## objective truth

![moses](http://4.bp.blogspot.com/-IQcM8lFtQMA/UQX0JJZDt5I/AAAAAAAAFnY/lXrrjh2bag8/s1600/moses_breaking-tablets.jpg)

???
## trancendental truth

- truth that is above or exists independtly

## opinions >>> objective truths

- handed down from on high

## this is how stuff is

---
## this is you

![passport](passport.jpg)

???
## easy to mistake this document (and it's opinions) for the truth

.

## this is a trivial example

how do you feel about administrative opinions about your:
- gender
- friendships
- loyalty to state
- religion
- health
- race

---
## the good word

![massacring protestants](https://upload.wikimedia.org/wikipedia/commons/5/52/Francois_Dubois_001.jpg)

???
## an error in reading or writing a text

- objective truth going bad

## what's the alternative?

---
## an alternative

![campfire](http://www.twistednether.net/wp-content/uploads/2009/10/campfire1.jpg)

???

## recording + re-presentating info (millenia)

- stories
- recipes
- music 

---
## inter-subjective truths

![campfire](http://www.twistednether.net/wp-content/uploads/2009/10/campfire1.jpg)

???


## how is truth stored and re-presented here?
  - a bunch of assertions
  - a lens for interpretation

## what if we could code like this ? 
  - no singular ledger, no prescriptive fields
  - a plurality of ledgers and a plurality of interpretation 

## doesn't sound institutionally legible

---
## build a subjective twitter

a system where: 
  - anyone can speak
  - anyone can interpret the world

???
## read / write / presentation

---
## built!

???
spoilers:
 - it's written and running
 - it's generating, subjective truth 

flash patchbay

---
## scut•tle•butt (skŭtˈl-bŭtˌ)

1. n. Slang Gossip; rumor.
2. n. _Nautical_ A drinking fountain on a ship.
3. n. _Nautical_ A cask on a ship used to hold the day's supply of drinking water.

???
- like stories, messages are gossiped
- remember the stories I've heard locally 

---
## important decent primitives

- content addressable storage
- public/ private keys

---
## content addressable storage

![git commit](git_commit_hash.png)

???

you've seen these already

---
## content addressable storage

![file](https://images.duckduckgo.com/iu/?u=http%3A%2F%2F3.bp.blogspot.com%2F-sY7whMXT83o%2FUECGK-oSdeI%2FAAAAAAAAABM%2F-OXkkmppfvE%2Fs1600%2Ftext-file-icon.png&f=1)
![fingerprint](https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fthesalesblog.com%2Fwp-content%2Fuploads%2F2010%2F03%2FFingerprint.jpg&f=1)

```js
hash(file) // => 63ef70b672446094009382b92008feb9b909d443
```

???


## verify right data

## OR requests the exact data

## fingerprints > used to find people

---
## public-private keys - signing

![hanko stamped doc](https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fmedia-cache-ec0.pinimg.com%2F736x%2Fd2%2Fd6%2F5d%2Fd2d65d783a02f8e865e07070d3befa05.jpg&f=1)
![hanko stamp](https://images.duckduckgo.com/iu/?u=http%3A%2F%2F1.bp.blogspot.com%2F_xEZ4gcVkeIY%2FTCN3uJGn0GI%2FAAAAAAAABAk%2F9OHlcyQDUBA%2Fs1600%2FHanko.jpg&f=1)

???
## mesopatamians 3000 years ago

## public part - everyone knows (like your name)

## private part - only you have (it's for signing)

---
## public-private keys - encryption

![encryption diagram](https://images.duckduckgo.com/iu/?u=http%3A%2F%2F4.bp.blogspot.com%2F-z-acQ-nDXqU%2FTxku_0Q3TvI%2FAAAAAAAAAKM%2FuVrkIgSLYjs%2Fs1600%2Fpke.gif&f=1)

???
## public part encrypts (hides content)
## private part decrypts (retrieves content)

probably should improve diagram

---
## message

```js
var message = {
  author: '@mixmix',
  content: {
    type: 'post',
    text: 'hope you are enjoying nz.js so far'
  },
  timestamp: 1488613256922
}
```

---
## message - author

```js
var message = {
  author: '@ye+QM09iPcDJD6YvQYjoQc7sLF/IFhmNbEqgdzQo3lQ=.ed25519',
  content: {
    type: 'post',
    text: 'hope you are enjoying nz.js so far'
  },
  timestamp: 1488613256922
}

```

You use your public key as your identity

???
## note author (me) is my public key

---
## message - signing

```js
var message = {
  author: '@ye+QM09iPcDJD6YvQYjoQc7sLF/IFhmNbEqgdzQo3lQ=.ed25519',
  content: {
    type: 'post',
    text: 'hope you are enjoying nz.js so far'
  },
  timestamp: 1488613256922
}

var signedMessage = sign(message, privateKey)
```

You use your private key to sign the message

???
## by include my public key in what is signed

- know who it's from
- can verify signature

---
## message - signed 

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
  signature: 'IBJXJC+DrwuX9iDwPUIJlSHs7BfENtx4D5fkCCT/+M42qhd6....==.sig.ed25519'
}
```

---
## content addressable storage

```js
{
  author: '@ye+QM09iPcDJD6YvQYjoQc7sLF/IFhmNbEqgdzQo3lQ=.ed25519',
  content: {
    type: 'post',
    text: 'greetings hello nz.js'
  },
  timestamp: 1488613256922,
  signature: 'IBJXJC+DrwuX9iDwPUIJlSHs7BfENtx4D5fkCCT/+M42qhd6....==.sig.ed25519'
}
```

```js
var messageId = hash(message)
// => %emva3qXR6+XtLKwxWIsVB/hO1i5PmV9v2AP5hjRNDKQ
```
hash produces a unique, verifiable 'finger-print' of our message.

---
## examples - `about`

`%fiidAb7c6qPNtpeNkoeo+wFb+dKqJXEcyuMlT54V3Qg=.sha256`
  
```js
{
  author: "@azsQJqrOazV1/VC2hF5rSylaN4A1lTXPIuer+PdCQ3M=.ed25519",
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
  timestamp: 1487904949711,
  signature: "ce+JOzOxNdCj7Vkdlgmpd+yKbw4qMpIZLm/54FJdGCMleGOS...."
}
```

???

# this is emergent - show patchbay

---
## patchwork-next

![patchwork-next](patchwork-next.png)

---
## examples - `post`

`%vwCaR1lR02hiiInODqT4OmAgTSwNJ1AbYTYmfTwtXXw=.sha256`

```js
{
  author: "@z8aJVHJTc6MM8FwaNE2GIS3AYYt2HYFNWQUO8/iydNw=.ed25519",
  content: {
    type: "post",
    root: "%TapY6/6ghLYlTdn0pjm7rDLK5kcAhcqJarp9cWrwAvc=.sha256",
    text: "on the old-web I am the product.",
  },
  timestamp: 1488849598356,
  signature: "lVzsUsU42/wynxvTexKeQgjGC7HsJCkOnrr2yUrZbffguAEg..."
}
```

???

## and reply

---
## examples - `git-update`

![dnsssb](https://www.scuttlebutt.nz/assets/git-ssb-repo.png)

???
- code is just messages
- github as a fire-side story (I don't have to hang out with a company)

---
## examples - `issue`

???

## git issue

## person issue

---
## examples - `music`

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
## top-down UI 

![kiwibank](kiwibank.png) 

???
- re-presenting data 
  - why can't I re-present my own data
- comic sans: article about accessibility of fonts

## no ads

---
## papers please

![logins](username_taken.png)

???
- weird constraints on form filling in

## why would I need to present my papers before I speak?
- not chill 

---
## border control

???
## integrations!

- caught in some object beauracratic paper shuffle

## !erryday conversation

- github + social + music
- free-form interplay
  - possible futures
  - an expressive space

## one group multiple places
  - my identity is not just me, it's my context, my social graph

---
![sailing into the west](http://68.media.tumblr.com/23858ef00a47e7ee1255c1865ee2a319/tumblr_nd6hiqXZAy1sns9vwo1_1280.jpg)

### scuttlebutt.nz

???
It's just my opinion, but I'm investing in a more subjective web

what is wrong with the old-web?
  - it used to be cool
    - people making stuff however! woo!
  - platforms have brought sweet efficiency + interconneciton with their objective efficiency 
  - they're also a block

I set out on a journey, and I won't be coming back.

If you're curious, you're most welcome

---
background-color: black;
color: white;

## embracing subjectivity

.

