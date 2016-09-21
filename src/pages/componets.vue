<template>
<div id="container">
    <div class="nav">
      <header>
        <a href="/" class="nav-logo" alt="egg"><img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAOUAAAAcCAYAAACeVHjHAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAABmJLR0QAAAAAAAD5Q7t/AAAACXBIWXMAAAsSAAALEgHS3X78AAAK60lEQVR42u2cf4xcVRXHP6etUCo2TBECNbEwJZEGS4lbEtBEE51ixBhi4hh+RI1otoY/NERxNySaaER2o/4hf4i7+o8kCNlRoiE16q4QREODuwkGDf7RnYKURAR3SIHyo4Wvf9xzO3ffvpl9M7Ozg3W+yWTeuz/O/fHOuefcc8978BaBpOvVxLsH3Z8hhhgUNkkayaQdB44Cz5jZ8bVoRNKZwLnAWYAlWUtmdjinym5J5yT3LwINM3uuXxMhaSOwHdgKbE7zzGyhH20uLS1p27Zt1julIU4pqDVelzQv6VuSLuiC7pWS7pR0qE0bdyflr9fqeF7SLyRVJb1tDcZ+jqSbJT0s6dVWjfZr7peWlvpGe4j/YRQQBEk6LmlK0tkF6O2R9FBBup0KZYrDkqpdjnmLpNslvVykoX7N/VAoh8jDJmBfTvpW4D3Ax4ErvdwocLWkT5jZY3nEJN0I3Amc5knHgN8CDwBPAq9lqvyrRb9uAP6d3G8EzgeuAK4BzgMuAGYk/RS4qaipLWkHcD+wO0l+zNP+Biytz9QPMUSXkHSRpHslvemK4yVJV+eU+06iXI75/Ts6aKeQo0fSBknXSXoqKf+ApC0F2tgt6dmk3oOS3jeouR2EppRUklTqtE6RtG76st7j77X9buavnwO4VtIrzswvS7osyftywuiHJO3qgn5H3ldJZ0qaSer8SpK1Kb89EcgTkr426DldT6F0ZhpT8BPM+3Uh5pK0qIxD0NNG29QZzfyqmfySpCVJYy3qlxW2TOWc9Czt0Zz6JUmzWunIzI6hTAfwPk11+QxmJVVWK7ehKEEzuxf4CMEk3QLcI+l0SZcA3/Nii8D7zeyJbjrdCczsJeA6IO5LrwFualPlZwQPMMDnzez7/e7joOGMWZU0A8x78j6aW5Z5X9iqrQTUmajRiQfaaY0kvwowkSk2CswBo3ltm1kdqAOzGcGpeN2U/grhNbMGUPP6qwrCOmGSsOVq25+O3fGSvgj8xG9vAa4iPORjwBVm9ng3vZV0PU0B22Fm/yxY73TgUeBS4AXgQjN7IVPmk8B9fvsDMxu4loT+HolImgXKwAKQMn28biRpDQJz181sX4bOjNNoZJoYIzB9PaVjZrWkbtXMaq7JRsxsv6eXgVkC34wCpZiXM44xL7PXzBotaC0CO12Qs/UrwIzXr2fyFoF9LeqVCQtAFlHj13Ly5vJoFe1P15Bkkv7sZuDRxHz8Zo90uw4ekPThpO6tOfmPet6TkjZ3Qruf6Kf56loyz9Sb9V82vZzVWJ62mPzH31LyS9Nnk7qj8d5N5akkbzY1Od2cbmcKV5LrqdTk9b6pnRnaKq+d+er9z45vscW4Y/poC1qlzNyMeZ1c62RTpw/bzCTpNuAAEB05LwN3dEprrWBmD0h6CPgQ8Bngu8kE7AIu99sfmtmrg+rnOs9JwxluhLC6zxG0XWSEEb8e8byFnJV7gubqvzMmSpr3unWvN57ThZgPQWPXve5MQicycQ0Yk3RS06bCYmZznlYhaK+8E4Oq15/OqV9vp/kkpVZAqu0aZrYzLRwXl6xmd63bCiWfg9ifSYWTtug0qsR+QxdC6fgd8B8gnlseyJqMA8DdBKG8WNIOM3vK069KyvxywH1cNyQCGc3Xhl9H5lggMOmC/0acqaPwVD2/lqFbIQhYFOZRIE8oo+lMbD8RyJrXT7GfsDeMfY170LKknU5vCtifLh4ucOPeDyTVWL6HLUna6+1lnUqlWC9Bg+UmeS/PYMJpzWXzzGwyeU4Tkk4uBl0JpZm9Iekg4RwT4OBaDKJHPJxc7wGiUF7m/4eK7lNPQZRpClcqZAs090gnERkFmGb5fhQCE08TBKQBzEkaTVf6pM3IjCMEJ8ccQftELV6KDiT3ko4ne9Jasl/EzOYk7ScIaZ4gTSZ9qMVxRg3mdLMLTMs95Rqh4uNuCV9UJgkLxn7oXlMCpDGrT/dpUJ0gNR/elVxvfwv1cd3gD7tB0yFTJQjhuAvFCEGwagRBSzVQFKJ4DZwU1rILSEyu0RTgFFEDTBAEe4Zgds5G4fJ2oyk6Qb7zJEXUdo2cvJKkmntdBw7X+Km10A41gid80szqvQjlseT66KAnwcyOJ4xyepJ1hv+/OOg+rhecIWYITDFNYOJpAlPHI4hqklcjuOrnCBonapmsRlohfC6gC5LGoknmGGe5lo2m4xxBg0wThLbkgpRq1lwke7Fyuqfzflb7IJClnL1iydus5KUnqBC82XWtchbqZeLCOdmLUL4zud7eNZU1gqSzkttUAGPY3HmD7uN6wTVh3OdVCAIxSVMw8euoraZpClsuYzvjl3LMVJz2rGuquvchCnaJwLCpUE64gNWBiv9T0IycJmiVETNbcIYfAz7dh6lssNL8bHUkkt2vxj13W/g+e7/Tm6JHobwkue4oKqJPSGNZDyXX0czeKWmjmb0x6I6uE+LBOjS9rCM0BTPraCkTPKkrhNK1whgwnWiOEsFjOkZwZkTB3Od5VW+jTOIIcs0avY5zSZm2Zp6kspnVfcGJTqFxXHuvFtyQ3cMWQNz/ZvehIz6O6Ux6dKRFVPE9YoHnVPJ5aUiqFo7oyXTgHJY/1Ku6obPG+Kj/H6cZvQLwiP+fTQiu/39BnaYnMfW8NjJ5adlW5l+F5mo+6b9Gcj/tTBoZNdXGe7OMTdOErXmZFV7enPbnoxnoRyQ1QgDCQsZsblV/hg7gC8Bqe9y0fC3xXMcoqLaaMi4UybxPUmwPmkvs61qJPV0Ra9LsJXjgDElHvO6BTN5WNWN2pzuh22/0OXig7Ify8eC/5PelTJ78PxvOFg/Qp1rQbxv7mtOXJbUIbG91kJ70bzHu4dSMiV2SNOF5K8LsMv1cytkD9jX2NaUbn0FOmUpeeseaUuGdylv8dh54ya9v75TWGuIrND2uP04zzOwocI/ffk7SxQPs53oiMmH0fs7S3NuN+fVEUqZMMEfX7A2IJJJnimac67JIGAIPlQiacFHLA9ej82cfzXPOaAXt9aCFvTRjZGeUBKAnZ557V9Naa43M/rjh/cmOfYaVXuuOJ9kU3vyXwqtcH5R0W6Lhbu6BdleaUtKlar6sfFA5b4r4ShW15V9V4DWv9UCfNWUaQldREkbn17m/DI0RtQ4dG1ObNzDS+pFGoqULtZ+hVfE2W2nEUrv8NmPo9DW2uI/u9Hnkjb23BVDSRkk/SgQnhjNtkfSEp52QdG2X9DsWSoV3PZ/2Oq+0M6EljSf0D0h6e08TsgYYfnlgiK4h6XxJv0mY+mCqbSS9V9ILiQb9tqTTOmyj0/cpP6XwzZ7Y5g2rlDdJv07amJd00SDndSiUQ3QMSTtcwF5MmPkRSdtyyl4u6bmk3GFJX1DBrw8UEUpJm9yMeTApe0LSlwq2sVnSfUnd1137d/xS9lpgKJRD5MGURO0n2AzsAlJNIsL3d77a6k0LF6afAx9Ikk8A/wCOsDKq5k9mdofXTd+nPMDyiCEI3+i5lPD9oIhngBvN7PdFByxpA3Ar8A2a3xKKtA4DzwJvLpsks34cTA8/MTlEPrQ63nDT9YqC9DZI+qykvxeg3e3X7J5X+PRl4W8A5fRzl6R7XFu2Rb/mfqgph8jDJlYeVorgwj0C/IXwWlbhtyvM7E3gLuAuSZcTXPN7CJ/i2JopfrgFmceB15P7Vwjhck8AfwT+YGav0QP8kyXXSToX+BjhS3kXEj4Y3Uuk0xBDnBro1NEzxBCnKv4Lt2F3A2rSh5IAAAAASUVORK5CYII="></a>
        <ul>
          <li>
            <a is-link="" href="#!/version">
          版本
      </a>
          </li>
          <li>
            <a is-link="" href="#!/tool">
          工具
      </a>
          </li>
          <li>
            <a is-link="" href="#!/componets">
          组件
      </a>
          </li>
          <li>
            <a is-link="" href="#!/rule">
          规范
      </a>
          </li>
        </ul>
      </header>
    </div>
    <div class="page-title center">
      <h1>组件</h1>
      <h2>Knowing about the past,Looking to the future</h2>
    </div>
    <div class="page-main">
      <div class="markdown-body">
      <iframe src="https://x-xdc.github.io/xdc-ui-docs/#!/zh-cn" frameborder="0" width="100%" height="800px"></iframe>
      </div>
    </div>
    <div class="footer">
      <footer>
        <ul>
          <li><a href="/guide/" alt="Guide">Guide</a></li>
          <li><a href="https://xdc.party/" alt="Plugins">Plugins</a></li>
          <li><a href="/release/" alt="Release">Release</a></li>
        </ul>
        <div class="license">Released under the MIT License </div>
      </footer>
    </div>
  </div>
  <div id="feedly-mini" title="feedly Mini tookit"></div>
  <div id="chrome_websiteIP" class="chrome_websiteIP_right">47.88.240.14</div>
</template>

<script type="text/babel">
  import '../font/iconfont.css';

  export default {
    data() {
      return {
        smallScreen: true,
        isMobile: false,
        logoAnimateReady: false,
        descAnimateReady: false
      };
    },

    methods: {
      handleResize() {
        this.smallScreen = document.body.clientWidth <= 650;
      }
    },

    compiled() {
      this.logoAnimateReady = true;
      setTimeout(() => {
        this.descAnimateReady = true;
      }, 500);
      this.handleResize();
      window.addEventListener('resize', () => {
        this.handleResize();
      });
      this.isMobile = document.body.clientWidth <= 500;
    },

    beforeDestroy() {
      window.removeEventListener('resize', () => {
        this.handleResize();
      });
    }
  };
</script>
