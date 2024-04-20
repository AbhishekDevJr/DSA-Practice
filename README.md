# DSA-Practice

Srting Questions:-
1.    Longest Common Prefix
  
      const longestCommonPrefix = (strs) => {
        let i = 1;
        let temp = strs[0];
  
        while(i < strs.length){
          if(!strs[i].startsWith(temp)){
            temp = temp.slice(0, -1);
          }
          else{
            i++;
          }
        }
     return temp;
   }

console.log(longestCommonPrefix(["flower","flow","flight"]));
// fl

2.   Valid Parentheses:-
   
      const isValid = (s) => {
        const stack = [];
  
        for(let i = 0; i < s.length; i++){
          if(s[i] === '('){
            stack.push(')');
          }
          else if(s[i] === '{'){
            stack.push('}');
          }
          else if(s[i] === '['){
            stack.push(']')
          }
          else if(stack.pop() !== s[i]){
            return false;
          }
        }
  
     return !stack.length;
   }
console.log(isValid('[{()}]'));
// true

3. Valid Palindrome
  const isValid = (s) => {
  const temp = s.toLowerCase().replace(/[^a-zA-Z0-9]/g, '');
  
  for(let i = 0; i < temp.length; i++){
    if(temp[i] !== temp[temp.length-1-i]){
      return false;
    }
  }
  
  return true;
}

console.log(isValid('A man, a plan, a canal: Panama'));
//true

5. Isomorphic Strings, Word Pattern (Similar Questions)

     const isIsomorphicString = (s, t) => {
  if(s.length !== t.length){
    return false;
  }
  
  const obj = {};
  const obj2 = {};
  
  for(let i = 0; i < s.length; i++){
    if((obj[s[i]] && obj[s[i]] !== t[i]) || (obj2[t[i]] && obj2[t[i]] !== s[i])){
      return false;
    }
    else{
      obj[s[i]] = t[i];
      obj2[t[i]] = s[i];
    }
  }
  
  return true;
  
}
console.log(isIsomorphicString('egg', 'add'));
//true
