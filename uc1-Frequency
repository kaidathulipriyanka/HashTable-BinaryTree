using System;
using System.Collections.Generic;

namespace HashTableAndTree
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Welcome to Hash Table and Tree Program...");

            string sentence = "To be or not to be";
            Dictionary<string, int> wordFrequency = GetWordFrequency(sentence);

            Console.WriteLine("Word Frequency:");
            foreach (var data in wordFrequency)
            {
                Console.WriteLine($"{data.Key}: {data.Value}");
            }
        }

        static Dictionary<string, int> GetWordFrequency(string sentence)
        {
            Dictionary<string, int> wordFrequency = new Dictionary<string, int>();

            string[] words = sentence.Split(' ');

            foreach (string word in words)
            {
                if (wordFrequency.ContainsKey(word))
                {
                    wordFrequency[word]++;
                }
                else
                {
                    wordFrequency[word] = 1;
                }
            }

            return wordFrequency;
        }
    }
}
