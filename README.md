# Ex-7-Write-a-java-program-to-insert-an-element-into-array
```
import java.util.Scanner;

public class InsertElementIntoArray {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the size of the array: ");
        int size = scanner.nextInt();
        int[] array = new int[size];
        System.out.println("Enter the elements of the array:");
        for (int i = 0; i < size; i++) {
            array[i] = scanner.nextInt();
        }
        System.out.print("Enter the element to insert: ");
        int elementToInsert = scanner.nextInt();
        System.out.print("Enter the position to insert (1 to " + (size + 1) + "): ");
        int position = scanner.nextInt();

        if (position < 1 || position > size + 1) {
            System.out.println("Invalid position. Element cannot be inserted.");
        } else {

            for (int i = size - 1; i >= position - 1; i--) {
                array[i + 1] = array[i];
            }
            array[position - 1] = elementToInsert;
System.out.println("Array after inserting the element:");
for (int i = 0; i < size + 1; i++) {
    System.out.print(array[i] + " ");
}

        }

        scanner.close();
    }
}

```
#Output
![Screenshot (71)](https://github.com/21002624/Ex-7-Write-a-java-program-to-insert-an-element-into-array/assets/113762183/4982aaa9-84f1-42b9-9955-169d4aeb73d9)
