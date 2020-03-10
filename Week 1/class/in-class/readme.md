# Answer
## problem 1
```
class Time
{
private:
    int hour;
    int minute;
    int second;
public:
    Time(int h, int m, int s);
    bool isEarlierThan(Time t);
    void print();
};

Time::Time(int h, int m, int s)
{
    hour = h; minute = m; second = s;
}

void Time::print()
{
    cout << hour << ":" << minute << ":"<< second;
}

bool Time::isEarlierThan(Time t)
{
    if(hour < t.hour)
       return true;
     else if(hour == t.hour)
     {
       if(minute < t.minute)
         return true;
       else if(minute == t.minute)
       {
         if(second < t.second)
           return true;
       }
     }
     return false;   
}

int main()
{
    int te[9] = {0};
    for(int i = 0; i < 9; i++)
      cin >> te[i];
    Time t1(te[0], te[1], te[2]);
    Time t2(te[3], te[4], te[5]);
    Time t3(te[6], te[7], te[8]);
    
    if(t1.isEarlierThan(t2))
    {
      if(t2.isEarlierThan(t3))
        cout << 3 <<endl;
      else
        cout << 2<< endl;
    }
    else
    {
      if(t1.isEarlierThan(t3))
        cout << 3 <<endl;
      else
        cout << 1 <<endl;
    }
    return 0;
}
```
## problem 2
```
class Time
{
private:
    int hour;
    int minute;
    int second;
    void printTwoDigits(int n);
public:
    Time(int h, int m, int s);
    bool isEarlierThan(Time t);
    void printNicely();
};

Time::Time(int h, int m, int s)
{
    hour = h; minute = m; second = s;
}

void Time::printTwoDigits(int n)
{
  cout << (n < 10 ? "0" : "");
  cout << n;
}

void Time::printNicely()
{
    printTwoDigits(hour);
     cout << ":";
     printTwoDigits(minute);
     cout << ":";
     printTwoDigits(second);
    cout  << endl;
}

bool Time::isEarlierThan(Time t)
{
    if(hour < t.hour)
       return true;
     else if(hour == t.hour)
     {
       if(minute < t.minute)
         return true;
       else if(minute == t.minute)
       {
         if(second < t.second)
           return true;
       }
     }
     return false;
     
}

int main()
{
    int te[9] = {0};
    for(int i = 0; i < 9; i++)
      cin >> te[i];
    Time t1(te[0], te[1], te[2]);
    Time t2(te[3], te[4], te[5]);
    Time t3(te[6], te[7], te[8]);
    
    if(t1.isEarlierThan(t2))
    {
      if(t2.isEarlierThan(t3))
          t3.printNicely();
      else
          t2.printNicely();
    }
    else
    {
      if(t1.isEarlierThan(t3))
          t3.printNicely();
      else
          t1.printNicely();
    }
    
    return 0;
}
```
## problem 3
## problem 4
## problem 5
## problem 6
