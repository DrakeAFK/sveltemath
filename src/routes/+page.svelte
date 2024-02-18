<script>
  
  function appendToResult(value) {
    const result = document.getElementById("result");
    result.value += value;
  }

  function clearResult() {
    const result = document.getElementById("result");
    result.value = "";
  }

  function calculateResult() {
    try {
      document.getElementById("result").value = eval(document.getElementById("result").value)
    } catch (error) {
      document.getElementById("result").value = "Error";
    }
  }

</script>

<div class="text-center my-5">
  <h1 class="text-2xl font-mono text-white">Svelte Math</h1>
  <p class="">Math doesn't have to be hard</p>
</div>

<div class="text-center py-5">
  <input type="text" id="result" class="py-3 text-center" disabled>
</div>

<div class="text-center">
  <div class="grid-col-3 space-x-5 pb-5">
    <button class="border border-secondary rounded-xl w-[5rem]" on:click={() => appendToResult("1")}>1</button>
    <button class="border border-secondary rounded-xl w-[5rem]" on:click={() => appendToResult("2")}>2</button>
    <button class="border border-secondary rounded-xl w-[5rem]" on:click={() => appendToResult("3")}>3</button>
  </div>
  <div class="grid-col-3 space-x-5 pb-5">
    <button class="border border-secondary rounded-xl w-[5rem]" on:click={() => appendToResult("4")}>4</button>
    <button class="border border-secondary rounded-xl w-[5rem]" on:click={() => appendToResult("5")}>5</button>
    <button class="border border-secondary rounded-xl w-[5rem]" on:click={() => appendToResult("6")}>6</button>
  </div>
  <div class="grid-col-3 space-x-5 pb-5">
    <button class="border border-secondary rounded-xl w-[5rem]" on:click={() => appendToResult("7")}>7</button>
    <button class="border border-secondary rounded-xl w-[5rem]" on:click={() => appendToResult("8")}>8</button>
    <button class="border border-secondary rounded-xl w-[5rem]" on:click={() => appendToResult("9")}>9</button>
  </div>
  <div class="grid-col-3 space-x-5 pb-5">
    <button class="border border-secondary rounded-xl w-[5rem]" on:click={() => appendToResult("0")}>0</button>
  </div>
  <div class="grid-col-3 space-x-5 pb-5">
    <button class="border border-primary rounded-xl w-[5rem]" on:click={() => appendToResult("+")}>+</button>
    <button class="border border-primary rounded-xl w-[5rem]" on:click={() => appendToResult("-")}>-</button>
    <button class="border border-primary rounded-xl w-[5rem]" on:click={() => appendToResult("*")}>*</button>
    <button class="border border-primary rounded-xl w-[5rem]" on:click={() => appendToResult("/")}>/</button>
  </div>
  <div class="grid-col-3 space-x-5 pb-5">
    <button class="border border-success rounded-xl w-[5rem]" on:click={() => clearResult()}>Clear</button>
    <button class="border border-success rounded-xl w-[5rem]" on:click={() => calculateResult()}>=</button>
  </div>
</div>