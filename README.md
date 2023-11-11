# Learning log

<!-- 
## 2 ##
*21st September*
### Today's progress ###
### Thoughts ###
### Links to work/resources ###
-->

## 8 ##
*10th November*
### Today's progress ###
I started to work on redesigning my portfolio and I can't wait to share the new version of that! I decided to work on my experience with Figma and I started the [Scrimba Figma to Code course](https://scrimba.com/learn/figmatocode).

### Thoughts ###
I regularly read tech newsletters. But the one that I always open and always read till the very end is the one by Quincy Larson from the FreeCode Camp. As a long life learner, I'm always excited for some inspiration on learning topics, and there is always a great quote. I appreciate a lot Quincy's talent for storytelling. I didn't have time to read [his book](https://www.freecodecamp.org/news/learn-to-code-book/), so I appreciated the [audio version](https://open.spotify.com/episode/7hz0vgue0AQWoB2CFsmwar?si=13cdd2a88ac74cbc). Really nice and encouraging one! It gave me some good vibes.  


## 7 ##
*19th September*

### Today's progress ###
* I spent some time working on [this kata on Codewars](https://www.codewars.com/kata/5d49c93d089c6e000ff8428c). When working on the programming problem, I tried different ways and found two solutions that worked.

I've started with this one: 

    function save(sizes, hd) {
      let sum = 0 
      let i = 0
      while (sum <= hd) {
        sum = sum + sizes[i]
        i++
      }
             
      return i - 1
    }

I tested it, and it passed all the exercise tests. But I noticed an issue when I considered an edge case: when the arguments are sizes = [1, 1, 1] and hd = 30. In this case, the test condition fails not because it meets the loop's criteria but because undefined <= hd results in NaN. And NaN is considered false in the condition statement. I decided to add an additional if statement to cover that. 

    function save(sizes, hd) { 
      let i = 0;
      while (sum <= hd ) {
        sum = sum + sizes[i]
        i++
        if (i >= sizes.length) {
          return i
        }
      }
      return i - 1
    }

And just as a mental exercise, I checked if I could rewrite it with reduce() (and I did :-). 

    function save(sizes, hd) {
      let result = 0;
      sizes.reduce((acc, curr) => {
        if ((acc += curr) <= hd) result += 1;
        return acc;
      }, 0);
      return result;
    }

* I've learned about the stories that have shaped today's cybersecurity landscape, including the Brain virus, Morris worm, Love letter, and the Equifax data breach. These stories are truly fascinating! 😄

### Thoughts ###

Today, I joined the second meeting for the Kids First project. I met the other teams and took part in discussions about data structures, UI, and information flow. It's fascinating to see the complexity of the decisions and the many factors that need consideration before making final choices. I have a lot to learn to fully engage, but I'm hopeful that my experience with React, styling and Figma files will be valuable!

### Links to work/resources ###
* [Brain virus](https://en.wikipedia.org/wiki/Brain_(computer_virus))
* [Morris worm](https://en.wikipedia.org/wiki/Morris_worm)
* [ILOVEYOU virus](https://en.wikipedia.org/wiki/ILOVEYOU)
* [Equifax data breach](https://en.wikipedia.org/wiki/2017_Equifax_data_breach) 
  
## 6 ##
*18th September*

### Today's progress ###
* I solved another [Codewar kata](https://www.codewars.com/kata/539de388a540db7fec000642). I learned that you can compare the dates using the new Date() constructor.

  

          function checkCoupon(enteredCode, correctCode, currentDate, expirationDate){
            const enteredDate = new Date(currentDate);
            const expiredDate = new Date(expirationDate);
          
            if (enteredCode === correctCode && enteredDate <= expiredDate) {
             return true;
            } else {
             return false;
            }
          }
  
* As I'm progressing in my cybersecurity course, I learned about the differences between PII (Personal Identifiable Information, including home address, e-mail, phone number, date of birth, IP address) and SPII (Sensitive Personal Identifiable Information, including biometric data, medical data, SSN number). I feel that nowadays understanding the basics of cybersecurity is like the ABCs of keeping our digital world safe.
  
### Thoughts ###
I just had my first meeting on the Kids First project as a front-end developer. I'm super excited. It's my first experience joining a project that's already in full swing. That gives me a fresh perspective. It also shows me even better the importance of effective communication and solid documentation. A lot to learn! 

### Links to work/resources ###
* [Date constructor on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/Date#return_value)

## 5 ##
*14th September*

### Today's progress ###
* I used a throw statement for throwing an error while checking the area of a circle in this codewars.com [kata](https://www.codewars.com/kata/537baa6f8f4b300b5900106c)

          function circleArea(radius) {
              if(radius > 0) {
              const area = (Math.PI*Math.pow(radius, 2))
              return area
              } else {
                 throw new Error ("Radius must be positive number")  
              }      
          }
* I had an interesting discussion with my pair programming partner about the differences between types of rounding of numbers. I've checked the differences between toFixed(), Math.floor(), Math.ceiling() and toPrecision(), and I've learned what significant digits are. Cool!
  
### Thoughts ###
I recently spent a lot of time with the tech community in Ottawa (Ottawa tech meetup this week, and I hope to join Ottawa React meetup next week too). Apart from finishing the mentor training for Canada Learning Code, I enrolled in the new project as a volunteer front-end developer. I'm also going slowly through the cybersecurity certification and I started my [Joy Of React](https://www.joyofreact.com/) course. I'm really busy but I can't stop, because one thing learned usually means 10 new to learn 🤷‍♀️.  Which is exciting 🎉

### Links to work/resources ###
* [Joy of React by Josh W. Caomeau](https://www.joyofreact.com/)
* [OttawaJS meetups](https://ottawajs.org/)
* [toFixed() on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toFixed)

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

As I practice pair programming with a new colleague recently, I discovered once again how good it is to have an extra pair of eyes to debug the code (and it makes it so much more time-efficient). You know, I used to think that programming was all about doing your thing solo, like a one-person show. But the more I dive into it, the more I realize that it's actually a team sport. It's pretty cool how it's all about teamwork in the end!

### Links to work/resources ###
[More about at()](https://www.freecodecamp.org/news/javascript-at-method/)


## 3 ##
*22nd August*

### Today's progress ###
* I spent some time with my pair programming partner on Codewars challenges, manipulating arrays and transforming strings. I needed to check the documentation of join(), especially how it behaves on the arrays containing arrays (you cannot control the separators of the nested arrays!) 
* I read about unary plus (+), which evaluates the operand, but tries to evaluate it to the number. I didn't think about the consequences of that for nonnumerical values, good to keep it in mind.  

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

