# demo
this repository is related to cloning.
function reverse_a_number(n)
{

    /* Write your code here
    No need to specify return type 
    Input and output already taken care of, you have to just return the output variable */
    var ans = 0 ;
    while(n != 0){
        var rem = n% 10;
        ans = ans * 10 + rem ;
        n = Math.floor(n/10);
    }
    return ans ;
}







process.stdin.resume();
process.stdin.setEncoding('ascii');

var input_stdin = "";
var input_stdin_array = "";
var input_currentline = 0;

process.stdin.on('data', function (data) {
    input_stdin += data;
});

process.stdin.on('end', function () {
    input_stdin_array = input_stdin.split("\n");
    main();    
});

function readLine() {
    return input_stdin_array[input_currentline++];
}


function main() {
    
    let n = parseInt(readLine());
    let ans = reverse_a_number(n);
    console.log(ans);

}
