#include <stdio.h>
#include <stdlib.h>
struct Node {
    int value;
    struct Node *left, *right;
};
struct Node* newNode(int value) {
    struct Node* node = malloc(sizeof(struct Node));
    node->value = value;
    node->left = node->right = NULL;
    return node;
}
void preorder(struct Node* root) {
    if (root) {
        printf("%d ", root->value);
        preorder(root->left);
        preorder(root->right);
    }
}
void inorder(struct Node* root) {
    if (root) {
        inorder(root->left);
        printf("%d ", root->value);
        inorder(root->right);
    }
}
void postorder(struct Node* root) {
    if (root) {
        postorder(root->left);
        postorder(root->right);
        printf("%d ", root->value);
    }
}
int main() {
    struct Node* root = newNode(1);
    root->left = newNode(2);
    root->right = newNode(3);
    root->left->left = newNode(4);
    root->left->right = newNode(5);
    root->right->left = newNode(6);
    root->right->right = newNode(7);
    
    printf("\nInorder: ");
    inorder(root);
    printf("Preorder: ");
    preorder(root);
    printf("\nPostorder: ");
    postorder(root);
    printf("\n");

    return 0;
}
