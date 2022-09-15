<template>
  <div class="flex flex-row">
    <!--row 1 -->
    <!--        -->
    <div id="a">
      <div id="a1" class="boardItemSize bg-blue-400">

      </div>
      <div id="a2" class="boardItemSize bg-blue-800">
        <img @click="decideMoveRook($event)" id="blackRookL" src="pieces/rook.svg"/>
      </div>
      <div id="a3" class="boardItemSize bg-blue-400">
      </div>
      <div id="a4" class="boardItemSize bg-blue-800">
        <img @click="decideMovePawn($event)" id="blackPawn1" class="w-[70%]" src="pieces/pawn.svg"/>
      </div>
      <div id="a5" class="boardItemSize bg-blue-400">

      </div>
      <div id="a6" class="boardItemSize bg-blue-800">
        <img @click="decideMoveRook($event)" id="whiteRookL" class="invert" src="pieces/rook.svg"/>
      </div>
      <div id="a7" class="boardItemSize bg-blue-400">
        <img @click="decideMovePawn($event)" id="whitePawn1" class="invert w-[70%]" src="pieces/pawn.svg"/>
      </div>
      <div id="a8" class="boardItemSize bg-blue-800">

      </div>
    </div>
    <!--row 2 -->
    <div id="b">
      <div id="b1" class="boardItemSize bg-blue-800">
        <img id="blackHorseL" class="w-[70%] invert" src="pieces/brute.png"/>
      </div>
      <div id="b2" class="boardItemSize bg-blue-400">
        <img @click="decideMovePawn($event)" id="blackPawn2" class="w-[70%]" src="pieces/pawn.svg"/>
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
        <img @click="decideMovePawn($event)" id="whitePawn1" class="invert w-[70%]" src="pieces/pawn.svg"/>
      </div>
      <div id="b8" class="boardItemSize bg-blue-400">
        <img id="whiteHorseL" class="w-[70%]" src="pieces/brute.png"/>
      </div>
    </div>
    <!--row 3 -->
    <div id="c">
      <div id="c1" class="boardItemSize bg-blue-400">
        <img id="blackBitchshopL" class="w-[50%]" src="pieces/bitchshop.svg"/>
      </div>
      <div id="c2" class="boardItemSize bg-blue-800">
        <img @click="decideMovePawn($event)" id="blackPawn3" class="w-[70%]" src="pieces/pawn.svg"/>
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
        <img @click="decideMovePawn($event)" id="whitePawn3" class="w-[70%] invert" src="pieces/pawn.svg"/>
      </div>
      <div id="c8" class="boardItemSize bg-blue-800">
        <img id="whiteBitchshopL" class="w-[50%] invert" src="pieces/bitchshop.svg"/>
      </div>
    </div>
    <!--row 4 -->
    <div id="d">
      <div id="d1" class="boardItemSize bg-blue-800">
        <img id="blackKing" class="invert" src="pieces/king.png"/>
      </div>
      <div id="d2" class="boardItemSize bg-blue-400">
        <img @click="decideMovePawn($event)" id="blackPawn4" class="w-[70%]" src="pieces/pawn.svg"/>
      </div>
      <div id="d3" class="boardItemSize bg-blue-800">

      </div>
      <div id="d4" class="boardItemSize bg-blue-400">

      </div>
      <div id="d5" class="boardItemSize bg-blue-800">

      </div>
      <div id="d6" class="boardItemSize bg-blue-400">
        <img @click="decideMovePawn($event)" id="whitePawn4" class="w-[70%] invert" src="pieces/pawn.svg"/>
      </div>
      <div id="d7" class="boardItemSize bg-blue-800">

      </div>
      <div id="d8" class="boardItemSize bg-blue-400">
        <img id="whiteKing" class="" src="pieces/king.png"/>
      </div>
    </div>
    <!--row 5 -->
    <div id="e">
      <div id="e1" class="boardItemSize bg-blue-400">
        <img id="blackQueen" class="invert" src="pieces/queen.png"/>
      </div>
      <div id="e2" class="boardItemSize bg-blue-800">
        <img @click="decideMovePawn($event)" id="blackPawn5" class="w-[70%]" src="pieces/pawn.svg"/>
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
        <img @click="decideMovePawn($event)" id="whitePawn5" class="w-[70%] invert" src="pieces/pawn.svg"/>
      </div>
      <div id="e8" class="boardItemSize bg-blue-800">
        <img id="whiteQueen" class="" src="pieces/queen.png"/>
      </div>
    </div>
    <!--row 6 -->
    <div id="f">
      <div id="f1" class="boardItemSize bg-blue-800">
        <img id="blackBitchshopR" class="w-[50%]" src="pieces/bitchshop.svg"/>
      </div>
      <div id="f2" class="boardItemSize bg-blue-400">
        <img @click="decideMovePawn($event)" id="blackPawn6" class="w-[70%]" src="pieces/pawn.svg"/>
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
        <img @click="decideMovePawn($event)" id="whitePawn6" class="w-[70%] invert" src="pieces/pawn.svg"/>
      </div>
      <div id="f8" class="boardItemSize bg-blue-400">
        <img id="whiteBitchshopR" class="w-[50%] invert" src="pieces/bitchshop.svg"/>
      </div>
    </div>
    <!--row 7 -->
    <div id="g">
      <div id="g1" class="boardItemSize bg-blue-400">
        <img id="blackHorseR" class="w-[70%] invert" src="pieces/brute.png"/>
      </div>
      <div id="g2" class="boardItemSize bg-blue-800">
        <img @click="decideMovePawn($event)" id="blackPawn7" class="w-[70%]" src="pieces/pawn.svg"/>
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
        <img @click="decideMovePawn($event)" id="whitePawn7" class="w-[70%] invert" src="pieces/pawn.svg"/>
      </div>
      <div id="g8" class="boardItemSize bg-blue-800">
        <img id="whiteHorseR" class="w-[70%]" src="pieces/brute.png"/>
      </div>
    </div>
    <!--row 8 -->
    <div id="h">
      <div id="h1" class="boardItemSize bg-blue-800">
        <img @click="decideMoveRook($event)" id="blackRookR" src="pieces/rook.svg"/>
      </div>
      <div id="h2" class="boardItemSize bg-blue-400">
        <img @click="decideMovePawn($event)" id="blackPawn8" class="w-[70%]" src="pieces/pawn.svg"/>
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
        <img @click="decideMovePawn($event)" id="whitePawn8" class="w-[70%] invert" src="pieces/pawn.svg"/>
      </div>
      <div id="h8" class="boardItemSize bg-blue-400">
        <img @click="decideMoveRook($event)" id="whiteRookL" class="invert" src="pieces/rook.svg"/>
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
      alphabet: ["a", "b", "c", "d", "e", "f", "g", "h"],
      freeData:null
    }
  },
  methods: {
    walkPawn(targeted, moveTo) {
      let currentPawn

      if (targeted.target === undefined) {
        currentPawn = targeted.id
      } else {
        currentPawn = targeted.target.id
      }

      const currentPawnId = document.getElementById(currentPawn);


      const moveToId = document.getElementById(moveTo);


      const targetClone = currentPawnId.cloneNode(true)

      moveToId.appendChild(targetClone)
      currentPawnId.remove()
      const self = this;
      moveToId.addEventListener("click", self.decideMovePawn(moveToId.childNodes[0]))
      document.querySelectorAll(".walkColor").forEach((el) => {
        el.classList.remove("walkColor");
      });
      document.querySelectorAll(".attackColor").forEach((el) => {
        el.classList.remove("attackColor");
      });
    },

    attackPawn(targeted, moveTo) {
      let currentPawn

      if (targeted.target === undefined) {
        currentPawn = targeted.id
      } else {
        currentPawn = targeted.target.id
      }

      const currentPawnId = document.getElementById(currentPawn);


      const moveToId = document.getElementById(moveTo);


      const targetClone = currentPawnId.cloneNode(true)

      // Remove attackee and remove pawn from old position
      moveToId.childNodes[0].remove();
      currentPawnId.remove()

      // Add the cloned pawn to the new position
      moveToId.appendChild(targetClone)
      const self = this;
      moveToId.addEventListener("click", self.decideMovePawn(moveToId.childNodes[0]))
    },

    decideMovePawn(targeted) {
      // Get block pawn is standing on
      let standingOn
      // Get current pawn in (white/black)Pawn# format
      let currentPawn

      // Make sure the method works for both first and 2nd move
      if (targeted.target === undefined) {
        standingOn = targeted.parentElement.id;
        currentPawn = targeted.id;
      } else {
        standingOn = targeted.target.parentElement.id;
        currentPawn = targeted.target.id;
      }


      // get only number of the square the pawn is standing on
      const standingOnNum = parseInt(standingOn.slice(1))
      // get the letter of the square the pawn is standing on
      const standingOnLett = standingOn.slice(0, 1);

      const currentPawnType = currentPawn.match(/[a-zA-Z]+/g);

      // Get current pawn's number
      const currentPawnNumber = parseInt(currentPawn.match(/\d/g));

      // Check if pawn has been moved so it can only take 2 steps once
      let pawnMoved = true
      if ((standingOnNum === 2 && currentPawnType[0] === "blackPawn") || (standingOnNum === 7 && currentPawnType[0] === "whitePawn")) {
        pawnMoved = false
      }

      if (!pawnMoved) {
        let maxMoveTo
        let alsoMoveable
        if (standingOnNum === 2 && currentPawnType[0] === "blackPawn") {
          maxMoveTo = standingOnLett + (standingOnNum + 2)
          alsoMoveable = standingOnLett + (standingOnNum + 1)
        } else if (standingOnNum === 7 && currentPawnType[0] === "whitePawn") {
          maxMoveTo = standingOnLett + (standingOnNum - 2)
          alsoMoveable = standingOnLett + (standingOnNum - 1)
        }
        const maxMoveToId = document.getElementById(maxMoveTo);
        const alsoMoveableId = document.getElementById(alsoMoveable);


        // Check if pawn is blocked by something

        const blockedMax = maxMoveToId.childNodes.length > 0
        const blockedAlso = alsoMoveableId.childNodes.length > 0
        if (!blockedMax && !blockedAlso) {


          maxMoveToId.classList.add("walkColor");
        }
        if (!blockedAlso) {
          alsoMoveableId.classList.add("walkColor");
        }
        // Get the current letter index the pawn is standing on in the aplhabet array


        const curLetterindex = this.alphabet.indexOf(standingOnLett)
        let leftPos

        // Make sure the pawn doesn't go off the board
        if (curLetterindex > 0) {
          const leftLetter = this.alphabet[curLetterindex - 1]
          if (currentPawnType[0] === "blackPawn") {
            leftPos = leftLetter + (standingOnNum + 1)
          } else if (currentPawnType[0] === "whitePawn") {
            leftPos = leftLetter + (standingOnNum - 1)
          }
        }

        const self = this

        let rightPos

        // Make sure the pawn doesn't go off the board
        if (curLetterindex < this.alphabet.length - 1) {
          const rightLetter = this.alphabet[curLetterindex + 1]
          // Check what type the pawn is and add or subtract 1 from the number so it moves correctly

          if (currentPawnType[0] === "blackPawn") {
            rightPos = rightLetter + (standingOnNum + 1)
          } else if (currentPawnType[0] === "whitePawn") {
            rightPos = rightLetter + (standingOnNum - 1)
          }
        }
        const currentPawnColor = currentPawn.match(/[black||white]+/g)[0];

        let attackRightId
        let rightAttackable = false
        if (rightPos !== undefined) {
          attackRightId = document.getElementById(rightPos);
          if (attackRightId.childNodes.length > 0) {
            rightAttackable = attackRightId.childNodes[0].id.match(/[black||white]+/g)[0] !== currentPawnColor;
          }
        }
        let attackLeftId
        let leftAttackable = false
        if (leftPos !== undefined) {
          attackLeftId = document.getElementById(leftPos);
          if (attackLeftId.childNodes.length > 0) {
            leftAttackable = attackLeftId.childNodes[0].id.match(/[black||white]+/g)[0] !== currentPawnColor;
          }
        }

        if (leftAttackable) {
          attackLeftId.classList.add("attackColor");
          const self = this

          // Needs this goofy implementation or else I can't remove the event listener
          const _listener = function () {
            self.attackPawn(targeted, leftPos);
            // Cleanup after itself
            attackLeftId.removeEventListener("click", _listener);
            attackLeftId.classList.remove("attackColor");

            // Remove the other parts too if you have multiple options
            if (leftAttackable) {
              attackRightId.removeEventListener("click", _listener);
              attackRightId.classList.remove("attackColor");
            }
          };

          attackLeftId.addEventListener("click", _listener);
        }
        if (rightAttackable) {
          attackRightId.classList.add("attackColor");
          const self = this

          // Needs this goofy implementation or else I can't remove the event listener
          const _listener = function () {
            self.attackPawn(targeted, rightPos);
            // Cleanup after itself
            attackRightId.removeEventListener("click", _listener);
            attackRightId.classList.remove("attackColor");

            if (leftAttackable) {
              attackLeftId.removeEventListener("click", _listener);
              attackLeftId.classList.remove("attackColor");
            }
          };

          attackRightId.addEventListener("click", _listener);
        }

        // Needs this goofy implementation or else I can't remove the event listener
        const _listener = function () {
          self.walkPawn(targeted, maxMoveTo);
          // Cleanup after itself
          maxMoveToId.removeEventListener("click", _listener);
          alsoMoveableId.removeEventListener("click", _listener2);
          maxMoveToId.classList.remove("walkColor");
          alsoMoveableId.classList.remove("walkColor");
        };
        const _listener2 = function () {
          self.walkPawn(targeted, alsoMoveable);
          // Cleanup after itself
          maxMoveToId.removeEventListener("click", _listener);
          alsoMoveableId.removeEventListener("click", _listener2);
          maxMoveToId.classList.remove("walkColor");
          alsoMoveableId.classList.remove("walkColor");
        };

        if (!blockedMax && !blockedAlso) {
          maxMoveToId.addEventListener("click", _listener);
        }
        if (!blockedAlso) {
          alsoMoveableId.addEventListener("click", _listener2);
        }
      } else {
        let moveable

        if (currentPawnType[0] === "blackPawn") {
          moveable = standingOnLett + (standingOnNum + 1)
        } else if (currentPawnType[0] === "whitePawn") {
          moveable = standingOnLett + (standingOnNum - 1)
        }
        const moveableId = document.getElementById(moveable);

        // Check if pawn is blocked by something
        const blocked = moveableId.childNodes.length > 0

        // Get the current letter index the pawn is standing on in the aplhabet array
        const curLetterindex = this.alphabet.indexOf(moveable.slice(0, 1))

        let leftPos
        // Make sure the pawn doesn't go off the board
        if (curLetterindex > 0) {
          const leftLetter = this.alphabet[curLetterindex - 1]
          if (currentPawnType[0] === "blackPawn") {
            leftPos = leftLetter + parseInt(moveable.slice(1))
          } else if (currentPawnType[0] === "whitePawn") {
            leftPos = leftLetter + parseInt(moveable.slice(1))
          }
        }

        let rightPos
        // Make sure the pawn doesn't go off the board
        if (curLetterindex < this.alphabet.length - 1) {
          const rightLetter = this.alphabet[curLetterindex + 1]

          // Check what type the pawn is and add or subtract 1 from the number so it moves correctly
          if (currentPawnType[0] === "blackPawn") {
            rightPos = rightLetter + parseInt(moveable.slice(1))
          } else if (currentPawnType[0] === "whitePawn") {
            rightPos = rightLetter + parseInt(moveable.slice(1))
          }
        }
        let attackRightId
        let rightAttackable = false
        if (rightPos !== undefined) {
          attackRightId = document.getElementById(rightPos);
          if (attackRightId.childNodes.length > 0) {
            rightAttackable = true
          }
        }
        let attackLeftId
        let leftAttackable = false
        if (leftPos !== undefined) {
          attackLeftId = document.getElementById(leftPos);
          if (attackLeftId.childNodes.length > 0) {
            leftAttackable = true
          }
        }

        if (leftAttackable) {
          attackLeftId.classList.add("attackColor");
          const self = this

          // Needs this goofy implementation or else I can't remove the event listener
          const _listener = function () {
            self.attackPawn(targeted, leftPos);
            // Cleanup after itself
            attackLeftId.removeEventListener("click", _listener);
            attackLeftId.classList.remove("attackColor");

            // Remove the other parts too if you have multiple options
            if (leftAttackable) {
              attackRightId.removeEventListener("click", _listener);
              attackRightId.classList.remove("attackColor");
            }
          };

          attackLeftId.addEventListener("click", _listener);
        }
        if (rightAttackable) {
          attackRightId.classList.add("attackColor");
          const self = this

          // Needs this goofy implementation or else I can't remove the event listener
          const _listener = function () {
            self.attackPawn(targeted, rightPos);
            // Cleanup after itself
            attackRightId.removeEventListener("click", _listener);
            attackRightId.classList.remove("attackColor");
            attackLeftId.removeEventListener("click", _listener);
            attackLeftId.classList.remove("attackColor");
          };

          attackRightId.addEventListener("click", _listener);
        }

        // Prevent pawn from moving if blocked
        if (!blocked) {

          moveableId.classList.add("walkColor");

          const self = this

          // Needs this goofy implementation or else I can't remove the event listener
          const _listener = function () {
            self.walkPawn(targeted, moveable);
            // Cleanup after itself
            moveableId.removeEventListener("click", _listener);
            moveableId.classList.remove("walkColor");
          };

          moveableId.addEventListener("click", _listener);
        }
      }
    },

    walkRook(targeted, moveTo){
      let currentRook

      if (targeted.target === undefined) {
        currentRook = targeted.id
      } else {
        currentRook = targeted.target.id
      }

      const currentPawnId = document.getElementById(currentRook);


      const moveToId = document.getElementById(moveTo);


      const targetClone = currentPawnId.cloneNode(true)

      moveToId.appendChild(targetClone)
      currentPawnId.remove()
      const self = this;
      // I needed to make the function a variable to call it, dunno why but I need to do it
      const _listener = function () {
        console.log(moveToId.childNodes[0])
        self.decideMoveRook(moveToId.childNodes[0]);
      };
      moveToId.addEventListener("click", _listener, { once: true });
      document.querySelectorAll(".walkColor").forEach((el) => {
        el.classList.remove("walkColor");
      });
      document.querySelectorAll(".attackColor").forEach((el) => {
        el.classList.remove("attackColor");
      });
    },

    decideMoveRook(targeted) {

      // Get block pawn is standing on
      let standingOn
      // Get current pawn in (white/black)Rook(R/L) format
      let currentRook
      if (targeted.target === undefined) {
        standingOn = targeted.parentElement.id;
        currentRook = targeted.id;
      } else {
        standingOn = targeted.target.parentElement.id;
        currentRook = targeted.target.id;
      }

      // get only number of the square the pawn is standing on
      const standingOnNum = parseInt(standingOn.slice(1))

      // get the letter of the square the pawn is standing on
      const standingOnLett = standingOn.slice(0, 1);

      const currentRookColor = currentRook.match(/[^RoL]+/g)[0];

      let maxMoveTo
      let topMax
      let bottomMax
      for (let i = 1; i < 9; i++) {
        let topEmpty = false
        let bottomEmpty = false
        let canGoTo = document.getElementById(standingOnLett + i)
        maxMoveTo = standingOnLett + i

        if (canGoTo.childNodes.length === 0 && i === 1) {
          topMax = standingOnLett + 1
          topEmpty = true
        }
        if (canGoTo.childNodes.length === 0 && i === 8) {
          bottomMax = standingOnLett + 8
          bottomEmpty = true
        }

        let stuckFront = false
        let stuckBack = false
        if (canGoTo.childNodes.length !== 0) {
          if (canGoTo.childNodes[0] !== document.getElementById(currentRook)) {
            const goToColor = canGoTo.childNodes[0].id.match(/[black|white]+/g)[0]
            if (goToColor === currentRookColor) {
              stuckFront = true
            }
          }
        }


        let canGoToPrev
        canGoToPrev = document.getElementById(standingOnLett + (standingOnNum + 1))
        if (canGoToPrev.childNodes.length !== 0) {
          if (canGoToPrev.childNodes[0] !== document.getElementById(currentRook)) {
            const goToColor = canGoToPrev.childNodes[0].id.match(/[black|white]+/g)[0]
            if (goToColor === currentRookColor) {
              stuckBack = true
            }
          }
        }

        if (stuckFront && stuckBack) {
          break
        }


        if (canGoTo.childNodes.length > 0) {
          if (canGoTo.childNodes[0] !== document.getElementById(currentRook)) {
            if (i < standingOnNum) {
              topMax = maxMoveTo
            } else {
              bottomMax = maxMoveTo
            }
          }
        }

        if (canGoTo.childNodes[0] !== document.getElementById(currentRook) && canGoTo.childNodes.length === 0) {
          canGoTo.classList.add("walkColor");

          const self = this
          const canGoToCopy = canGoTo
          const maxMoveToCopy = maxMoveTo

          const _listener = function () {
            self.walkRook(targeted, maxMoveToCopy);
            // Cleanup after itself
            canGoToCopy.removeEventListener("click", _listener);
          };

          canGoTo.addEventListener("click", _listener, {once: true});
        }

        if ((topMax !== undefined || bottomMax !== undefined) && canGoTo.childNodes.length > 0) {
          const goToColor = canGoTo.childNodes[0].id.match(/[black|white]+/g)[0]
          if (!topEmpty) {
            canGoTo.classList.remove("walkColor");
            if (goToColor !== currentRookColor) {
              canGoTo.classList.add("attackColor");
            }
          } else {
            console.log("goofed")
          }

          if (!bottomEmpty) {
            canGoTo.classList.remove("walkColor");
            if (goToColor !== currentRookColor) {
              canGoTo.classList.add("attackColor");
            }
          }
          // console.log('TopMax ', topMax, 'bottomMax', bottomMax, 'topEmpty', topEmpty, 'bottomEmpty', bottomEmpty, 'can go to ', canGoTo, 'can go to child', canGoTo.childNodes)
        }
      }

      let leftMax
      let rightMax
      let curLetterindex = this.alphabet.indexOf(standingOnLett)
      for (let i = 0; i < 8; i++) {
        let leftEmpty = false
        let rightEmpty = false
        let canGoTo = document.getElementById(this.alphabet[i] + standingOnNum)
        maxMoveTo = this.alphabet[i] + standingOnNum

        if (canGoTo.childNodes.length === 0 && i === 1) {
          leftMax = this.alphabet[1] + standingOnNum
          leftEmpty = true
        }
        if (canGoTo.childNodes.length === 0 && i === 8) {
          rightMax = this.alphabet[8] + standingOnNum
          rightEmpty = true
        }

        if (canGoTo.childNodes.length > 0 && canGoTo.childNodes[0] !== document.getElementById(currentRook)) {
          if (i < this.alphabet.indexOf(standingOnLett)) {
            leftMax = maxMoveTo
          } else {
            rightMax = maxMoveTo
          }
        }

        if (canGoTo.childNodes[0] !== document.getElementById(currentRook) && canGoTo.childNodes.length === 0) {
          canGoTo.classList.add("walkColor");
          const self = this
          const canGoToCopy = canGoTo
          const maxMoveToCopy = maxMoveTo

          const _listener = function () {
            self.walkRook(targeted, maxMoveToCopy);
            // Cleanup after itself
            canGoToCopy.removeEventListener("click", _listener);
          };

          canGoTo.addEventListener("click", _listener, {once: true});
        }

        if (leftMax !== undefined && rightMax !== undefined) {
          const goToColor = canGoTo.childNodes[0].id.match(/[black|white]+/g)[0]
          if (!leftEmpty) {
            canGoTo.classList.remove("walkColor");
            if (goToColor !== currentRookColor) {
              canGoTo.classList.add("attackColor");
            }
          }
          if (!rightEmpty) {
            canGoTo.classList.remove("walkColor");
            if (goToColor !== currentRookColor) {
              canGoTo.classList.add("attackColor");
            }
          }
          break
        }
      }
    },
  }
}
</script>

<style>
.boardItemSize {
  @apply w-[100px] h-[100px] flex justify-center content-center
}

.walkColor {
  @apply bg-green-400
}

.attackColor {
  @apply bg-red-400
}
</style>