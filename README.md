# mywork-space

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
Author:BIKRAMADITYA DALAI
