# racingAssignment

<script>

var Person = function(name, drinks, sobering){
  this.name = name;
  this.drinks = parseInt((prompt("Enter # of drinks")), 10);//still not working. returns NaN for all answrs
  this.sobering = parseInt((prompt("How many hours passed?")), 10);

  this.drunkLevel = 0; 
  
  this.report = function(){
    return this.name + "'s alcohol level is: " + this.drunkLevel;
  }

  this.drinking = function(){
  return this.drunkLevel += drinks;
  return this.drunkLevel -= sobering;
  }; 
}

//var num = parseInt(trimmed, 10); found this somewhere online

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
