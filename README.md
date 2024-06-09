# Mywork-space
//1=> it find a non-empty contiguous subarray with the largest sum
function contigiousSequence(n, arr) {
    let sum=0;
    let max=-Infinity;
    for(let i=0;i<n;i++){
        sum=Math.max(sum+arr[i],arr[i]);
        max=Math.max(sum,max);
    }
    return max;
}

//this is my first git Repository
//2=>it find the element, partitioning along which, the sum of elements to its left, equals the sum of elements to its right
function equalPartition(n, arr) {
    let leftside=new Array(n);
    for(let i=0;i<n;i++){
        leftside[i]=((i==0)?0:leftside[i-1])+arr[i]
    }
    let rightside=new Array(n);
    for(let i=n-1;i>=0;i--){
        rightside[i]=((i==n-1)?0:rightside[i+1])+arr[i]
    }
    for(let i=0;i<n;i++){
        if(leftside[i]==rightside[i]){
            return i;
        }
    }
    return -1;
}

//3=>it find if there is any subarray with 0 sum.
function subarraySumZero(n, arr) {
  let res=new Set();
  let sum=0;
  for(let i=0;i<n;i++){
    sum+=arr[i];
    if(sum===0 || res.has(sum)){
      return 'Yes';
    }
    res.add(sum);

  }
  return 'No';
}

Author:BIKRAMADITYA DALAI
