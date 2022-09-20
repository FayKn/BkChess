<template>
  <div id="wrapper">
    <h1 class="text-white">{{ turn }}</h1>
    <div id="board">
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
          </div>
          <div id="a8" class="boardItemSize bg-blue-800">
            <img @click="decideMoveRook($event)" id="whiteRookL" class="invert" src="pieces/rook.svg"/>
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
            <img @click="decideMovePawn($event)" id="blackPawn3" class="w-[70%]" src="pieces/pawn.svg"/>
          </div>
          <div id="b5" class="boardItemSize bg-blue-800">

          </div>
          <div id="b6" class="boardItemSize bg-blue-400">

          </div>
          <div id="b7" class="boardItemSize bg-blue-800">
            <img @click="decideMovePawn($event)" id="whitePawn2" class="invert w-[70%]" src="pieces/pawn.svg"/>
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
    switchTurn() {
      if (this.turn === "white") {
        // TODO: change back to black
        this.turn = "white"
      } else {
        this.turn = "white"
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
        } else {
          console.log("no " + this.turn + " pawn " + i)
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
    },

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

      let loopProgressionId
      let topMax
      let bottomMax

      let verticalAttackables = []
      for (let i = 1; i < 9; i++) {
        let topEmpty = false
        let bottomEmpty = false
        let canGoTo = document.getElementById(standingOnLett + i)
        loopProgressionId = standingOnLett + i

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
        if (canGoToPrev !== null) {
          if (canGoToPrev.childNodes.length !== 0) {
            if (canGoToPrev.childNodes[0] !== document.getElementById(currentRook)) {
              const goToColor = canGoToPrev.childNodes[0].id.match(/[black|white]+/g)[0]
              if (goToColor === currentRookColor) {
                stuckBack = true
              }
            }
          }
        }


        if (stuckFront && stuckBack) {
          break
        }

        if (canGoTo.childNodes.length > 0) {
          if (canGoTo.childNodes[0] !== document.getElementById(currentRook)) {
            if (i < standingOnNum) {
              topMax = loopProgressionId
            } else {
              bottomMax = loopProgressionId
            }
          }
        }

        if (canGoTo.childNodes[0] !== document.getElementById(currentRook) && canGoTo.childNodes.length === 0) {
          canGoTo.classList.add("walkColor");

          const self = this
          const maxMoveToCopy = loopProgressionId

          const _listener = function () {
            self.walkRook(targeted, maxMoveToCopy);
          };

          canGoTo.addEventListener("click", _listener);
        }

        if ((topMax !== undefined || bottomMax !== undefined) && canGoTo.childNodes.length > 0) {
          const goToColor = canGoTo.childNodes[0].id.match(/[black|white]+/g)[0]
          canGoTo.classList.remove("walkColor");
          if (goToColor !== currentRookColor) {
            verticalAttackables.push(canGoTo.id)
/*
            canGoTo.classList.add("attackColor");
            const maxMoveToCopy = loopProgressionId
            canGoTo.addEventListener("click", () => {
              this.attackRook(targeted, maxMoveToCopy)
            })*/
          }
        }
      }


      if(verticalAttackables !== []){
        //Make the values only an array of numbers
        let verticalAttackablesNum = verticalAttackables.map((value) => {
          return parseInt(value.slice(1))
        })

        console.log("All nums",verticalAttackablesNum)

        // Find out which numbers are smaller then the current number
        let smallerNums = verticalAttackablesNum.filter((value) => {
          return value < standingOnNum
        })

        console.log("Smaller: ", smallerNums)


        // Find out which numbers are larger then the current number
        let largerNums = verticalAttackablesNum.filter((value) => {
          return value > standingOnNum
        })

        console.log("Larger: ", largerNums)

        let topNum = Math.max(...smallerNums)
        let bottomNum = Math.min(...largerNums)

        console.log("Top num: ", topNum)
        console.log("Bottom num: ", bottomNum)

        if(topNum !== Infinity){
          let topNumId = standingOnLett + topNum

          console.log(topNumId)
          let topNumIdElement = document.getElementById(topNumId)
          topNumIdElement.classList.add("attackColor")
          topNumIdElement.addEventListener("click", () => {
            this.attackRook(targeted, topNumId)
          })
        }

        if(bottomNum !== Infinity){
          let bottomNumId = standingOnLett + bottomNum
          let bottomNumIdElement = document.getElementById(bottomNumId)
          bottomNumIdElement.classList.add("attackColor")
          bottomNumIdElement.addEventListener("click", () => {
            this.attackRook(targeted, bottomNumId)
          })
        }
        

      }


      // Horinzontal movement
      let leftMax
      let rightMax

      let horizonalAttackables = []
      for (let i = 0; i < 8; i++) {
        let canGoTo = document.getElementById(this.alphabet[i] + standingOnNum)
        loopProgressionId = this.alphabet[i] + standingOnNum

        // Check if the square is empty and not own suqare
        if (canGoTo.childNodes[0] !== document.getElementById(currentRook) && canGoTo.childNodes.length === 0) {
          // Add the color to walk to the square
          canGoTo.classList.add("walkColor");
          // Make a copy of the square id to use in function because it gets redefined every loop and this works
          const maxMoveToCopy = loopProgressionId

          const self = this

          const _handler = function () {
            self.walkRook(targeted, maxMoveToCopy);
          };

          // Add event listener to the square
          canGoTo.addEventListener("click", _handler);

        }
        // Make sure the square is not empty
        if (canGoTo.childNodes.length !== 0) {
          const goToColor = canGoTo.childNodes[0].id.match(/[black|white]+/g)[0]
          // Check if the square is not own team (and by extent self)
          if (goToColor !== currentRookColor) {
            horizonalAttackables.push(canGoTo)
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

        // TODO: do check similar to ln.836

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


        // Remove the walks after the attackable rooks
        if ((closestLettIndexR + 1) < this.alphabet.length) {
          const timesToLoop = this.alphabet.length - (closestLettIndexR + 1)
          for (let i = 0; i < timesToLoop; i++) {
            let removeable = document.getElementById(this.alphabet[closestLettIndexR + i + 1] + standingOnNum)
            removeable.classList.remove("walkColor");

            // Clone node and replace to remove event listener
            const removeableClone = removeable.cloneNode(true)
            removeable.parentNode.replaceChild(removeableClone, removeable)
          }
        }

        // Remove the walks after the attackable rooks
        if ((closestLettIndexL - 1) < this.alphabet.length) {
          const timesToLoop = this.alphabet.length - (closestLettIndexL + 1)
          for (let i = 0; i < timesToLoop; i++) {
            let removeable = document.getElementById(this.alphabet[closestLettIndexL - i - 1] + standingOnNum)
            removeable.classList.remove("walkColor");

            // Clone node and replace to remove event listener
            const removeableClone = removeable.cloneNode(true)
            removeable.parentNode.replaceChild(removeableClone, removeable)
          }
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