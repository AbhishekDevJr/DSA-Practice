# DSA-Practice

Srting Questions:-
1. Longest Common Prefix
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
