#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>
#include <sys/wait.h>

#define infinite 1

int main(int arg, char **argv)
{

    char arr[1000];
    while (infinite)
    {
        printf("MyShell > ");
        fgets(arr, 1000, stdin);
        

        if (strstr(&arr[0], "l") && strstr(&arr[1], "s"))
        {
            if (fork() > 0)
            {
                wait(NULL);
            }
            else
            {
                char *list[] = {"ls", NULL};
                execvp("ls", list);
                exit(1);
            }
        }

        else if (strstr(&arr[0], "c") && strstr(&arr[1], "d"))
        {
            if (fork() > 0)
            {
                wait(NULL);
            }
            else
            {
                chdir(getenv("HOME"));
            }
        }

        else if (strstr(&arr[0], "p") && strstr(&arr[1], "w") && strstr(&arr[2], "d"))
        {
            if (fork() > 0)
            {
                wait(NULL);
            }
            else
            {
                char *list[] = {"pwd", NULL};
                execvp("pwd", list);
                exit(1);
            }
        }

        else if (strstr(&arr[0], "d") && strstr(&arr[1], "a") && strstr(&arr[2], "t") && strstr(&arr[3], "e"))
        {
            if (fork() > 0)
            {
                wait(NULL);
            }
            else
            {
                char *list[] = {"date", NULL};
                execvp("date", list);
                exit(1);
            }
        }

        else if (strstr(&arr[0], "c") && strstr(&arr[1], "a") && strstr(&arr[2], "t"))
        {
            if (fork() > 0)
            {
                wait(NULL);
            }
            else
            {
                char *list[] = {"cat", NULL};
                execvp("cat", list);
                exit(1);
            }
        }

        else if (arr[0] == '\0' || arr[0] == '\n')
        {
        }

        else if (strstr(&arr[0], "e") && strstr(&arr[1], "x") && strstr(&arr[2], "i") && strstr(&arr[3], "t"))
        {

            exit(0);
        }

        else
        {

            printf("invalid command\n");
        }
    }

    return 0;
}
