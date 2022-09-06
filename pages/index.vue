<template>
  <div class="flex flex-row">
    <!--row 1 -->
    <div id="a">
      <div id="a1" class="boardItemSize bg-blue-400">
        <img id="blackRookL" src="public/pieces/rook.svg"/>
      </div>
      <div id="a2" class="boardItemSize bg-blue-800">
        <img @click="movePawn($event)" id="blackPawn1" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="a3" class="boardItemSize bg-blue-400">
        3
      </div>
      <div id="a4" class="boardItemSize bg-blue-800">
        4
      </div>
      <div id="a5" class="boardItemSize bg-blue-400">
        5
      </div>
      <div id="a6" class="boardItemSize bg-blue-800">
        6
      </div>
      <div id="a7" class="boardItemSize bg-blue-400">
        <img @click="movePawn($event)" id="whitePawn1" class="invert w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="a8" class="boardItemSize bg-blue-800">
        <img id="whiteRookL" class="invert" src="public/pieces/rook.svg"/>
      </div>
    </div>
    <!--row 2 -->
    <div id="b">
      <div id="b1" class="boardItemSize bg-blue-800">
        <img id="blackHorseL" class="w-[70%]" src="public/pieces/horse.svg"/>
      </div>
      <div id="b2" class="boardItemSize bg-blue-400">
        <img @click="movePawn($event)" id="blackPawn2" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="b3" class="boardItemSize bg-blue-800">
        3
      </div>
      <div id="b4" class="boardItemSize bg-blue-400">
        4
      </div>
      <div id="b5" class="boardItemSize bg-blue-800">
        5
      </div>
      <div id="b6" class="boardItemSize bg-blue-400">
        6
      </div>
      <div id="b7" class="boardItemSize bg-blue-800">
        <img @click="movePawn($event)" id="whitePawn1" class="invert w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="b8" class="boardItemSize bg-blue-400">
        <img id="whiteHorseL" class="w-[70%] invert" src="public/pieces/horse.svg"/>
      </div>
    </div>
    <!--row 3 -->
    <div id="c">
      <div id="c1" class="boardItemSize bg-blue-400">
        <img id="blackBitchshopL" class="w-[50%]" src="public/pieces/bitchshop.svg"/>
      </div>
      <div id="c2" class="boardItemSize bg-blue-800">
        <img @click="movePawn($event)" id="blackPawn2" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="c3" class="boardItemSize bg-blue-400">
        3
      </div>
      <div id="c4" class="boardItemSize bg-blue-800">
        4
      </div>
      <div id="c5" class="boardItemSize bg-blue-400">
        5
      </div>
      <div id="c6" class="boardItemSize bg-blue-800">
        6
      </div>
      <div id="c7" class="boardItemSize bg-blue-400">
        <img @click="movePawn($event)" id="whitePawn3" class="w-[70%] invert" src="public/pieces/pawn.svg"/>
      </div>
      <div id="c8" class="boardItemSize bg-blue-800">
        <img id="whiteBitchshopL" class="w-[50%] invert" src="public/pieces/bitchshop.svg"/>
      </div>
    </div>
    <!--row 4 -->
    <div id="d">
      <div id="d1" class="boardItemSize bg-blue-800">
        <img id="blackQueen" class="invert" src="public/pieces/queen.png"/>
      </div>
      <div id="d2" class="boardItemSize bg-blue-400">
        <img @click="movePawn($event)" id="blackPawn4" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="d3" class="boardItemSize bg-blue-800">
        3
      </div>
      <div id="d4" class="boardItemSize bg-blue-400">
        4
      </div>
      <div id="d5" class="boardItemSize bg-blue-800">
        5
      </div>
      <div id="d6" class="boardItemSize bg-blue-400">
        6
      </div>
      <div id="d7" class="boardItemSize bg-blue-800">
        <img @click="movePawn($event)" id="whitePawn4" class="w-[70%] invert" src="public/pieces/pawn.svg"/>
      </div>
      <div id="d8" class="boardItemSize bg-blue-400">
        <img id="whiteKing" class="" src="public/pieces/king.png"/>
      </div>
    </div>
    <!--row 5 -->
    <div id="e">
      <div id="e1" class="boardItemSize bg-blue-400">
        <img id="blackKing" class="invert" src="public/pieces/king.png"/>
      </div>
      <div id="e2" class="boardItemSize bg-blue-800">
        <img @click="movePawn($event)" id="blackPawn5" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="e3" class="boardItemSize bg-blue-400">
        3
      </div>
      <div id="e4" class="boardItemSize bg-blue-800">
        4
      </div>
      <div id="e5" class="boardItemSize bg-blue-400">
        5
      </div>
      <div id="e6" class="boardItemSize bg-blue-800">
        6
      </div>
      <div id="e7" class="boardItemSize bg-blue-400">
        <img @click="movePawn($event)" id="whitePawn5" class="w-[70%] invert" src="public/pieces/pawn.svg"/>
      </div>
      <div id="e8" class="boardItemSize bg-blue-800">
        <img id="whiteQueen" class="" src="public/pieces/queen.png"/>
      </div>
    </div>
    <!--row 6 -->
    <div id="f">
      <div id="f1" class="boardItemSize bg-blue-800">
        <img id="blackBitchshopR" class="w-[50%]" src="public/pieces/bitchshop.svg"/>
      </div>
      <div id="f2" class="boardItemSize bg-blue-400">
        <img @click="movePawn($event)" id="blackPawn6" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="f3" class="boardItemSize bg-blue-800">
        3
      </div>
      <div id="f4" class="boardItemSize bg-blue-400">
        4
      </div>
      <div id="f5" class="boardItemSize bg-blue-800">
        5
      </div>
      <div id="f6" class="boardItemSize bg-blue-400">
        6
      </div>
      <div id="f7" class="boardItemSize bg-blue-800">
        <img @click="movePawn($event)" id="whitePawn6" class="w-[70%] invert" src="public/pieces/pawn.svg"/>
      </div>
      <div id="f8" class="boardItemSize bg-blue-400">
        <img id="whiteBitchshopR" class="w-[50%] invert" src="public/pieces/bitchshop.svg"/>
      </div>
    </div>
    <!--row 7 -->
    <div id="g">
      <div id="g1" class="boardItemSize bg-blue-400">
        <img id="blackHorseR" class="w-[70%]" src="public/pieces/horse.svg"/>
      </div>
      <div id="g2" class="boardItemSize bg-blue-800">
        <img @click="movePawn($event)" id="blackPawn7" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="g3" class="boardItemSize bg-blue-400">
        3
      </div>
      <div id="g4" class="boardItemSize bg-blue-800">
        4
      </div>
      <div id="g5" class="boardItemSize bg-blue-400">
        5
      </div>
      <div id="g6" class="boardItemSize bg-blue-800">
        6
      </div>
      <div id="g7" class="boardItemSize bg-blue-400">
        <img @click="movePawn($event)" id="whitePawn7" class="w-[70%] invert" src="public/pieces/pawn.svg"/>
      </div>
      <div id="g8" class="boardItemSize bg-blue-800">
        <img id="whiteHorseR" class="w-[70%] invert" src="public/pieces/horse.svg"/>
      </div>
    </div>
    <!--row 8 -->
    <div id="h">
      <div id="h1" class="boardItemSize bg-blue-800">
        <img id="blackRookR" src="public/pieces/rook.svg"/>
      </div>
      <div id="h2" class="boardItemSize bg-blue-400">
        <img @click="movePawn($event)" id="blackPawn8" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="h3" class="boardItemSize bg-blue-800">
        3
      </div>
      <div id="h4" class="boardItemSize bg-blue-400">
        4
      </div>
      <div id="h5" class="boardItemSize bg-blue-800">
        5
      </div>
      <div id="h6" class="boardItemSize bg-blue-400">
        6
      </div>
      <div id="h7" class="boardItemSize bg-blue-800">
        <img @click="movePawn($event)" id="whitePawn8" class="w-[70%] invert" src="public/pieces/pawn.svg"/>
      </div>
      <div id="h8" class="boardItemSize bg-blue-400">
        <img id="whiteRookL" class="invert" src="public/pieces/rook.svg"/>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "index",
  head() {
    return {
      title: "TopGhess"
    };
  },
  data() {
    return {
      alphabetic: ["a", "b", "c", "d", "e", "f", "g", "h"],
    }
  },
  methods: {
    movePawn(targeted) {

      const standingOn = targeted.target.parentElement.id;
      const currentPawn = targeted.target.id;
      const currentPawnNumber = parseInt(currentPawn.match(/\d/g));

      const staningOnNum = parseInt(standingOn.slice(1))
      if( (staningOnNum-1) === currentPawnNumber){
        const pawnMoved = false
      }
      else{
        const pawnMoved = true
      }
    }
  }
}
</script>

<style>
.boardItemSize {
  @apply w-[100px] h-[100px] flex justify-center content-center
}
</style>