# 709.-To-Lower-Case
You can use ToLower() method 
alternative: dictionary using method: 


```c#

public class Solution {
    public string ToLowerCase(string str) {

       Dictionary<char, char> dict = new Dictionary<char, char>();
        
       string up = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
        string lo = "abcdefghijklmnopqrstuvwxyz";
        
        for(int i=0; i< 26; i++){
            dict.Add(up[i], lo[i]);
        }
        
        
        StringBuilder sb = new StringBuilder();
        
        foreach(var x in str.ToCharArray()){
            sb.Append(dict.ContainsKey(x) ? dict[x]: x);
        }
    
        return sb.ToString();
    }
}

`````
