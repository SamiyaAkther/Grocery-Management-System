#include<stdio.h>
#include<string.h>

int main()
{
    char name[50];
    char phone_number[15];
    int customer_id;

    int total = 0;
    int choice, quantity, sub_choice;

    printf("------------------\n");
    printf("Billing System\n");
    printf("------------------\n");
    printf("Customer Details\n\n");

    printf("Customer Name: ");
    fgets(name, sizeof(name), stdin);
    printf("Phone Number: ");
    fgets(phone_number, sizeof(phone_number), stdin);
    printf("Customer ID: ");
    scanf("%d", &customer_id);

    printf("--------------\n");

    while (1)
    {
        printf("Choose a Category:\n");
        printf("1. Cosmetics\n");
        printf("2. Groceries\n");
        printf("3. Beverages\n");
        printf("4. Exit and Show Bill\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice)
        {
        case 1:
            printf("Cosmetics:\n");
            printf("1. Body Soap (70tk)\n");
            printf("2. Hair Cream (290tk)\n");
            printf("3. Shampoo (310tk)\n");
            printf("4. Hair Spray (550tk)\n");
            printf("5. Body Spray (440tk)\n");
            printf("Choose an item: ");
            scanf("%d", &sub_choice);

            printf("Enter quantity: ");
            scanf("%d", &quantity);
            if (quantity <= 0)
            {
                printf("Invalid quantity!\n");
                break;
            }

            switch (sub_choice)
            {
            case 1:
                total += quantity * 70;
                break;
            case 2:
                total += quantity * 290;
                break;
            case 3:
                total += quantity * 310;
                break;
            case 4:
                total += quantity * 550;
                break;
            case 5:
                total += quantity * 440;
                break;
            default:
                printf("Invalid item choice!\n");
                break;
            }
            break;

        case 2:
            printf("Groceries:\n");
            printf("1. Sugar (40tk)\n");
            printf("2. Tea (90tk)\n");
            printf("3. Coffee (230tk)\n");
            printf("4. Rice (50tk)\n");
            printf("5. Wheat (110tk)\n");
            printf("Choose an item: ");
            scanf("%d", &sub_choice);

            printf("Enter quantity: ");
            scanf("%d", &quantity);
            if (quantity <= 0)
            {
                printf("Invalid quantity!\n");
                break;
            }

            switch (sub_choice)
            {
            case 1:
                total += quantity * 40;
                break;
            case 2:
                total += quantity * 90;
                break;
            case 3:
                total += quantity * 230;
                break;
            case 4:
                total += quantity * 50;
                break;
            case 5:
                total += quantity * 110;
                break;
            default:
                printf("Invalid item choice!\n");
                break;
            }
            break;

        case 3:
            printf("Beverages:\n");
            printf("1. Pepsi (20tk)\n");
            printf("2. CocaCola (25tk)\n");
            printf("3. 7 Up (20tk)\n");
            printf("4. Sprite (35tk)\n");
            printf("5. Mojo (20tk)\n");
            printf("Choose an item: ");
            scanf("%d", &sub_choice);

            printf("Enter quantity: ");
            scanf("%d", &quantity);
            if (quantity <= 0)
            {
                printf("Invalid quantity!\n");
                break;
            }

            switch (sub_choice)
            {
            case 1:
                total += quantity * 20;
                break;
            case 2:
                total += quantity * 25;
                break;
            case 3:
                total += quantity * 20;
                break;
            case 4:
                total += quantity * 35;
                break;
            case 5:
                total += quantity * 20;
                break;
            default:
                printf("Invalid item choice!\n");
                break;
            }
            break;

        case 4:
            printf("--------------\n");
            printf("Customer Name: %s\n", name);
            printf("Phone Number: %s\n", phone_number);
            printf("Customer ID: %d\n", customer_id);
            printf("Total Amount: %d tk\n", total);
            printf("--------------\n");
            return 0;

        default:
            printf("Invalid category choice!\n");
            break;
        }
    }

    return 0;
}
