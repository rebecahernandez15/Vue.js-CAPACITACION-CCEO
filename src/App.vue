<script setup>
import { ref, computed } from 'vue'; // 1. Importamos computed

const name = "Vue dinámico";

const counter = ref(0);
const increment = () => {

</template>

<style>
h1 {
  color: red;
}
.positive {
  color: green;
}
.negative {
  color: red;
}
.zero {
  color: peru;
}
</style>