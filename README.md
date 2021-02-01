# Linkedlist_reverse
To reverse a linkedlist.
void reversePrint(SinglyLinkedListNode* head) {
SinglyLinkedListNode *prevnode,*curnode,*nextnode,*ptr;
prevnode=0;
curnode=nextnode=head;
while(nextnode!=0)
{
    nextnode=nextnode->next;
    curnode->next=prevnode;
    prevnode=curnode;
    curnode=nextnode;
}
head=prevnode;
ptr=head;
while(ptr->next!=0)
{
    cout<<ptr->data<<"\n";
    ptr=ptr->next;
}
cout<<ptr->data<<"\n";
}
