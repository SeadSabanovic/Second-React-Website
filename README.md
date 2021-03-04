
#  Second React.js Website

![Second React.js Website](https://raw.githubusercontent.com/SeadSabanovic/Second-React-Website/main/Bijoux.png)
___

### What I learned:
- Reusable Components
- Styled Components
- Hooks
### Functionality:
- Slide Change (Automatic)
```javascript
const [current, setCurrent] =  useState(0);
const  length  =  slides.length;
const  timeout  =  useRef(null);

useEffect(() => {
	const  nextSlide  = () => {
		setCurrent(current  => (current  ===  length  -1  ?  0  :  current  +  1))
	}
	
	timeout.current  =  setTimeout(nextSlide, 4500)
	
	return  function () {
		if (timeout.current) {
			clearTimeout(timeout.current)
		}
	}

}, [current, length])

```
