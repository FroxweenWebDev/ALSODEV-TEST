<template>
	<div class="part">
		<div class="part__title">Part 1</div>
		<div class="subtitle">
			1.1
		</div>
		<div class="result">
			<div class="task">
				<span class="cols">
					Написать функцию которая: учитывает массив несортированных чисел и определяет являются ли числа
					в массиве
					последовательными, например :
				</span>
				<br>
				<br>
				<span class="cols">
					<b><i>a</i></b>. Если массив равен [5, 2, 3, 1, 4] тогда функция должна вернуть true потому что массив содержит
					последовательные
					числа от 1 до 5 (1,2,3,4,5)
				</span>
				<br>
				<task-one :array="[5, 2, 3, 1, 4]" /><br>
				<span class="cols">
					<b><i>b</i></b>. Если массив равен [34, 23, 52, 12, 3] тогда функция должна возвращать значения false потому что
					элементы не
					являются последовательными.
				</span>
				<br>
				<task-one :array="[34, 23, 52, 12, 3]" /><br>
				<span class="cols">
					<b><i>c</i></b>. Если массив равен [7, 6, 5, 5, 3, 4] тогда функция должна возвращать значения false, потому что
					5
					и 5 не являются
					последовательными
				</span>
				<br>
				<task-one :array="[7, 6, 5, 5, 3, 4]" />
				<div class="subtitle">
					1.2
				</div>
				<span class="cols">Необходимо реализовать функцию, которая принимает этот массив в качестве аргумента и возвращает
					новый массив,
					содержащий только уникальные элементы. Новый массив должен быть отсортирован по возрастанию.</span>

				<span class="cols">
					Примеры: <br>

					Входной массив: [1, 3, 2, 2, 4, 3, 5, 6, 5] Выходной массив: [1, 2, 3, 4, 5, 6] <br>

					Входной массив: [9, 9, 9, 9, 9] Выходной массив: [9] <br>

					Входной массив: [1, 2, 3, 4, 5] Выходной массив: [1, 2, 3, 4, 5] <br>
				</span>
				<br>
				<div class="result">
					<task-two />
				</div>
				<div class="subtitle">
					1.3
				</div>
				<div class="result">
					<task-three />
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import TaskOne from "@/components/TaskOne.vue";
import TaskTwo from '@/components/TaskTwo.vue';
import TaskThree from '@/components/TaskThree.vue';

export default {
	name: 'HomeView',
	components: {
		TaskOne,
		TaskTwo,
		TaskThree
	}
}
</script>
