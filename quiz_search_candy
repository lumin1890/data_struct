#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#define MAX_NUMBER 100

int main() {
	int num_of_test;
	scanf("%d", &num_of_test);
	for (int i = 0; i < num_of_test; i++) {
		int num_of_candy;
		int request;

		scanf("%d %d", &num_of_candy, &request);

		int heights[MAX_NUMBER];
		int max_height = 0;
		for (int j = 0; j < num_of_candy; j++) {
			scanf("%d", &heights[j]);
			if (heights[j] > max_height) {
				max_height = heights[j];
			}
		}

		int low = 0;
		int high = max_height;
		int result = 0;
		while (low <= high) {
			int mid = (low + high) / 2;
			long total = 0;

			for (int i = 0; i < num_of_candy; i++) {
				if (heights[i] > mid) {
					total += heights[i] - mid;
				}
			}
			if (total >= request) {
				result = mid;
				low = mid + 1;
			}
			else {
				high = mid - 1;
			}
		}
		printf("%d\n", result);
	}
	return 0;
}
