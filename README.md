# BkChess: It's like chess but worse

In this project I want to attemt to make Chess easier to learn and also less boring by upping the pace
white making it more "realistic" by applying logic

The differences between this and normal chess are:
- King and queen need to be captured to win (a country can still function with only one monarch)
- Castling is not allowed (it's dumb.)
- Knights are brutes
- Everything can kill eachother
- Brutes move 2 steps in a cross and kill everything in their path including thier own team

![Brute movement](bruteMovement.png)

- Enpessant is not allowed
- Promotion is not allowed this leaves pawn stranded and unable to move as a kind of meat shield, brutes need to clear the way if you want them gone

- The bichop has an AOE distraction effect, the blocks around is are confused and won't be able to move except for the king because he's based

The code is a mess right now and I should maybe fix it sometime...

Progress so far:
- [x] Turns
- [x] Board made
- [ ] Checkmate https://www.chess.com/terms/checkmate-chess

- Pawns
- [x] Pawns move
- [x] Pawns stop when they should
- 
- [x] Pawns attack

- Brutes
- [ ] Brute move
- [ ] Brute attack
- [ ] Brute can friendly fire

- Bishops
- [ ] Bishops move
- [ ] Bishops attack

- Rooks
- [ ] Rooks move
- [ ] Rooks attack

- Queens
- [ ] Queens move
- [ ] Queens attack

- Kings
- [ ] Kings move
- [ ] Kings attack

- Advanced stuff/rules:
- [ ] Check prevent walking into check https://www.chess.com/terms/check-chess  
- [ ] Stalemate  https://www.chess.com/terms/stalemate-chess

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
