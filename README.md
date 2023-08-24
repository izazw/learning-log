# Learning log

<!-- 
## 2 ##
*21st August*
### Today's progress ###
### Thoughts ###
### Links to work/resources ###

-->
## 4 ##
*23rd August*

### Today's progress ###
* learnt at() array method, a relatively new addition to JavaScript. At() allows for the usage of relative indexing and is pretty cool! From my perspective, it adds a lot of readability to the code and is so much more intuitive. Have a look here:

        const myGatineau =["Pink Lake Trail", "King Mountain Trail", "Luskville Falls Trail",
        "Champlain Lookout Trail", "Wolf Trail"]
        console.log(myGatineau.at(0))
        //output: "Pink Lake Trail"
        console.log(myGatineau.at(-1))
        //output: "Wolf Trail"

        // And before at() it could be achieved by:
         console.log(myGatineau[MyGatineau.length - 1])
        //output: "Wolf Trail"
        

  * used the spread operator to find the smallest value in the array with Math.min() to solve [one of kata in Codewars](https://www.codewars.com/kata/577a98a6ae28071780000989) 

### Thoughts ###

As I practice pair programming with a new colleague recently, I feel again that's so good to have an extra pair of eyes to debug the code (and it makes it so much more time-efficient). You know, I used to think that programming was all about doing your thing solo, like a one-person show. But the more I dive into it, the more I realize that it's actually a team sport. It's pretty cool how it's all about teamwork in the end!

### Links to work/resources ###
[More about at()](https://www.freecodecamp.org/news/javascript-at-method/)


## 3 ##
*22nd August*

### Today's progress ###
* I spent some time with my pair programming partner on Codewars challenges, manipulating arrays and transforming strings. I needed to check the documentation of join(), especially how it behaves on the arrays containing arrays (you cannot control the separators of the nested arrays!) 
* I read a bit unary plus (+), which evaluates to the operand, but tries to evaluate it to the number. I didn't think about the consequences of that for nonnumerical values, good to keep it in mind.  

      const x = 1;
      console.log(+x);
      // output: 1
      
      console.log(+true);
      //output: 1
      
      console.log(+false);
      //output: 0

      console.log(+"");
      // output: 0
      
      console.log(+'hello');
      // Expected output: NaN


### Thoughts ###

As part of my post-Bootcamp coding routine, I coorganize pair programming sessions. I primarily concentrate on JavaScript, considering it a solid foundation for my ongoing learning. I found pair programming particularly useful in boosting confidence to learn, code, and solve problems in public, fostering open communication. It brings a lot of enjoyment from puzzle-solving too! Good to see how it steadily enhances my grasp of JavaScript.

### Links to work/resources ###
[Unary plus(+) documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Unary_plus)

[join() documentation ](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)


## 2 ##
*21st August* 

### Today's progress ###
Learn about GitHub gists today. Gists are just a simple way to share code snippets and entire files. They work as repositories and can be cloned or forked by other people (if set to public).  [https://gist.github.com/]. I used gist to add the Totoro gif. [Check it out here.](https://gist.github.com/izazw/91d94f1a0fcf047e85ef9c75733fd09f)


### Thoughts ###
Came back after camping holidays (explored Quebec's fiords and mountains in Grands Jardins) and need to stretch again my coding muscles! I'm updating my portfolio and can't wait to share the results. 

### Links to work/resources ###
[Gists basics](https://docs.github.com/en/get-started/writing-on-github/editing-and-sharing-content-with-gists/creating-gists)


## 1 ##
*10th August* 

### Today's progress ###
* Inspired by [Katie Hawcutt 100 Days Of Code Diary](https://github.com/katiehawcutt/100DaysOfCode) I decided to keep track of my learning :-)

### Thoughts ###
I hope that this log will help me to embrace the fact that learning is a continuous process, celebrate small victories, and view challenges as opportunities for growth. I treat is a reminder that the journey matters as much as the destination!  

### Links to work/resources ###
* [Wes Bos' intro to Markdown](https://masteringmarkdown.com/) 

