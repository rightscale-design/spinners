# designkit-spinners
1.0.0

A Sass module for spinners used in RightScale apps.

## Install
```
npm i --save designkit-spinners
```

## CSS

```css
@-webkit-keyframes spinner-disc-rotate {
  0% {
    -webkit-transform: rotateZ(-360deg);
            transform: rotateZ(-360deg);
  }
  100% {
    -webkit-transform: rotateZ(0deg);
            transform: rotateZ(0deg);
  }
}

@keyframes spinner-disc-rotate {
  0% {
    -webkit-transform: rotateZ(-360deg);
            transform: rotateZ(-360deg);
  }
  100% {
    -webkit-transform: rotateZ(0deg);
            transform: rotateZ(0deg);
  }
}

@-webkit-keyframes spinner-dots-fade {
  0%,
  80%,
  100% {
    opacity: 1;
  }
  40% {
    opacity: .2;
  }
}

@keyframes spinner-dots-fade {
  0%,
  80%,
  100% {
    opacity: 1;
  }
  40% {
    opacity: .2;
  }
}

.spinner-disc {
  display: block;
  width: 10px;
  height: 10px;
}

.spinner-disc:after {
  position: relative;
  display: block;
  width: 20px;
  height: 20px;
  content: '';
  border-style: solid;
  border-width: 1px;
  border-top-color: #000;
  border-right-color: #ddd;
  border-bottom-color: #ddd;
  border-left-color: #000;
  border-radius: 100%;
  opacity: .5;
  -webkit-animation: spinner-disc-rotate .6s linear infinite;
          animation: spinner-disc-rotate .6s linear infinite;
}

.spinner-disc.spinner-disc-sm:after {
  width: 10px;
  height: 10px;
}

.spinner-disc.spinner-disc-md:after {
  width: 16px;
  height: 16px;
}

.spinner-disc.spinner-disc-thick:after {
  border-width: 2px;
}

.spinner-disc.spinner-disc-thicker:after {
  border-width: 3px;
}

.spinner-disc {
  position: absolute;
  top: calc(50% - 11px);
  left: calc(50% - 11px);
}

.spinner-dots,
.spinner-dots:before,
.spinner-dots:after {
  width: 16px;
  height: 16px;
  background-color: #000;
  border-radius: 50%;
  -webkit-animation: spinner-dots-fade 1s infinite ease-in-out;
          animation: spinner-dots-fade 1s infinite ease-in-out;
  -webkit-animation-fill-mode: both;
          animation-fill-mode: both;
}

.spinner-dots {
  -webkit-animation-delay: -.16s;
          animation-delay: -.16s;
  -webkit-transform: translateZ(0);
          transform: translateZ(0);
}

.spinner-dots:before, .spinner-dots:after {
  position: absolute;
  top: 0;
  content: '';
}

.spinner-dots:before {
  left: -24px;
  -webkit-animation-delay: -.32s;
          animation-delay: -.32s;
}

.spinner-dots:after {
  left: 24px;
}

.spinner-dots {
  position: absolute;
  top: calc(50% - 8px);
  left: calc(50% - 8px);
}

```

## Author

Jason Melgoza

## License

MIT
