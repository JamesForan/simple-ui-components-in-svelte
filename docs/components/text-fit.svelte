<h2>Text-fit</h2>
<input type="text" bind:value="{textFitText}">
<div class="text-fit-div" style="width: 100px"><TextFit>{textFitText}</TextFit></div>
<div class="text-fit-div" style="width: 200px"><TextFit>{textFitText}</TextFit></div>
<div class="text-fit-div" style="width: 300px"><TextFit>{textFitText}</TextFit></div>



<script>
import { TextFit } from '../../src';
let textFitText = 'My Lovely Text';

</script>
