## 1. What teams at Vineti are you interested in and why? (Dev or QA) ##
#### I am interested in dev team.  At first for me creating and improving codes is more interesting than testing them. Software Development is more attractive for me and I think it will give me many opportunities to go forward, go ahead. Also I am more familiar with development rather than QA.   ####

## 2.What is your favorite programming language and why? ##
####   I don't have a lot of experience with many programming languages . But working with Java I saw that I like it more than other languages I have worked with, because Java is simple to learn. Java is an object oriented language which helps in improving programming skills. And also Java helps me to enhance my logical thinking . ###

## 3. What is a linked list? ##
#### A linked list is a linear data structure where each element is a separate object. Each element( node) of a list is comprising of two items - the data and a reference to the next node. The last one has a reference to null. The entry point into a linked list is called the head of the list. Head is not a separate node, but the reference to the first node. If the list is empty then the head is a null reference. ####

## 4.You work in an ice cream shop and step into the back for a few minutes. You return and see a large group of people waiting. How would you serve them? ##
#### FIFO , who came the first ,will be served the first  :D ####

## 5. How would you test a pen? ##
#### 1.	I will test the type of pen ( ball point pen, ink pen or gel pen), ####
#### 2.	the outer body of the pen(whether it should be metallic, plastic or any other material as per the specification).  ####    
#### 3.	Size and shape should be confirmable for writing(UI Testing). ####              
#### 4.	I will check if the grip on the pen is superior (Usability Testing). ####
#### 5.	Pen must  write  smoothly with continuous and not breaking while writing(Usability Testing). ####
#### 6.	Check  if ink in not being leak from refill in normal conditions. ####
#### 7. Pen must write  on the page properly (Functional Testing). ####


## 6. As a test engineer in Amazon what would you test first (assuming authentication functionality is already covered)? ##
#### First of all I will test the system of payment .Because if it doesn't work properly one day it will cause discount of a great amount of money and customers. ####

## 7. You have a list of numbers from one to one million and there is a missing number. How would you find the missing number? ##
#### //First I will Get the sum of numbers  ####
####  Total= n*(n+1)/2  ####
#### Then subtract all the numbers from sum and I will get the missing number// ####
``` java  
    int getMissingNum (int a[], int n)
    {
        int i, total;
        total  = (n+1)*(n+2)/2;    
        for ( i = 0; i< n; i++)
           total -= a[i];
        return total;
    }

```

## 8. How would you determine the angle between the hour-hand and minute-hand of a clock at 3:20.  ##
#### The angle between 3 and 4 is 360/12 = 30. And when the minute-hand is at 4 (20 minutes), the hour-hand is already past 1/3 of an hour, so the angle between them is equal to  30-30*1/3 = 20 ####


## 9. How would you determine if a number is a power of two.  ##
#### For me an easy way to solve the problem is this ###
``` java
boolean powerOfTwo(int x) {
        if (x== 0) {
            return false;
        }
        return (x & (x - 1)) == 0;
  }
```
## 10. How would you remove duplicates from a list? ##

#### I would use Hash table data structure for this purpose, as the average complexity of search is O(1). We iterate through the list, and add the element to the hash table if it doesn’t already contain it, and if it does, we remove that value from our list. ####
#### And also I know that in PHP there is a function called array_unique(array) ,which removes duplicate values from an array.  #####

## 11. How would you determine if a string has all unique characters? ##
#### We can use  2 loops with variable i and j. Compare a[i] and a[j]. If they become equal at any point, return false. ####
``` java
boolean uniqueChars(String a)
    {

        for (int i = 0; i < a.length(); i++)
            for (int j = i + 1; j < a.length(); j++)
                if (a.charAt(i) == a.charAt(j))
                    return false;

        return true;
    }
```

## 12. How would you reverse a string? ##

#### As we have the string, we have to start printing with the last letter.  ####
``` java
    public static void main(String[] args)
    {


        Scanner read = new Scanner(System.in);
        String str = read.nextLine();
        String reverse = "";


        for(int i = str.length() - 1; i >= 0; i--)
        {
            reverse = reverse + str.charAt(i);
        }
        System.out.println(reverse);

        }
```
## 13. How would you compress a string such that 'AAABCCDDDD' becomes 'A3BC2D4'? Only compress the string if it saves space. ##

