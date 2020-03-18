## problem 1
```
bool isMyPunct(char c, string punct);

int main()
{
  string s = "";
  getline(cin, s);
  
  int numMyPunct = 0;
  for(int i = 0; i < s.length(); i++)
    if(isMyPunct(s[i], ",.:;!?"))
      numMyPunct++;
  
  cout << numMyPunct << endl;
  
  return 0;
}

bool isMyPunct(char c, string punct)
{
  for(int i = 0; i < punct.length(); i++)
    if(c == punct[i])
      return true;
  return false;
}
```
## problem 2
```
void makeLowercase(string& str);

int main()
{
  int wordCnt = 0;
  cin >> wordCnt;
  string target = "";
  cin >> target;
  makeLowercase(target);
  
  string* dict = new string[wordCnt];
  for(int i = 0; i < wordCnt; i++)
    cin >> dict[i];
  
  // just a linear search
  bool targetExist = false;
  for(int i = 0; i < wordCnt; i++)
  {
    if(target.compare(dict[i]) == 0)
    {
      cout << 1; 
      targetExist = true;
      break;
    }
  }
  if(targetExist == false)
    cout << 0;

  delete [] dict;

  return 0;
}

void makeLowercase(string& str)
{
  for(int i = 0; i < str.length(); i++)
    str[i] = tolower(str[i]);
}
```
## problem 3
```
const int MAX_DIGIT = 100;

string toDollarNumber(int value)
{
  // one way of converting an integer to a C++ string
  // char c[MAX_DIGIT] = {0};
  // itoa(value, c, 10);
  // string s = c;

  // another way
  string s = to_string(value);
  
  string dn = "$";
  int n = s.length();

  int startPos = n % 3;
  if(startPos == 1)
    dn = dn + s[0] + ",";
  else if(startPos == 2)
    dn = dn + s.substr(0, 2) + ",";

  for(int i = startPos; i < n; i += 3)
    dn = dn + s.substr(i, 3) + ",";
  dn.erase(dn.length() - 1);
  
  return dn;
}

int main()
{
  int dollar = 0;
  cin >> dollar; 
  
  cout << toDollarNumber(dollar) << endl;
  
  return 0;
}
```
## problem 4
```
void makeLowercase(string& str);
bool isInDict(string target, string dict[], int wordCnt);


int main()
{
  int wordCnt = 0;
  cin >> wordCnt;

  string target = "";
  cin >> target;
  makeLowercase(target);
  
  string filePath = "";
  cin >> filePath;
  
  ifstream fin(filePath);
  if(fin)
  {
    string* dict = new string[wordCnt];
    for(int i = 0; i < wordCnt; i++)
      fin >> dict[i];
    
    cout << isInDict(target, dict, wordCnt) << endl;
  
    delete [] dict;
  }
  fin.close();

  return 0;
}








void makeLowercase(string& str)
{
  for(int i = 0; i < str.length(); i++)
    str[i] = tolower(str[i]);
}

bool isInDict(string target, string dict[], int wordCnt)
{
  for(int i = 0; i < wordCnt; i++)
  {
    if(target.compare(dict[i]) == 0)
      return true;
  }
  return false;
}
```
## problem 5
```
void makeLowercase(string& str);
bool isInDict(string target, ifstream& fin);


int main()
{
  string target = "";
  cin >> target;
  makeLowercase(target);
  
  string filePath = "";
  cin >> filePath;
  
  ifstream fin(filePath);
  if(fin)
    cout << isInDict(target, fin) << endl;
  fin.close(); 

  return 0;
}
```
## problem 6
```

void makeLowercase(string& str);
bool isInDict(string target, ifstream& fin);


int main()
{
  string target = "";
  cin >> target; // be careful!!
  cin.ignore(); 
  makeLowercase(target);
  
  string filePath = "";
  getline(cin, filePath); // be careful!!
  
  ifstream fin(filePath);
  if(fin)
    cout << isInDict(target, fin) << endl;
  fin.close(); 

  return 0;
}








void makeLowercase(string& str)
{
  for(int i = 0; i < str.length(); i++)
    str[i] = tolower(str[i]);
}

bool isInDict(string target, ifstream& fin)
{
  while(!fin.eof())
  {
    string current = ""; 
    getline(fin, current);

    if(target.compare(current) == 0)
      return true;
  }
  return false;
}
```
