#include <iostream>
using namespace std;

struct node
{
    int data;
    node *ptr;
};
class Queue
{
private:
    node *next, *rear, *front, *temp;
    int count;

public:
    Queue()
    {
        next = rear = front = NULL;
        count = 0;
    }
    void display()
    {
        if (rear == NULL)
        {
            cout << "antrian kosong\n";
        }
        else
        {
            next = front;
            while (next != NULL)
            {
                cout << "| " << next->data << " |";
                next = next->ptr;
            }
        }
    }
    void Enqueue(int x)
    {
        if (rear == NULL)
        {
            next = new node;
            next->data = x;
            front = next;
            rear = next;
            rear->ptr = NULL;
            count++;
        }
        else
        {
            next = new node;
            next->data = x;
            rear->ptr = next;
            rear = next;
            rear->ptr = NULL;
            count++;
        }
    }
    void Dequeue()
    {
        if (isEmpty())
        {
            cout << "antrian kosong\n";
        }
		else if (front == rear)
		{
			front = rear = NULL;	
		}
        else
        {
            temp = front;
            front = front->ptr;
            delete (temp);
            cout << "antrian berhasil di tambahkan.\n";
            count--;
        }
    }
    void peek()
    {
        if (rear == NULL)
        {
            cout << "antrian kosong\n";
        }
        else
        {
            cout << "antrian pertama:\n";
            cout << rear->data << endl;
        }
    }
    bool isEmpty()
    {
        if (rear == NULL)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
};
int main()
{
    Queue obj;
    int data, op=-1;
    
    while (op != 7)
    {
        cout << "\n=====================================================\n";
        cout << "IMPLEMENTASI QUEUE MENGGUNAKAN LINKEDLIST\n";
        cout << "=====================================================\n";
        cout << "1. masukkan antrian\n2. hapus antrian\n3. display\n4. exit\n";
        cin >> op;
        system("CLS");
        switch (op)
        {
        case 1:
            cout << "masukkan angka kedalam antrian:\n";
            cin >> data;
            obj.Enqueue(data);
            obj.display();
            cout << "\ndata antrian berhasil di tambahkan.\n";
            break;

        case 2:
            obj.Dequeue();
            obj.display();
            break;

        case 3:
            cout << "antrian:\n";
            obj.display();
            break;

        case 4:
            obj.peek();
            break;

        case 5:
            if (obj.isEmpty())
            {
                cout << "antrian kosong\n";
            }
            else
            {
                cout << "antrian tidak kosong\n";
            }
            break;

        case 6:
            system("CLS");
            break;

        default:
            cout << " masukin angka yang bener.\n";
            break;
        }
    }
    return 0;
}
