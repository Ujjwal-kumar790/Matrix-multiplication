# Matrix-multiplication
#include <stdio.h>

int main()
{
    int mat1[10][10];
    int mat2[10][10];
    int mul[10][10];
    int row, col, row1, col1, sum;
    printf("Enter the row value of first matrix : ");
    scanf("%d", &row);
    printf("Enter the column value of first matrix : ");
    scanf("%d", &col);
    printf("Enter the row value of second matrix : ");
    scanf("%d", &row1);
    printf("Enter the column value of second matrix : ");
    scanf("%d", &col1);
    printf("Enter the elements of %d x %d matrix1 \n", row, col);
    for (int i = 0; i < row; i++)
    {
        for (int j = 0; j < col; j++)
        {
            printf("Enter the value of %d%d element : ", i, j);
            scanf("%d", &mat1[i][j]);
        }
    }
    printf("Enter the elements of %d x %d matrix2 \n", row1, col1);
    for (int i = 0; i < row1; i++)
    {
        for (int j = 0; j < col1; j++)
        {
            printf("Enter the value of %d%d element : ", i, j);
            scanf("%d", &mat2[i][j]);
        }
    }
    for (int i = 0; i < col; i++)
    {
        for (int j = 0; j < row1; j++)
        {
            for (int k = 0; k < row; k++)
            {
                sum += mat1[i][k] * mat2[k][j];
            }
            mul[i][j] = sum;
            sum = 0;
        }
    }
    printf("Result after multiplication");
    for (int i = 0; i < row; i++)
    {
        for (int j = 0; j < col1; j++)
        {
            printf("%d\t",mul[i][j]);
        }
        printf("\n");
    }

    return 0;
}
