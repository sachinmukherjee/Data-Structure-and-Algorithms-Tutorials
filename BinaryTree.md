# Binary Trees

It is a non linear data structure each points to a number of nodes

![image](https://www.cs.cmu.edu/~adamchik/15-121/lectures/Trees/pix/tree1.bmp)

### Properties

* There can be atmost one root in a binary Trees
* An edge refers to link between patent and child
* A node with no child is a leaf node
* Child of same parent is called is siblings
* Ancestor means Parent
* Descender means Child
* Depth of tree is length of path from root to the node
* Height of binary tree is the length of the path from deepest node to the root
* Size of binary tree is number of child it has including itself


### Types of Binary Trees

<b>Strict Binary Tree </b> If each node has exactly two children or no child.

<b>Full Binary Tree </b> If each node has exactly two children and all leaf nodes are at same level.

<b>Full Binary Tree</b> If all leaf nodes are at height h or h-1


### Tree Traversal

Visiting nodes in a particular order is called tree transversal

* Pre Order <b>DLR</b>
* In Order <b>LDR</b>
* Post Order <b>LRD</b>
* Level Order <b>Level Wise</b> Bredth First search


## Pre Order Transversal

In this transversal method first root is processed and then its left subtree and then its right subtree. Therefore order of visit is DLR

<i><b>Recursive</b></i>

    void preOrder(Node root)
    {
      if(root==null)
         return;
      else
      {
        Print(root.data)
        preOrder(root.leftchild);
        preOrder(root.rightchild);
      }
    }

<i><b>Iterative</b><i>
    void preOrder()
    {
      Stack thestack = new Stack();
      while(true)
      {
        while(root!=null)
        {
          Print(root.data)
          Push(root);
          root = root.leftchild;

        }
        if(thestack.isEmpty)
           break;
        root = Pop();
        root = root.rightchild;
      }
    }
It simply displays the root and then goes on to its leftchild after displaying. Then when it reaches the null node it pops the last item inserted and goes to its right child if available.

## Inorder Transversal

In this transversal method first leftsub tree is processed then displays it data and then goes to right subtree. Thats why LDR

<i><b>Recursive</b></i>

    void inOrder(Node root)
    {
      if(root==null)
         return;
      else
      {
        inOrder(root.leftchild);
        Print(root.data);
        inOrder(root.rightchild);
      }
    }


<i><b>Iterative</b><i>

    void inOrder()
    {
      Stack thestack = new Stack();
      while(true)
      {
        while(root!=null)
        {
          Push(root);
          root = root.leftchild;
        }
        if(!isEmpty)
           break;
        root = Pop();
        Print(root.data);
        root = root.rightchild;
      }
    }

It first goes to leftmost child then displays it and search for its rightchild it available then it goes to rightchild else move towards the root.


## Post Order Transversal

It first goes to Leftmost child the its rightchild if available then prints its data.Thats why it is LRD

<i><b> Recursive </b></i>

    void postOrder(Node root)
    {
      if(root==null)
         return;
      else
      {
        postOrder(root.leftchild);
        postOrder(root.rightchild);
        Print(root.data);
      }
    }


<i><b> Iterative </b></i>

    void postOrder()
    {
      Stack thestack = new Stack();
      while(true)
      {
        while(root!=null)
        {
          root = root.rightchild;
        }
      }
      if(!isEmpty)
         break;
      root = Peek();
      if(root.rightchild)
         root = root.rightchild;
    }
