#include<iostream>
#include<stdio.h>
#include<stddef.h>
#include<malloc.h>
#include<limits.h>
#include<queue>
#include<algorithm>
#include<stack>
using namespace std;



struct treenode
{
    char data;
    struct treenode *left;
    struct treenode *right;

};



struct treenode* buildtree(char arr[],int i)
{
    struct treenode *root;
    root=(struct treenode *)malloc(sizeof(struct treenode));
    root->data=arr[i];
    root->left=NULL;
    root->right=NULL;
    if(!root)
    {
        free(root);
        return NULL;
    }
    if(arr[i]=='L')
    {
        return root;
    }
    i++;
    root->left=buildtree(arr,i);
    i++;
    root->right=buildtree(arr,i);
    return root;
}

static void printtree(struct treenode *root)
{
    if(root)
    {
        printtree(root->left);

        printf("%c",root->data);
        printtree(root->right);
    }
}
int main()
{

    char arr[]= {'I','L','I','L','L'};
    printtree(buildtree(arr,0));
    return 0;
}
