given a size **S**, create a array of length **S** as the (first-level) hash table.

- Each entry of the hash table is a **List**



**List**: head -> next -> next ->....



**List Entry**

- name: string ==as the key==

- name_Next: string

- ptr2next_entry: pointer

- Shared memory opened using `name` ==stores the value== (we create this shared memory when insertion and open it on reading )

  

