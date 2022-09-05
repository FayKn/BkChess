<template>
  <div class="flex flex-row">
    <!--row 1 -->
    <div>
      <div class="boardItemSize bg-blue-400">
        <img ref="blackRookL" src="public/pieces/rook.svg"/>
      </div>
      <div class="boardItemSize bg-blue-800">
        <img ref="blackPawn1" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div class="boardItemSize bg-blue-400">
        3
      </div>
      <div class="boardItemSize bg-blue-800">
        4
      </div>
      <div class="boardItemSize bg-blue-400">
        5
      </div>
      <div class="boardItemSize bg-blue-800">
        6
      </div>
      <div class="boardItemSize bg-blue-400">
        <img ref="whitePawn1" class="invert w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div class="boardItemSize bg-blue-800">
        <img ref="whiteRookL" class="invert" src="public/pieces/rook.svg"/>
      </div>
    </div>
    <!--row 2 -->
    <div>
      <div class="boardItemSize bg-blue-800">
        1
      </div>
      <div class="boardItemSize bg-blue-400">
        <img ref="blackPawn2" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div class="boardItemSize bg-blue-800">
        3
      </div>
      <div class="boardItemSize bg-blue-400">
        4
      </div>
      <div class="boardItemSize bg-blue-800">
        5
      </div>
      <div class="boardItemSize bg-blue-400">
        6
      </div>
      <div class="boardItemSize bg-blue-800">
        <img ref="whitePawn1" class="invert w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div class="boardItemSize bg-blue-400">
        8
      </div>
    </div>
    <!--row 3 -->
    <div>
      <div class="boardItemSize bg-blue-400">
        1
      </div>
      <div class="boardItemSize bg-blue-800">
        <img ref="blackPawn2" class="w-[70%]" src="public/pieces/pawn.svg"/>
      </div>
      <div class="boardItemSize bg-blue-400">
        3
      </div>
      <div class="boardItemSize bg-blue-800">
        4
      </div>
      <div class="boardItemSize bg-blue-400">
        5
      </div>
      <div class="boardItemSize bg-blue-800">
        6
      </div>
      <div class="boardItemSize bg-blue-400">
        7
      </div>
      <div class="boardItemSize bg-blue-800">
        8
      </div>
    </div>
    <!--row 4 -->
    <div>
      <div class="boardItemSize bg-blue-800">
        1
      </div>
      <div class="boardItemSize bg-blue-400">
        2
      </div>
      <div class="boardItemSize bg-blue-800">
        3
      </div>
      <div class="boardItemSize bg-blue-400">
        4
      </div>
      <div class="boardItemSize bg-blue-800">
        5
      </div>
      <div class="boardItemSize bg-blue-400">
        6
      </div>
      <div class="boardItemSize bg-blue-800">
        7
      </div>
      <div class="boardItemSize bg-blue-400">
        8
      </div>
    </div>
    <!--row 5 -->
    <div>
      <div class="boardItemSize bg-blue-400">
        1
      </div>
      <div class="boardItemSize bg-blue-800">
        2
      </div>
      <div class="boardItemSize bg-blue-400">
        3
      </div>
      <div class="boardItemSize bg-blue-800">
        4
      </div>
      <div class="boardItemSize bg-blue-400">
        5
      </div>
      <div class="boardItemSize bg-blue-800">
        6
      </div>
      <div class="boardItemSize bg-blue-400">
        7
      </div>
      <div class="boardItemSize bg-blue-800">
        8
      </div>
    </div>
    <!--row 6 -->
    <div>
      <div class="boardItemSize bg-blue-800">
        1
      </div>
      <div class="boardItemSize bg-blue-400">
        2
      </div>
      <div class="boardItemSize bg-blue-800">
        3
      </div>
      <div class="boardItemSize bg-blue-400">
        4
      </div>
      <div class="boardItemSize bg-blue-800">
        5
      </div>
      <div class="boardItemSize bg-blue-400">
        6
      </div>
      <div class="boardItemSize bg-blue-800">
        7
      </div>
      <div class="boardItemSize bg-blue-400">
        8
      </div>
    </div>
    <!--row 7 -->
    <div>
      <div class="boardItemSize bg-blue-400">
        1
      </div>
      <div class="boardItemSize bg-blue-800">
        2
      </div>
      <div class="boardItemSize bg-blue-400">
        3
      </div>
      <div class="boardItemSize bg-blue-800">
        4
      </div>
      <div class="boardItemSize bg-blue-400">
        5
      </div>
      <div class="boardItemSize bg-blue-800">
        6
      </div>
      <div class="boardItemSize bg-blue-400">
        7
      </div>
      <div class="boardItemSize bg-blue-800">
        8
      </div>
    </div>
    <!--row 8 -->
    <div>
      <div class="boardItemSize bg-blue-800">
        <img ref="blackRookR" src="public/pieces/rook.svg"/>
      </div>
      <div class="boardItemSize bg-blue-400">
        2
      </div>
      <div class="boardItemSize bg-blue-800">
        3
      </div>
      <div class="boardItemSize bg-blue-400">
        4
      </div>
      <div class="boardItemSize bg-blue-800">
        5
      </div>
      <div class="boardItemSize bg-blue-400">
        6
      </div>
      <div class="boardItemSize bg-blue-800">
        7
      </div>
      <div class="boardItemSize bg-blue-400">
        <img ref="whiteRookL" class="invert" src="public/pieces/rook.svg"/>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "index"
}
</script>

<style>
.boardItemSize {
  @apply w-[100px] h-[100px] flex justify-center content-center
}
</style>