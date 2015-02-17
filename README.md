# racingAssignment
# racingAssignment
<script>

var Person = function(name, drinks, sobering){
  this.name = name;
  this.drinks = filterInt(prompt("Enter # of drinks"));
  this.sobering = filterInt(prompt("How many hours passed?"));

  this.drunkLevel = 0; 
  
  this.report = function(){
    return this.name + "'s alcohol level is: " + this.drunkLevel;
  }

  this.drinking = function(){
  return this.drunkLevel += drinks;
  return this.drunkLevel -= sobering;
  }; 
}

filterInt = function (value) {
  if(/^(\-|\+)?([0-9]+|Infinity)$/.test(value))
    return Number(value);
  return NaN;
  }//found at https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseInt

var JoeShmoe = new Person ("Joe Shmoe");
var BobShmob = new Person ("Bob Shmob");

var passOut = 15;
while (JoeShmoe.drunkLevel < passOut || BobShmob.drunkLevel < passOut) {
	JoeShmoe.drinking();
  BobShmob.drinking();

  if (this.drunkLevel >= passOut){
    console.log(this.name + " passed out");
  } else {
    JoeShmoe.drinking;
    BobShmob.drinking;
  }
};

console.log(JoeShmoe.report() + " and " + BobShmob.report());
</script>