``` Java
public static String compress(String str) {
    String result = "";

    int index = 0;

    while (index < str.length()) {
        char ch = str.charAt(index);
        int count = count(str, index);
        if (count == 1)
            result += "" + ch;
        else
            result += "" + ch + count;
        index += count;
    }

    return result;
}

public static int count(String str, int index) {
    char ch = str.charAt(index);
    int i = 1;
    while (index + i < str.length() && str.charAt(index + i) == ch)
        i++;
    return i;
}
```

## 14.Given an array of 0's and 1's, how would you move all of the 0's to the beginning of the array and all of the 1's to the end of the array? ##
#### First I will count the number of 0s.    Let count be K. As we have count, we can put K 0s at the beginning and 1s at the remaining n – K positions in array. ####
``` java
   void seperate(int a[], int n)
    {
        int count = 0;

        for (int i = 0; i < n; i++) {
            if (a[i] == 0)
                count++;
        }

        for (int i = 0; i < count; i++)
            a[i] = 0;
        for (int i = count; i < n; i++)
            a[i] = 1;
    }

```
## 15. How would you design a vending machine or a toaster? ##
### First of all I will be focused on this questions-  ###
#### 1.	How much time do I have to do that. ####
#### 2.	Who will use this product and for what purpose? ####
#### 3.	What are the use cases? ####
#### 4.	What are the boundaries of use? ####
#### 5.	I will clarify age range, ####
#### 6.	 Is it safe enough to be operated by a child  ? ####
#### 7.	What sizes of bread would fit it? ####
#### 8.	How much power limit does it operate on as per the  vendor? ####
#### 9.	And I try to find optimal way to design it with using less money and time. ####


## 16. You have two lightbulbs at a 100-story building. You want to find the lowest floor at which the bulbs will break when dropped. How would you find the floor using the least number of drops? ##
#### I will start trying from 16th  floor, if it  breaks , I will try 1-15 floors and the worst case it  will 16 tries. If it doesn’t break in 16th floor ,then I will try 31 and if it breaks , the 17-30(16 tries , including the try on the floor 16).Then 45,58,70,81,91,100  floors. If I reach 91, it means that I have tried 7 floors so far and if it doesn’t break , then there is 9 more tries to  get 100 (thus 16 in the worst case). ####

## 17. If you have a square room with no roof, and you had four pillars you had to plant on the walls so that each pillar touched two walls, how would you do it? ##
#### In the square of the roof(or everywhere  bun only not the part with the floor ) I will inscribe a square formed by the pillars, that   all of  the vertices  of square formed by pillars lies on the boundaries of the roof’s square. If it will be needed I can cut the pillars so that they  can be in the boundaries of square.  ####

## 18.Given 9 balls all of which weigh the same except for one, what is the minimum of weightings necessary to find the ball weighs more (or less)? ##
#### As we didn’t know that the different ball is heavier or lighter , the minimum weighting is 3. ####
#### 1 weigh:=>   First I form by the balls three groups  A={B1,B2,B3}, B={B4,B5,B6} and C={B7,B8,B9}.And  let’s choose 2 groups and weigh them ,for example A and B . If the scale is in balance then  the different ball is in C. ####
#### 2nd weigh: => To find out weather the ball is heavier or lighter I will weigh A and C . If C is on lighter side then a ball is lighter or if C is on heavier side then a ball is heavier. Let’s assume that different ball is heavier. ####
#### 3th :=>Then I will weigh 2 balls from C. If scale is in balance .then the remaining ball is the different one, otherwise the  ball on the heavier side is the heavy ball. ####
#### 2nd:=> If the scale is not balanced, then the different  ball must be either in A or B. Now weigh A and  C. If the scale is balanced, then the ball must be in B  and will be lighter if B  was on the lighter side or will be heavier if B  was on the heavier side during First weigh.  ####
