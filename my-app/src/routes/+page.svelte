<script>
	let current = ''; // 現在の入力
	let result = '';  // 計算結果
  
	// 数字や演算子を押したとき
	function append(char) {
	  current += char;
	}
  
	// 計算する
	function calculate() {
	  try {
		result = eval(current); // 安全性に気をつけて使用
	  } catch (error) {
		result = 'Error';
	  }
	}
  
	// クリア
	function clearAll() {
	  current = '';
	  result = '';
	}

	let show = false;
	function isEqual(){
		show = !show;
	}

	function delEqual(){
		show = false;
	}
  </script>
  
  <style>
	.calculator {
	  width: 200px;
	  margin: 0 auto;
	}
  
	.display {
	  width: 100%;
	  height: 50px;
	  margin-bottom: 10px;
	  background-color: #f0f0f0;
	  font-size: 24px;
	  text-align: right;
	  padding: 10px;
	  box-sizing: border-box;
	  border: 1px solid #ccc;
	  display :flex;
	}
  
	.buttons {
	  display: grid;
	  grid-template-columns: repeat(4, 1fr);
	  grid-gap: 10px;
	}
  
	button {
	  width: 100%;
	  height: 50px;
	  font-size: 18px;
	}
  
	button.clear {
	  grid-column: span 2;
	  background-color: #f44336;
	  color: white;
	}
  
	button.equals {
	  grid-column: span 2;
	  background-color: #4CAF50;
	  color: white;
	}

	.transp{
		opacity: 0;
	}
  </style>
  
  <div class="calculator">
	<!-- ディスプレイ部分 -->
	<div class="display">
	  <div>{current || 0}</div>
	  {#if show}
	  <div>=</div>
	  {/if}
	  <div>{result}</div>
	</div>
  
	<!-- ボタン部分 -->
	<div class="buttons">
	  <button on:click={() => append('1')}>1</button>
	  <button on:click={() => append('2')}>2</button>
	  <button on:click={() => append('3')}>3</button>
	  <button on:click={() => append('+')}>+</button>
  
	  <button on:click={() => append('4')}>4</button>
	  <button on:click={() => append('5')}>5</button>
	  <button on:click={() => append('6')}>6</button>
	  <button on:click={() => append('-')}>-</button>
  
	  <button on:click={() => append('7')}>7</button>
	  <button on:click={() => append('8')}>8</button>
	  <button on:click={() => append('9')}>9</button>
	  <button on:click={() => append('*')}>×</button>
  
	  <button on:click={() => {clearAll(); delEqual();} } class="clear">C</button>
	  <button on:click={() => append('0')}>0</button>
	  <button on:click={() => append('/')}>÷</button>
	  <button on:click={() => { calculate(); isEqual(); }} class="equals">=</button>

	</div>
  </div>
  

