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

3. 
