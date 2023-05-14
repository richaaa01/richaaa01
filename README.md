<form action="" class="container">
  <div class="input-container">
      <div class="input-content">
          <div class="input-dist">
              <div class="input-type">
                  <input placeholder="User" required="" type="text" class="input-is">  
                  <input placeholder="Password" required="" type="password" class="input-is">  
              </div>
          </div>
      </div>
  </div>
</form>
/*The eye icon on the password can be stylize with any tool you want
to use (the only way i know to do this correctly is using JS)
this is meant to be wide supported and it really depends on you browsers
if i realize any way to stylize the eye it could be added in the future
in other input type*/

.container {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-style: italic;
  font-weight: bold;
  display: flex;
  margin: auto;
  aspect-ratio: 16/9;
  align-items: center;
  justify-items: center;
  justify-content: center;
  flex-wrap: wrap;
  flex-direction: column;
  gap: 1em;
}

.input-container {
  filter: drop-shadow(46px 36px 24px #4090b5) drop-shadow(-55px -40px 25px #9e30a9);
  animation: blinkShadowsFilter 8s ease-in infinite;
}

.input-content {
  display: grid;
  align-content: center;
  justify-items: center;
  align-items: center;
  text-align: center;
  padding-inline: 1em;
}

.input-content::before {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  filter: blur(40px);
  -webkit-clip-path: polygon(26% 0, 66% 0, 92% 0, 100% 8%, 100% 89%, 91% 100%, 7% 100%, 0 92%, 0 0);
  clip-path: polygon(26% 0, 66% 0, 92% 0, 100% 8%, 100% 89%, 91% 100%, 7% 100%, 0 92%, 0 0);
  background: rgba(122, 251, 255, 0.5568627451);
  transition: all 1s ease-in-out;
}

.input-content::after {
  content: "";
  position: absolute;
  width: 98%;
  height: 98%;
  box-shadow: inset 0px 0px 20px 20px #212121;
  background: repeating-linear-gradient(to bottom, transparent 0%, rgba(64, 144, 181, 0.6) 1px, rgb(0, 0, 0) 3px, hsl(295, 60%, 12%) 5px, #153544 4px, transparent 0.5%), repeating-linear-gradient(to left, hsl(295, 60%, 12%) 100%, hsla(295, 60%, 12%, 0.99) 100%);
  -webkit-clip-path: polygon(26% 0, 31% 5%, 61% 5%, 66% 0, 92% 0, 100% 8%, 100% 89%, 91% 100%, 7% 100%, 0 92%, 0 0);
  clip-path: polygon(26% 0, 31% 5%, 61% 5%, 66% 0, 92% 0, 100% 8%, 100% 89%, 91% 100%, 7% 100%, 0 92%, 0 0);
  animation: backglitch 50ms linear infinite;
}

.input-dist {
  z-index: 80;
  display: grid;
  align-items: center;
  text-align: center;
  width: 100%;
  padding-inline: 1em;
  padding-block: 1.2em;
  grid-template-columns: 1fr;
}

.input-type {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  gap: 1em;
  font-size: 1.1rem;
  background-color: transparent;
  width: 100%;
  border: none;
}

.input-is {
  color: #fff;
  font-size: 0.9rem;
  background-color: transparent;
  width: 100%;
  box-sizing: border-box;
  padding-inline: 0.5em;
  padding-block: 0.7em;
  border: none;
  transition: all 1s ease-in-out;
  border-bottom: 1px solid hsl(221, 26%, 43%);
}

.input-is:hover {
  transition: all 1s ease-in-out;
  background: linear-gradient(90deg, transparent 0%, rgba(102, 224, 255, 0.2) 27%, rgba(102, 224, 255, 0.2) 63%, transparent 100%);
}

.input-content:focus-within::before {
  transition: all 1s ease-in-out;
  background: hsla(0, 0%, 100%, 0.814);
}

.input-is:focus {
  outline: none;
  border-bottom: 1px solid hsl(192, 100%, 100%);
  color: hsl(192, 100%, 88%);
  background: linear-gradient(90deg, transparent 0%, rgba(102, 224, 255, 0.2) 27%, rgba(102, 224, 255, 0.2) 63%, transparent 100%);
}

.input-is::-moz-placeholder {
  color: hsla(192, 100%, 88%, 0.806);
}

.input-is::placeholder {
  color: hsla(192, 100%, 88%, 0.806);
}

@keyframes backglitch {
  0% {
    box-shadow: inset 0px 20px 20px 30px #212121;
  }

  50% {
    box-shadow: inset 0px -20px 20px 30px hsl(297, 42%, 10%);
  }

  to {
    box-shadow: inset 0px 20px 20px 30px #212121;
  }
}

@keyframes rotate {
  0% {
    transform: rotate(0deg) translate(-50%, 20%);
  }

  50% {
    transform: rotate(180deg) translate(40%, 10%);
  }

  to {
    transform: rotate(360deg) translate(-50%, 20%);
  }
}

@keyframes blinkShadowsFilter {
  0% {
    filter: drop-shadow(46px 36px 28px rgba(64, 144, 181, 0.3411764706)) drop-shadow(-55px -40px 28px #9e30a9);
  }

  25% {
    filter: drop-shadow(46px -36px 24px rgba(64, 144, 181, 0.8980392157)) drop-shadow(-55px 40px 24px #9e30a9);
  }

  50% {
    filter: drop-shadow(46px 36px 30px rgba(64, 144, 181, 0.8980392157)) drop-shadow(-55px 40px 30px rgba(159, 48, 169, 0.2941176471));
  }

  75% {
    filter: drop-shadow(20px -18px 25px rgba(64, 144, 181, 0.8980392157)) drop-shadow(-20px 20px 25px rgba(159, 48, 169, 0.2941176471));
  }

  to {
    filter: drop-shadow(46px 36px 28px rgba(64, 144, 181, 0.3411764706)) drop-shadow(-55px -40px 28px #9e30a9);
  }
}
    <div align=center>
        <a href="https://www.linkedin.com/in/ahmedfathydev/"><img src="https://img.shields.io/badge/Linkedin-0077b5?style=flat&logo=linkedin" alt="LinkedIn" /></a>
        <a href="https://www.upwork.com/freelancers/~0121ca7f3563e57c0b"><img src="https://img.shields.io/badge/Upwork-494949?style=flat&logo=upwork" alt="UpWork" /></a>
        <a href="https://stackoverflow.com/users/11837259/ahmed-fathy"><img src="https://img.shields.io/badge/Stack Overflow-f48024?style=flat&logo=stackoverflow&logoColor=white" alt="Stack Overflow" /></a>
        <a href="https://www.quora.com/profile/Ahmed-Fathy-616"><img src="https://img.shields.io/badge/Quora-B92B27?style=flat&logo=quora" alt="Quora" /></a>
        <a href="https://t.me/ahmedfathydev"><img src="https://img.shields.io/badge/Telegram-0088cc?style=flat&logo=telegram" alt="Telegram" /></a>
    </div>

- 🌱 I’m currently learning **Google Data Analytics Course**

- 👯 I’m looking to collaborate on **machine learning projects**

- 📫 How to reach me **richasingh742421@gmail.com**

- ⚡ Fun fact **My mood changes faster than the stocks in share market.**

<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="https://instagram.com/richaaaa.01" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg" alt="richaaa.01" height="30" width="40" /></a>
</p>

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://aws.amazon.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" alt="aws" width="40" height="40"/> </a> <a href="https://www.cprogramming.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="c" width="40" height="40"/> </a> <a href="https://canvasjs.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/Hardik0307/Hardik0307/master/assets/canvasjs-charts.svg" alt="canvasjs" width="40" height="40"/> </a> <a href="https://www.w3schools.com/cpp/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="cplusplus" width="40" height="40"/> </a> <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://cloud.google.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/google_cloud/google_cloud-icon.svg" alt="gcp" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> <a href="https://www.adobe.com/in/products/illustrator.html" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/adobe_illustrator/adobe_illustrator-icon.svg" alt="illustrator" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> </a> <a href="https://www.mathworks.com/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/2/21/Matlab_Logo.png" alt="matlab" width="40" height="40"/> </a> <a href="https://www.mysql.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="40" height="40"/> </a> <a href="https://nodejs.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40"/> </a> <a href="https://opencv.org/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/opencv/opencv-icon.svg" alt="opencv" width="40" height="40"/> </a> <a href="https://www.oracle.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/oracle/oracle-original.svg" alt="oracle" width="40" height="40"/> </a> <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a> <a href="https://www.photoshop.com/en" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/photoshop/photoshop-line.svg" alt="photoshop" width="40" height="40"/> </a> <a href="https://www.php.net" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" alt="php" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://scikit-learn.org/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/> </a> <a href="https://seaborn.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/> </a> <a href="https://www.tensorflow.org" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="tensorflow" width="40" height="40"/> </a> <a href="https://www.typescriptlang.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" alt="typescript" width="40" height="40"/> </a> <a href="https://www.adobe.com/products/xd.html" target="_blank" rel="noreferrer"> <img src="https://cdn.worldvectorlogo.com/logos/adobe-xd.svg" alt="xd" width="40" height="40"/> </a> </p>

<p><img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=richaaa01&show_icons=true&locale=en&layout=compact" alt="richaaa01" /></p>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=richaaa01&show_icons=true&locale=en" alt="richaaa01" /></p>

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=richaaa01&" alt="richaaa01" /></p>

