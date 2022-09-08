<template>
  <div class="flex flex-row">
    <!--row 1 -->
    <div id="a">
      <div id="a1" class="boardItemSize bg-blue-400">
        <img id="blackRookL" src="public/pieces/rook.svg"/>
      </div>
      <div id="a2" class="boardItemSize bg-blue-800">
        <img @click="decideMovePawn($event)" id="blackPawn1" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="a3" class="boardItemSize bg-blue-400">

      </div>
      <div id="a4" class="boardItemSize bg-blue-800">

      </div>
      <div id="a5" class="boardItemSize bg-blue-400">

      </div>
      <div id="a6" class="boardItemSize bg-blue-800">

      </div>
      <div id="a7" class="boardItemSize bg-blue-400">
        <img @click="decideMovePawn($event)" id="whitePawn1" class="invert w-[70%]" src="public/pieces/pawn.svg"/>
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
        <img @click="decideMovePawn($event)" id="blackPawn2" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="b3" class="boardItemSize bg-blue-800">

      </div>
      <div id="b4" class="boardItemSize bg-blue-400">

      </div>
      <div id="b5" class="boardItemSize bg-blue-800">

      </div>
      <div id="b6" class="boardItemSize bg-blue-400">

      </div>
      <div id="b7" class="boardItemSize bg-blue-800">
        <img @click="decideMovePawn($event)" id="whitePawn1" class="invert w-[70%]" src="public/pieces/pawn.svg"/>
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
        <img @click="decideMovePawn($event)" id="blackPawn3" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="c3" class="boardItemSize bg-blue-400">

      </div>
      <div id="c4" class="boardItemSize bg-blue-800">
      </div>
      <div id="c5" class="boardItemSize bg-blue-400">

      </div>
      <div id="c6" class="boardItemSize bg-blue-800">

      </div>
      <div id="c7" class="boardItemSize bg-blue-400">
        <img @click="decideMovePawn($event)" id="whitePawn3" class="w-[70%] invert" src="public/pieces/pawn.svg"/>
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
        <img @click="decideMovePawn($event)" id="blackPawn4" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="d3" class="boardItemSize bg-blue-800">

      </div>
      <div id="d4" class="boardItemSize bg-blue-400">

      </div>
      <div id="d5" class="boardItemSize bg-blue-800">

      </div>
      <div id="d6" class="boardItemSize bg-blue-400">

      </div>
      <div id="d7" class="boardItemSize bg-blue-800">
        <img @click="decideMovePawn($event)" id="whitePawn4" class="w-[70%] invert" src="public/pieces/pawn.svg"/>
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
        <img @click="decideMovePawn($event)" id="blackPawn5" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="e3" class="boardItemSize bg-blue-400">

      </div>
      <div id="e4" class="boardItemSize bg-blue-800">

      </div>
      <div id="e5" class="boardItemSize bg-blue-400">

      </div>
      <div id="e6" class="boardItemSize bg-blue-800">

      </div>
      <div id="e7" class="boardItemSize bg-blue-400">
        <img @click="decideMovePawn($event)" id="whitePawn5" class="w-[70%] invert" src="public/pieces/pawn.svg"/>
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
        <img @click="decideMovePawn($event)" id="blackPawn6" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="f3" class="boardItemSize bg-blue-800">

      </div>
      <div id="f4" class="boardItemSize bg-blue-400">

      </div>
      <div id="f5" class="boardItemSize bg-blue-800">

      </div>
      <div id="f6" class="boardItemSize bg-blue-400">

      </div>
      <div id="f7" class="boardItemSize bg-blue-800">
        <img @click="decideMovePawn($event)" id="whitePawn6" class="w-[70%] invert" src="public/pieces/pawn.svg"/>
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
        <img @click="decideMovePawn($event)" id="blackPawn7" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="g3" class="boardItemSize bg-blue-400">

      </div>
      <div id="g4" class="boardItemSize bg-blue-800">

      </div>
      <div id="g5" class="boardItemSize bg-blue-400">

      </div>
      <div id="g6" class="boardItemSize bg-blue-800">

      </div>
      <div id="g7" class="boardItemSize bg-blue-400">
        <img @click="decideMovePawn($event)" id="whitePawn7" class="w-[70%] invert" src="public/pieces/pawn.svg"/>
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
        <img @click="decideMovePawn($event)" id="blackPawn8" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div id="h3" class="boardItemSize bg-blue-800">

      </div>
      <div id="h4" class="boardItemSize bg-blue-400">

      </div>
      <div id="h5" class="boardItemSize bg-blue-800">

      </div>
      <div id="h6" class="boardItemSize bg-blue-400">

      </div>
      <div id="h7" class="boardItemSize bg-blue-800">
        <img @click="decideMovePawn($event)" id="whitePawn8" class="w-[70%] invert" src="public/pieces/pawn.svg"/>
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
    walkPawn(targeted, moveTo) {

      console.log("inWalk")
      let currentPawn

      if(targeted.target === undefined){
        currentPawn = targeted.id
        console.log("yeet",currentPawn);
      }
      else{
        currentPawn = targeted.target.id
        console.log("yeet",currentPawn);
      }

      const currentPawnId = document.getElementById(currentPawn);


      const moveToId = document.getElementById(moveTo);


      const targetClone = currentPawnId.cloneNode(true)

      moveToId.appendChild(targetClone)
      currentPawnId.remove()
      const self = this;
      moveToId.addEventListener("click", self.decideMovePawn(moveToId.childNodes[0]))
    },

    decideMovePawn(targeted) {
      console.log("Yeet", targeted)
      // Get block pawn is standing on
      let standingOn
      // Get current pawn in (white/black)Pawn# format
      let currentPawn

      if(targeted.target === undefined){
         standingOn = targeted.parentElement.id;
         currentPawn= targeted.id;
      }
      else{
         standingOn = targeted.target.parentElement.id;
         currentPawn= targeted.target.id;
      }


      // get only number of the square the pawn is standing on
      const standingOnNum = parseInt(standingOn.slice(1))
      // get the letter of the square the pawn is standing on
      const standingOnLett = standingOn.slice(0, 1);

      const currentPawnType = currentPawn.match(/[a-zA-Z]+/g);

      // Get current pawn's number
      const currentPawnNumber = parseInt(currentPawn.match(/\d/g));

      let pawnMoved
      if((standingOnNum === 2 && currentPawnType[0] === "blackPawn") || (standingOnNum === 7 && currentPawnType[0] === "whitePawn")) {
        pawnMoved = false
      }
      else{
        pawnMoved = true
      }
      if(!pawnMoved){
        let maxMoveTo
        let alsoMoveable
        if(standingOnNum === 2 && currentPawnType[0] === "blackPawn") {
          maxMoveTo = standingOnLett + (standingOnNum + 2)
          alsoMoveable = standingOnLett + (standingOnNum + 1)
        }
        else if(standingOnNum === 7 && currentPawnType[0] === "whitePawn") {
          maxMoveTo = standingOnLett + (standingOnNum - 2)
          alsoMoveable = standingOnLett + (standingOnNum - 1)
        }
        const maxMoveToId = document.getElementById(maxMoveTo);
        const alsoMoveableId = document.getElementById(alsoMoveable);

        maxMoveToId.classList.add("!bg-red-400");
        alsoMoveableId.classList.add("!bg-red-400");

        const self = this

        // Needs this goofy implementation or else I can't remove the event listener
        const _listener = function() {
          self.walkPawn(targeted, maxMoveTo);
          // Cleanup after itself
          maxMoveToId.removeEventListener("click", _listener);
          alsoMoveableId.removeEventListener("click", _listener2);
          maxMoveToId.classList.remove("!bg-red-400");
          alsoMoveableId.classList.remove("!bg-red-400");
        };
        const _listener2 = function() {
          self.walkPawn(targeted, alsoMoveable);
          // Cleanup after itself
          maxMoveToId.removeEventListener("click", _listener);
          alsoMoveableId.removeEventListener("click", _listener2);
          maxMoveToId.classList.remove("!bg-red-400");
          alsoMoveableId.classList.remove("!bg-red-400");
        };

        maxMoveToId.addEventListener("click", _listener);
        alsoMoveableId.addEventListener("click", _listener2);
      }
      else{
        console.log("pawn has moved")
        let moveable

        if(currentPawnType[0] === "blackPawn") {
          moveable = standingOnLett + (standingOnNum + 1)
        }
        else if(currentPawnType[0] === "whitePawn") {
          moveable = standingOnLett + (standingOnNum - 1)
        }
        const moveableId = document.getElementById(moveable);

        moveableId.classList.add("!bg-red-400");

        const self = this

        // Needs this goofy implementation or else I can't remove the event listener
        const _listener = function() {
          self.walkPawn(targeted, moveable);
          // Cleanup after itself
          moveableId.removeEventListener("click", _listener);
          moveableId.classList.remove("!bg-red-400");
        };

        moveableId.addEventListener("click", _listener);
      } 
    },
  }
}
</script>

<style>
.boardItemSize {
  @apply w-[100px] h-[100px] flex justify-center content-center
}
</style>