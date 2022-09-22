<template>
  <div id="wrapper" class="flex justify-center content-center flex-col">
    <h1 class="text-white text-center">It's now: <span class="bold text-3xl">{{ turn }}</span> 's turn</h1>
    <div id="board" class="flex justify-center">
      <div class="flex flex-row select-none">
        <!--row 1 -->
        <div id="a">
          <div id="a1" class="boardItemSize bg-blue-400">
            <img @click="decideMoveRook($event)" id="blackRookL" src="pieces/rook.svg"/>
          </div>
          <div id="a2" class="boardItemSize bg-blue-800">
            <img @click="decideMovePawn($event)" id="blackPawn1" class="w-[70%]" src="pieces/pawn.svg"/>
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
            <img @click="decideMovePawn($event)" id="whitePawn1" class="invert w-[70%]" src="pieces/pawn.svg"/>
          </div>
          <div id="a8" class="boardItemSize bg-blue-800">
            <img @click="decideMoveRook($event)" id="whiteRookL" class="invert" src="pieces/rook.svg"/>
          </div>
        </div>
        <!--row 2 -->
        <div id="b">
          <div id="b1" class="boardItemSize bg-blue-800">

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
            <img @click="decideMovePawn($event)" id="whitePawn2" class="invert w-[70%]" src="pieces/pawn.svg"/>
          </div>
          <div id="b8" class="boardItemSize bg-blue-400">
            <img @click="decideMoveBrute($event)" id="whiteBruteL" class="w-[70%]" src="pieces/brute.png"/>
          </div>
        </div>
        <!--row 3 -->
        <div id="c">
          <div id="c1" class="boardItemSize bg-blue-400">
            <img id="blackClownL" class="w-[50%] invert" src="pieces/clown.png"/>
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
            <img id="whiteClownL" class="w-[50%]" src="pieces/clown.png"/>
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
            <img @click="decideMoveBrute($event)" id="blackBruteL" class="w-[70%] invert" src="pieces/brute.png"/>
          </div>
          <div id="d4" class="boardItemSize bg-blue-400">

          </div>
          <div id="d5" class="boardItemSize bg-blue-800">

          </div>
          <div id="d6" class="boardItemSize bg-blue-400">

          </div>
          <div id="d7" class="boardItemSize bg-blue-800">
            <img @click="decideMovePawn($event)" id="whitePawn4" class="w-[70%] invert" src="pieces/pawn.svg"/>
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
            <img id="blackPawnR" class="w-[50%] invert" src="pieces/clown.png"/>
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
            <img id="whiteKnightR" class="w-[50%]" src="pieces/clown.png"/>
          </div>
        </div>
        <!--row 7 -->
        <div id="g">
          <div id="g1" class="boardItemSize bg-blue-400">
            <img @click="decideMoveBrute($event)" id="blackBruteR" class="w-[70%] invert" src="pieces/brute.png"/>
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
            <img @click="decideMoveBrute($event)" id="whiteBruteR" class="w-[70%]" src="pieces/brute.png"/>
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
            <img @click="decideMoveRook($event)" id="whiteRookR" class="invert" src="pieces/rook.svg"/>
          </div>
        </div>
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
      turn: "white",
    }
  },
  methods: {
    // Universal functions
    switchTurn(switchColor = true) {
      if (switchColor) {
        if (this.turn === "white") {
          // TODO: change back to black
          this.turn = "black"
        } else {
          this.turn = "black"
        }
      } else {
        console.log("not switching turn")
      }
      // Remove all the walk or attack classes
      document.querySelectorAll(".walkColor").forEach((el) => {
        el.classList.remove("walkColor");
      });
      document.querySelectorAll(".attackColor").forEach((el) => {
        el.classList.remove("attackColor");
      });

      // Remove the board from the DOM and place it back with a clone to delete all the event listeners
      const board = document.getElementById("board")
      const boardClone = board.cloneNode(true)
      const wrapper = document.getElementById("wrapper")
      board.remove()
      wrapper.appendChild(boardClone)


      // Put event listeners back on pawn
      for (let i = 1; i < 9; i++) {
        const pawnToSelect = this.turn + "Pawn" + i
        const pawnSelected = document.getElementById(pawnToSelect)
        if (pawnSelected) {
          pawnSelected.addEventListener("click", (e) => {
            this.decideMovePawn(e)
          })
        }
      }

      const rookToSelectL = this.turn + "RookL"
      const rookToSelectR = this.turn + "RookR"

      const rookSelectedL = document.getElementById(rookToSelectL)
      const rookSelectedR = document.getElementById(rookToSelectR)

      if (rookSelectedL) {
        rookSelectedL.addEventListener("click", (e) => {
          this.decideMoveRook(e)
        })
      }
      if (rookSelectedR) {
        rookSelectedR.addEventListener("click", (e) => {
          this.decideMoveRook(e)
        })
      }

      const bruteToSelectL = this.turn + "BruteL"
      const bruteToSelectR = this.turn + "BruteR"

      const bruteSelectedL = document.getElementById(bruteToSelectL)
      const bruteSelectedR = document.getElementById(bruteToSelectR)

      if (bruteSelectedL) {
        bruteSelectedL.addEventListener("click", (e) => {
          this.decideMoveBrute(e)
        })
      }
      if (bruteSelectedR) {
        bruteSelectedR.addEventListener("click", (e) => {
          this.decideMoveBrute(e)
        })
      }

    },


    // Pawn move set
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

      this.switchTurn()
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

      this.switchTurn()
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
          };

          attackLeftId.addEventListener("click", _listener);
        }
        if (rightAttackable) {
          attackRightId.classList.add("attackColor");
          const self = this

          // Needs this goofy implementation or else I can't remove the event listener
          const _listener = function () {
            self.attackPawn(targeted, rightPos);
          };

          attackRightId.addEventListener("click", _listener);
        }

        // Needs this goofy implementation or else I can't remove the event listener
        const _listener = function () {
          self.walkPawn(targeted, maxMoveTo);
        };
        const _listener2 = function () {
          self.walkPawn(targeted, alsoMoveable);
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
          };

          attackLeftId.addEventListener("click", _listener);
        }
        if (rightAttackable) {
          attackRightId.classList.add("attackColor");
          const self = this

          // Needs this goofy implementation or else I can't remove the event listener
          const _listener = function () {
            self.attackPawn(targeted, rightPos);
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
          };

          moveableId.addEventListener("click", _listener);
        }
      }
    },


    // Rook move set
    walkRook(targeted, moveTo) {
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
        self.decideMoveRook(moveToId.childNodes[0]);
      };
      moveToId.addEventListener("click", _listener);
      this.switchTurn()
    },

    attackRook(targeted, moveTo) {
      let currentRook

      if (targeted.target === undefined) {
        currentRook = targeted.id
      } else {
        currentRook = targeted.target.id
      }

      const currentPawnId = document.getElementById(currentRook);

      const moveToId = document.getElementById(moveTo);

      const targetClone = currentPawnId.cloneNode()

      // Remove attackee and remove pawn from old position
      moveToId.childNodes[0].remove();
      targeted.target.remove()

      // Add the cloned pawn to the new position
      moveToId.appendChild(targetClone)

      this.switchTurn()
    },

    decideMoveRook(targeted) {
      // Get block pawn is standing on
      let standingOn
      // Get current pawn in (white/black)Rook(R/L) format
      let currentRook

      standingOn = targeted.target.parentElement.id;
      currentRook = targeted.target.id;

      // get only number of the square the pawn is standing on
      const standingOnNum = parseInt(standingOn.slice(1))

      // get the letter of the square the pawn is standing on
      const standingOnLett = standingOn.slice(0, 1);

      const currentRookColor = currentRook.match(/[^RoL]+/g)[0];

      let verticalAttackables = []
      let stuckUpPre = false
      const rookUp = document.getElementById(standingOnLett + (standingOnNum - 1))

      if (rookUp === null || (rookUp.childNodes.length > 0 && rookUp.childNodes[0].id.match(/[black|white]+/g)[0] === currentRookColor)) {
        stuckUpPre = true
      }

      const rookDown = document.getElementById(standingOnLett + (standingOnNum + 1))
      let stuckDownPre = false

      if (rookDown === null || (rookDown.childNodes.length > 0 && rookDown.childNodes[0].id.match(/[black|white]+/g)[0] === currentRookColor)) {
        stuckDownPre = true
      }


      // Check if the rook if stuck up or down to prevent it from going through the loop
      if (!stuckUpPre) {
        for (let i = 1; i < standingOnNum; i++) {
          const upPosNum = standingOnNum - i
          const upPos = standingOnLett + upPosNum

          const upPosSelected = document.getElementById(upPos)

          if (upPosSelected.childNodes.length === 0) {
            upPosSelected.classList.add("walkColor");
            const self = this
            const upPosCopy = upPos

            const _listener = function () {
              self.walkRook(targeted, upPosCopy);
            };

            upPosSelected.addEventListener("click", _listener);
          } else if (upPosSelected.childNodes[0].id.match(/[black|white]+/g)[0] !== currentRookColor) {
            verticalAttackables.push(upPosSelected)
            break
          } else {
            break
          }
        }
      }
      if (!stuckDownPre) {
        for (let i = standingOnNum + 1; i < 9; i++) {
          const downPos = standingOnLett + i


          const downPosSelected = document.getElementById(downPos)

          if (downPosSelected.childNodes.length === 0) {
            downPosSelected.classList.add("walkColor");
            const self = this
            const upPosCopy = downPos

            const _listener = function () {
              self.walkRook(targeted, upPosCopy);
            };

            downPosSelected.addEventListener("click", _listener);
          } else if (downPosSelected.childNodes[0].id.match(/[black|white]+/g)[0] !== currentRookColor) {
            verticalAttackables.push(downPosSelected)
            break
          } else {
            break
          }
        }
      }

      if (verticalAttackables !== []) {
        //Make the values only an array of numbers
        let verticalAttackablesNum = verticalAttackables.map((value) => {
          return parseInt(value.id.slice(1))
        })

        // Find out which numbers are smaller then the current number
        let smallerNums = verticalAttackablesNum.filter((value) => {
          return value < standingOnNum
        })


        // Find out which numbers are larger then the current number
        let largerNums = verticalAttackablesNum.filter((value) => {
          return value > standingOnNum
        })

        let topNum = Math.max(...smallerNums)
        let bottomNum = Math.min(...largerNums)

        if (topNum !== Number.NEGATIVE_INFINITY && topNum !== Infinity) {
          let topNumId = standingOnLett + topNum

          let topNumIdElement = document.getElementById(topNumId)
          topNumIdElement.classList.add("attackColor")
          topNumIdElement.addEventListener("click", () => {
            this.attackRook(targeted, topNumId)
          })
        }

        if (bottomNum !== Infinity) {
          let bottomNumId = standingOnLett + bottomNum
          let bottomNumIdElement = document.getElementById(bottomNumId)
          bottomNumIdElement.classList.add("attackColor")
          bottomNumIdElement.addEventListener("click", () => {
            this.attackRook(targeted, bottomNumId)
          })
        }
      }


      // Horinzontal movement
      let horizonalAttackables = []

      let stuckLeftPre = false

      const curLettIndex = this.alphabet.indexOf(standingOnLett)

      const rookLeft = this.alphabet[curLettIndex - 1] + standingOnNum
      const rookLeftElement = document.getElementById(rookLeft)

      if (curLettIndex === 0 || (rookLeftElement.childNodes.length > 0 && rookLeftElement.childNodes[0].id.match(/[black|white]+/g)[0] === currentRookColor)) {
        stuckLeftPre = true
      }

      let stuckRightPre = false
      const rookRight = this.alphabet[curLettIndex + 1] + standingOnNum

      const rookRightElement = document.getElementById(rookRight)

      if (curLettIndex === 7 || (rookRightElement.childNodes.length > 0 && rookRightElement.childNodes[0].id.match(/[black|white]+/g)[0] === currentRookColor)) {
        stuckRightPre = true
      }

      if (!stuckLeftPre) {
        for (let i = 0; i < curLettIndex; i++) {
          const leftPos = this.alphabet[curLettIndex - (i + 1)] + standingOnNum

          const leftPosSelected = document.getElementById(leftPos)


          if (leftPosSelected.childNodes.length === 0) {
            leftPosSelected.classList.add("walkColor");
            const self = this
            const leftPosCopy = leftPos

            const _listener = function () {
              self.walkRook(targeted, leftPosCopy);
            };

            leftPosSelected.addEventListener("click", _listener);
          } else if (leftPosSelected.childNodes[0].id.match(/[black|white]+/g)[0] !== currentRookColor) {
            horizonalAttackables.push(leftPosSelected)
            break
          } else {
            break
          }
        }
      }

      if (!stuckRightPre) {
        for (let i = curLettIndex + 1; i < 8; i++) {
          const rightPos = this.alphabet[i] + standingOnNum

          const rightPosSelected = document.getElementById(rightPos)

          if (rightPosSelected.childNodes.length === 0) {
            rightPosSelected.classList.add("walkColor");
            const self = this
            const rightPosCopy = rightPos

            const _listener = function () {
              self.walkRook(targeted, rightPosCopy);
            };

            rightPosSelected.addEventListener("click", _listener);
          } else if (rightPosSelected.childNodes[0].id.match(/[black|white]+/g)[0] !== currentRookColor) {
            horizonalAttackables.push(rightPosSelected)
            break
          } else {
            break
          }
        }
      }

      if (horizonalAttackables !== []) {
        // strip the first character of every value in the array and put it in another array
        let horizonalAttackablesLett = horizonalAttackables.map((square) => {
          return square.id.slice(0, 1)
        })

        // get parse the attackableLett array to get the index in the alphabet array
        let horizonalAttackablesLettIndex = horizonalAttackablesLett.map((letter) => {
          return this.alphabet.indexOf(letter)
        })

        const standingOnLettIndex = this.alphabet.indexOf(standingOnLett)

        // Find the letters closest to the rook
        // Filter out all letters larger then the current letter
        const horizonalAttackablesLettIndexSmaller = horizonalAttackablesLettIndex.filter((letter) => {
          return letter < standingOnLettIndex
        })

        let closestLetterL
        let closestLettIndexL

        if (horizonalAttackablesLettIndexSmaller.length > 0) {
          // Find index of the closest letter
          closestLettIndexL = horizonalAttackablesLettIndexSmaller.reduce(function (prev, curr) {
            return (Math.abs(curr - standingOnLettIndex) < Math.abs(prev - standingOnLettIndex) ? curr : prev);
          });

          // parse that index to get the letter
          closestLetterL = this.alphabet[closestLettIndexL]
        }

        let closestLetterR
        let closestLettIndexR
        if (horizonalAttackablesLettIndexSmaller.length !== horizonalAttackables.length) {
          // Filter out all letters smaller then the current letter
          const horizonalAttackablesLettIndexLarger = horizonalAttackablesLettIndex.filter((letter) => {
            return letter > standingOnLettIndex
          })

          // Find index of the closest letter
          closestLettIndexR = horizonalAttackablesLettIndexLarger.reduce(function (prev, curr) {
            return (Math.abs(curr - standingOnLettIndex) < Math.abs(prev - standingOnLettIndex) ? curr : prev);
          });

          // parse that index to get the letter
          closestLetterR = this.alphabet[closestLettIndexR]
        }


        if (closestLetterL !== undefined) {
          let canGoTo = document.getElementById(closestLetterL + standingOnNum)
          canGoTo.classList.remove("walkColor");
          canGoTo.classList.add("attackColor");
          const maxMoveToCopy = closestLetterL + standingOnNum
          canGoTo.addEventListener("click", () => {
            this.attackRook(targeted, maxMoveToCopy)
          })
        }

        if (closestLetterR !== undefined) {
          let canGoTo = document.getElementById(closestLetterR + standingOnNum)
          canGoTo.classList.remove("walkColor");
          canGoTo.classList.add("attackColor");
          const maxMoveToCopy = closestLetterR + standingOnNum
          canGoTo.addEventListener("click", () => {
            this.attackRook(targeted, maxMoveToCopy)
          })
        }
      }

    },


    // Brute move set
    decideMoveBrute(targeted){
      // Get block pawn is standing on
      const standingOn =targeted.target.parentElement.id;
      // Get current pawn in (white/black)Brute(R/L) format
      const currentBrute = targeted.target.id;

      // get only number of the square the pawn is standing on
      const standingOnNum = parseInt(standingOn.slice(1))

      // get the letter of the square the pawn is standing on
      const standingOnLett = standingOn.slice(0, 1);
      const standingOnLettIndex = this.alphabet.indexOf(standingOnLett)

      const currentBruteColor = currentBrute.match(/[black|white]+/)[0];

      const stuckUp = (standingOnNum-2) <= 0
      const stuckDown = (standingOnNum+2) >= 8
      const stuckLeft = (standingOnLettIndex-2) < 0
      const stuckRight = (standingOnLettIndex+2) > 7



      function addAttackables(self,firstAttack, secondAttack){
        const firstAttackSelected = document.getElementById(firstAttack)
        const secondAttackSelected = document.getElementById(secondAttack)

        console.log(firstAttack, secondAttack)

        firstAttackSelected.classList.add("attackColor")
        secondAttackSelected.classList.add("attackColor")

        const _function = function(){
          self.bruteMovement(targeted.target ,firstAttackSelected, secondAttackSelected)
        }

        firstAttackSelected.addEventListener("click", _function)
        secondAttackSelected.addEventListener("click", _function)
      }

      if(!stuckUp){
        const firstAttack =  standingOnLett+(standingOnNum-1)
        const secondAttack = standingOnLett+(standingOnNum-2)

        addAttackables(this ,firstAttack, secondAttack)
      }

      if(!stuckDown){
        const firstAttack =  standingOnLett+(standingOnNum+1)
        const secondAttack = standingOnLett+(standingOnNum+2)

        addAttackables(this, firstAttack, secondAttack)
      }

      if(!stuckLeft){
        const firstAttack = this.alphabet[standingOnLettIndex-1] + standingOnNum
        const secondAttack = this.alphabet[standingOnLettIndex-2] + standingOnNum

        addAttackables(this, firstAttack, secondAttack)
      }

      if(!stuckRight){
        const firstAttack = this.alphabet[standingOnLettIndex+1] + standingOnNum
        const secondAttack = this.alphabet[standingOnLettIndex+2] + standingOnNum

        addAttackables(this, firstAttack, secondAttack)
      }
    },

    bruteMovement(currentBrute ,firstVictim, secondVictim){

      // Haal alle kiddo's weg
      while (firstVictim.firstChild) {
        firstVictim.removeChild(firstVictim.lastChild);
      }

      while (secondVictim.firstChild) {
        secondVictim.removeChild(secondVictim.lastChild);
      }

      const bruteClone = currentBrute.cloneNode()

      // haal de brute weg
      currentBrute.remove()

      // plak hem weer terug op z'n nieuwe plek
      secondVictim.appendChild(bruteClone)

      // Haal de classes weg en wissel de beurt
      this.switchTurn()
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