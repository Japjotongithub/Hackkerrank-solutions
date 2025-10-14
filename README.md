\# Hackkerrank-solutions
Solutions for the hackerrank problems i have solved

int* dynamicArray(int n, int queries_rows, int queries_columns, int** queries, int* result_count) {
    // Allocate dynamic arrays for storing sequences
    int **arr = (int **)malloc(n * sizeof(int *));
    int *sizes = (int *)calloc(n, sizeof(int));  // To track sizes of each sequence

    
   // Allocate initial space for each sequence (start with small size)
    for (int i = 0; i < n; i++) {
        arr[i] = (int *)malloc(1 * sizeof(int));
    }

// Allocate result array (worst case: every query is type 2)
    int *result = (int *)malloc(queries_rows * sizeof(int));
    int res_index = 0;

