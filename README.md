Javascript:

1 - What is your favourite new javascript feature and why?

* one of my favourite new javascript features is template literals , they made me finally get rid of string concatenation .


2 - Explain an interesting way in which you have used this javascript feature.

* this feature was very handy once when i had to add html tags as javascript objects in database , so template literals helped me in jumping to new line without extra coding and effort


3 - Is there any difference between regular function syntax and the shorter arrow function syntax? (Write the answer in your own words)

* there's few differences between normal function and arrow functions , one of them is that arrow functions don't have their own "this"

4 - What is the difference between ‘myFunctionCall(++foo)’   and  ‘myFunctionCall(foo++)’

* the value of foo is added by 1 immediately in myFunctionCall(++foo) and in the 2nd function it will be added after the second call 


5 - In your own words, explain what a javascript ‘class’ is and how it differs from a function.

* classes in javascript are a different type of functions , and the difference between classes and usual functions is that functions are hoisted and classes not .



Css:

6 - In your own words, explain css specificity.

* css specificity are the rules that the browser follows when there is conflicts in css 


7 - In your own words, explain, what is ‘!important’ in css.  Also how does it work?  Are there any special circumstances when using it, where it’s behaviour might not be what you expect?

* we use !important to force use the css values


8 - What is your prefered layout system: inline-block, floating + clearing, flex, grid, other?  And why?

* flex is my favourite nowdays because it makes my work easy 


9 - Are negative margins legal and what do they do (margin: -20px)?

* yes they are legal and i use them for overlapping


10 - If a <div/> has no margin or other styling and a <p/> tag inside of it has a margin top of some kind, the margin from the <p/> tag will show up on the div instead (the margin will show above the div not inside of it), why is this?  What are the different things that can be done to prevent it?





Unit tests:

11 - What technologies do you use to unit test your react components?

* i use jest

12 - Are there any pitfalls associated with this technology that have caused you difficulty in the past?

* it is slow


13 - How do you test in your unit tests to see if the correct properties are being passed to child components.






React:

14 - React test step1:

Create a react component that has a <div/> with a border.
Inside this <div/> should be a <span/> that displays the ‘live’ width of the browser window at all times.  Keep in mind that the size of the window could easily be changed by the user and you should reflect this.

* class ChangeWindowDimensions extends React.Component {
  state = { width: 0, height: 0 };
  render() {
    return( 
    <div style={{border: '1px solid #000000'}}>
      <span>Window size: {this.state.width} x {this.state.height}</span>;
    </div>
  )
  }
  updateDimensions = () => {
    this.setState({ width: window.innerWidth, height: window.innerHeight });
  };
  componentDidMount() {
    window.addEventListener('resize', this.updateDimensions);
  }
  componentWillUnmount() {
    window.removeEventListener('resize', this.updateDimensions);
  }
}


15 - React test step2:

Inside the <div/> you created in the previous step, add a text input that, as a number is entered into it, uses that number to set the height of the div itself in pixels, live as you update the text field (keypress not change event).


*    handleKeyUp(e) {
      this.setState({height: e.target.value});
    }

    <div style={{border: '1px solid #000000'}}>
    <input onKeyUp={() => this.handleKeyUp}/>
      <span>Window size: {this.state.width} x {this.state.height}</span>;
    </div>


16 - React test step3:

Add the following code to your project root (same project as in step 2, but add the code in the global / window space):  

    Let divHeight;
    window.setDivHeight = (height) => divHeight = height;

Add a HOC for your div component that allows you to set the height of your <div/> component from the previous steps by calling that external function.

If you do not know what a HOC is or how to create one, that is also fine, just mention that in your answer and instead create a parent component that can still do this (allow you to call that function ‘setDivHeight’ in order to set the height of the div manually.

Bare in mind that when the height of the div is forcefully set like this, the text fields value should also update to reflect this and should still carry on working as normal (user can continue to modify its value).









RXjs:


17 - What are the differences between Subject, BehaviorSubject and ReplaySubject?  And in what situation would you use each of these (please provide example scenarios)?


18 - If you have an array of values in a stream and you wish to pipe it such that it will emit the arrays values individually, one by one and wait for them all to be completed before processing another array, how would you do this?  Please provide a code example.


19 - If you have a stream that receives individual values and would like to pipe it such that it builds an array out of these values, emitting the updated array each time a new value is added to it, how would you do this?  Please provide a code example.


Twilio:


20 - Explain which of the Twilio Api’s you have used.  Also explain how and in what scenarios you have used them.

* i used twilio to send sms from an application

