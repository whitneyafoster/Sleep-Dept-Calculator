# Sleep-Dept-Calculator

const getSleepHours = day => {
  if (day === 'monday') {
    return 8;
  } else if (day === 'tuesday') {
    return 8;
  } else if (day === 'wednesday') {
    return 8;
  } else if (day === 'thursday') { 
   return 8;
  } else if (day === 'friday') {
    return 8;
  } else if (day === 'saturday') {
    return 8;
  } else if (day === 'sunday') {
    return 8;
  }
}

const getActualSleepHours = () => 
getSleepHours('monday') + getSleepHours ('tuesday') + getSleepHours ('wednesday') + getSleepHours ('thursday') +
  getSleepHours ('friday') + getSleepHours ('saturday') + getSleepHours ('sunday'); 


const getIdealSleepHours = () => {
  let idealHours = 8;
  return idealHours * 7;
}

const calculateSleepDebt = () => {
  const actualSleepHours = getActualSleepHours();
  const idealSleepHours = getIdealSleepHours();
  
  if (actualSleepHours === idealSleepHours) {
    console.log("You've got the perfect amount of sleep!");
  }
  
  else if (actualSleepHours > idealSleepHours) {
    console.log("You've got " + (idealSleepHours -= actualSleepHours) + "more hours of sleep this week.");
  }
  
  else if (actualSleepHours < idealSleepHours) {
    console.log("You should get some rest because you've slept " + (idealSleepHours - actualSleepHours) + "hours less than you should have this week.");
  }
  
  else {
    console.log("Error. Something went wrong. Check your code.");
  }
};

calculateSleepDebt();

