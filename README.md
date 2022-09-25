# BkChess: It's like chess but worse

In this project I want to attemt to make Chess easier to learn and also less boring by upping the pace and adding some funni
while making it more "realistic" by applying logic


Known bugs
----------
- None yet :)
----------

The differences between this and normal chess are:
- King and queen need to be captured to win (a country can still function with only one monarch and gender equality)
- Castling is not allowed (I don't understand it lol)
- Brutes only move 2 steps in a cross and kill everything in their path including thier own team

![Brute movement](bruteMovement.png)

- Enpessant is not allowed, I don't like the rule because you're hitting something that isn't there and it's confusing for new players


- Promotion is not allowed this leaves pawn stranded and unable to move as a kind of meat shield, brutes would be best to clear the way if you want them gone

 
- The clown has an AOE distraction effect, the blocks in front of it is are confused and won't be able to move except for the king because he's based. 
Can walk 1 step each direction
  ![clown movement](clownMovement.png)
- If movement fields of clowns overlaps and the other clown moves the clown will need to move to reset it because attention has been stolen
- Clowns can't distract other clowns

- Queen only moves 1 step in any direction and can't kill anything because she's old and decrepit, when she dies the team that didn't kill her has to skip 2 turns
- so if a white brute kills a white queen the black team has to skip 2 turns, no this isn't a bug I've covered up as a rule because I found it hilarious and writing this would probably take longer then fixing it

Progress so far:
- [x] Turns
- [x] Board made
- [x] Victory condition (if queen is killed last player can still walk because funni)

- Pawns
- [x] Pawns move
- [x] Pawns stop when they should
- [x] Pawns attack

- Brutes
- [x] Brute move
- [x] Brute attack
- [x] Brute can friendly fire

- Clowns
- [X] Clowns move
- [X] Clowns stop moving when they should
- [X] Clowns distract the right troops
- [X] Clowns can't distract themselves
- [X] Can remove each other's distraction

- Rooks
- [X] Rooks move
- [X] Rooks attack

- Queens
- [X] Queens move
- [X] Queens attack (who am I kidding)
- [X] Turns skip at death

- Kings
- [X] Kings move
- [X] Kings attack

## How to start programming

Project was made in [nuxt 3](https://v3.nuxtjs.org)

### Setup

Make sure to install the dependencies:

```bash
# npm
npm install
```

### Development Server

Start the development server on http://localhost:3000

```bash
npm run dev
```

### Production

Build the application for production:

```bash
npm run build
```

Locally preview production build:

```bash
npm run preview
```

Checkout the [deployment documentation](https://v3.nuxtjs.org/guide/deploy/presets) for more information.
