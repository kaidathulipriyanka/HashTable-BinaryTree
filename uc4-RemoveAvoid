using System;
using System.Collections.Generic;

namespace HashTableAndTree
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Welcome to Hash Table and Tree Program...");

            string paragraph = "Paranoids are not paranoid because they are paranoid but because they keep putting themselves deliberately into paranoid avoidable situations";
            Dictionary<string, MyLinkedListNode<string, int>> hashTable = new Dictionary<string, MyLinkedListNode<string, int>>();

            string[] words = paragraph.Split(' ');

            foreach (string word in words)
            {
                string key = word.ToLower();

                if (key == "avoidable")
                {
                    continue; // Skip the word "avoidable"
                }

                if (hashTable.ContainsKey(key))
                {
                    MyLinkedListNode<string, int> node = hashTable[key];
                    node.Value++;
                }
                else
                {
                    MyLinkedListNode<string, int> newNode = new MyLinkedListNode<string, int>(key, 1);
                    hashTable[key] = newNode;
                }
            }

            Console.WriteLine("Word Frequency:");
            foreach (var data in hashTable.Values)
            {
                Console.WriteLine($"{data.Key}: {data.Value}");
            }
        }
    }

    public class MyLinkedListNode<K, V>
    {
        public K Key { get; set; }
        public V Value { get; set; }
        public MyLinkedListNode<K, V> Next { get; set; }

        public MyLinkedListNode(K key, V value)
        {
            Key = key;
            Value = value;
        }
    }
}
