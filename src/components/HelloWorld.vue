<template>
  <div>
    <div v-if="leadings">
        <skeleton></skeleton>
    </div>
    <div v-else class="main-container">
      <div class="pro-list">
        <div class="list-item"></div>
        <div class="list-item"></div>
        <div class="list-item"></div>
        <div class="list-item"></div>
      </div>
      <div class="pro-list">
        <div class="list-item"></div>
        <div class="list-item"></div>
        <div class="list-item"></div>
        <div class="list-item"></div>
      </div>
      <div class="pro-list">
        <div class="list-item"></div>
        <div class="list-item"></div>
        <div class="list-item"></div>
        <div class="list-item"></div>
      </div>
    </div>
  </div>
</template>
<script>
import skeleton from './hellowWorld.skeleton'
export default {
  data () {
    return {
      leadings: true
    }
  },
  mounted () {
    setTimeout(() => {
      this.leadings = false
    }, 3000)
  },
  components: {
    skeleton
  }
}
</script>
<style rel="stylesheet/scss" lang="scss" scoped>
  .main-container{
    .pro-list{
      display: flex;
      width: 300px;
      margin: 0 auto;
      justify-content: space-between;
      .list-item{
        width: 50px;
        height: 50px;
        border-radius: 100%;
        background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAFAAAABQCAYAAACOEfKtAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyZpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuNi1jMTM4IDc5LjE1OTgyNCwgMjAxNi8wOS8xNC0wMTowOTowMSAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENDIDIwMTcgKFdpbmRvd3MpIiB4bXBNTTpJbnN0YW5jZUlEPSJ4bXAuaWlkOjc0NzE5OTcyNEE4MzExRTg4NUQyODZCQzJGOTkyMTVFIiB4bXBNTTpEb2N1bWVudElEPSJ4bXAuZGlkOjc0NzE5OTczNEE4MzExRTg4NUQyODZCQzJGOTkyMTVFIj4gPHhtcE1NOkRlcml2ZWRGcm9tIHN0UmVmOmluc3RhbmNlSUQ9InhtcC5paWQ6NzQ3MTk5NzA0QTgzMTFFODg1RDI4NkJDMkY5OTIxNUUiIHN0UmVmOmRvY3VtZW50SUQ9InhtcC5kaWQ6NzQ3MTk5NzE0QTgzMTFFODg1RDI4NkJDMkY5OTIxNUUiLz4gPC9yZGY6RGVzY3JpcHRpb24+IDwvcmRmOlJERj4gPC94OnhtcG1ldGE+IDw/eHBhY2tldCBlbmQ9InIiPz6YHrXLAAATa0lEQVR42rxd289dR3X/rePP/j5fU2LXQKDOzYEYVAqtWoQqHkhtCA889KlB6gM0lUAiEqJIXP4DShUq1LRqpSatFKnQF/rQqKmDoH1AkVrsQA1KeglKYhpwfElCaifx5ZvVNXP2PmdmzW/t87lVe6zZZ3/77MvMmnX5rctsi547CkCw+ORdxbCpjue/RYbf0B5vzsPyHAU/Pn5e0AO2fY+1t1u7c/h+i7X91nZZ22PtirWL1l4evs9a+zdr/zp8fw83yPnlM6r+6Pj3MLC6X+N56oaRj+t4vi6/tbonlteKnjtGiIfpY+V4ddPmxq6z9eEXNBPlN6zdZe0Ddtq7sN222+yv3GYy/86f2XChDvdKw37+Tva9ad+byE3t3ynb+wdr37b2LezFq/O+adwXrQg+nuuJ1PzNGUP0/DFOIPYR91AZH4SWC7UhWiZFnqWPWfsIdmA3ttu561gSqxmgVsekep7rRD1hm3bsqu1fKwS9ZNu/tfaX1r6J3ZI6Anqu1OrHmmiO2xb9GOfGzu0JWIuwoOKy4UphM0PE/UwRv9+19mms4RbsHIgmVQ+0IpCwwXhuHokrLXfWn2Ttmh28Wvafte1Xrf25Pf8ivWfNDON+LbrNBPfXDSLsiVMRRNAPAHDiWxHlDHbazn3WPmcEO4Bddny7umuI+Gsg/vX96+co0WuegzYHYm4i68g/sPZHWJfX5sNzuq4jUk1ML75LjlzqQEGvJL2RUEdQr4DP6D22/X0j3CETHWDNXdsp+Uo8xM2+v786axTpJwz6spaIzJVZxBNO297nsUO+3hGoI079nPq7nThprLAQ2jGiep3ygt5s2z81Ub3bFDiKjkN0D7Si6/VaJ8JEV6nTl51UOPEev0fDozhu209gTZ5rxVjnxM7qJLn++mcOBJ31MEOXndUtQZHftu0p47i78QZZEk+J6Dv2n+9XxFF1RJa+D+qtmiwU+uL3NIqlG4ssrP2HSp+vWd9rbk1Df9LSSMz3/b2W0GbWYThvDLxlHYl8RjesPWgdehg3yj6zrZV1mhC/FFj4pnPjRCrRUe4+43UF3lTnKePaStJm2Gfbh+0+DxlnbsyvVcdltTi6iR7uP+MD0WpWCUw5g4MFc63jd4x481llHNvMWq1HKky3wHiuD8lxl+qSM5IuiTj2TeJB8ufIHHcCHx/w48ElZ/nrx746SJMaEVaOBxsRKyJ7q20fNz/hfWUOJQCpDXoXp4ylR/tAP8hUESmwgksOlJYbOwuO3uoupeF9ZUxiY9Oqvx06qNXFvM04LHHmWxbEO2Lb72CP3G4thhydIRhmLzEjJK37BJnWvxTgOsnJx1PguqUaqtV6DreXsc1wpFMpaZwU7Z416wyGNyTjzc7qYds+hr1yU0F6ygaFVuySn7Ho/hNEGycluWcm57WociOYpBVHiONYXRI82djyGLfZWDtLXxkXeB3oOaYZsGbO+3nbe9SI91ZsTAQKKAHIZKRKFyKw/I3oSu/Wqbfg4oyLOv9c+/t6K118axtjHut2G/OCETS8ZtbDAkeUs+a9Zt9yFw4X4qnTURqAWa+IPVRJTqd0kqA9MZO7h7fOKQDg9bOYxW8mt2DFw2XMO3S91aHSQZtZY7ITsZ7An5i1fW/xLBpO1Z7zOkIJNywqxOIHPjAbdIMT1WG1Ss81SEIXlpNCrFRN7NyPfq9t/7ghGDxTZCMi0kKBGnudM6C5DfeWsECj44QTr55FEE+gUd616I6dd0ZHa8IoNzy18UPguzYc5/WtLK12LfJXyu692JkdBSXSMcYDf3q0D5Tm/XPFPTtl3sW+Bc6TyJ1igcnAFex8TKw47nAoDR44AB350epdSg+NXAA1W4gNfcW278JFPMf85VlDvAb34M9M7y2JB6J0VXs/cSEmBETXYsbcNcop4ty/AGeOltRzS6MriWeVpCVaLfbZd74i+wotGnShC6mZtRBgOOGc3oM1fKjE8BrZhxMncbBCKiwn5DoHdjt44vQVA+idPnKguPMm4Aiky76ORE0aWGeZi3IyWuzRjzJdL/qTY21Hz5ew+1PYJ4dKHE+dZU4aAOiJfIiy8L+PbPQYq49SC48Se2cg1eGxwCdXF9BFDYNqTs9huZyh0RwKO4KX5dW6T7Parxs+9xlwOVQuajgGTtkyZQ+K1kOPQRnHCMGH0ofDpu7TeFPeMFXGyqukVIPmasKvlgj3oUIbbRGI6PPHlg+4UOztM7hBDjRhBmogyMzTjJhMBEB9EHXFeXBElorYSeIINsWL7py0wtBleuwzCgG34IJcHLs7c2b/48Z9BxbJHg83GEBuwKv0xgCV3mo40EV7G0ND9JvX1agzdQ4SNRGY2ijJ0rVrggrahsl8JCrvbxZos3+I3izGtHTlXiz7n8G6xHoMzPpVBEqdOujjdqjA9CLAoL3zTg0GnPcivcgq83C8KPtJFg5xklMVr5Vffg/7dVYFExadOGacd+tc94FHUZKPEaobmHJI1HgNwj2XzjCJmyCJvZ7ELK/Ln6jErmUtEd7lrM+9Vtottv3geOta030MOxzFkzhuU6ePpLfSi2iHU8yR1+JduhHe7PlV4B1fN7v316Z7fs0l2SMwjDYClNiEaY9pk+PgxAIPg/i/PtBqAWNOmxF5qUCXs8iBeZHAg9CJ+J9swSvQ3qeVwFrnTybe9hsHK/gi8MN7JtKNQjje53wJd0Y54DATN7DcgZK8fyPOyKUxGvNBE9058VhtR0c8p6CpW0TSg0l645KCeOFIvPzJ++r0bMMZbNKU5EvE9c25bt5YeZ2KhTHZXVReZYXvXui+FH1rqxM9flLfERa90F5X1nhyERGZSDpBeMid9YcBZkp8Idxb6W04yz4X47vz/towkLuwTXgVE8vbsmhtVz1Q678Bs4G4hl1OWHhUeszXNuGvKPri7ikuctOAfo8JlUTmnShf1jnN7MAaXsFBO3ZHke3OSWfAWVrLJkpcM1JLkqo8sNcvPtEehfUXgNerDul1Ghv8VNVVpwtr8XYAe+4f34GbcDAL7i83EZdFqYXHcQQwj1ZPEGSxah9YAgMSZc9IaVhCXyngQ16eOOJy0bWq6Wp0WHjNG8vh/Cv29wZ+JRPw3U0gFcTF8qGgup6lyXSxYIITOdCod8+ZU/lqkDxyTWA/cC+eWBWTVKJW3PU5ar2BX8oEPFwSzA1kYX6lEw+QhE4tMp0uDco0Gv9Z+noXD5e64iPl5W9RiVoX5vdFTxKkI5wkXi0HDmcC3tpXmQqPKNNCIRLyUpL79fgwrAad4kCGP4XED7UPZtByD3FVtVPFRK4fV8tft2UC3tTXBhO9J+Q3H0XpZpHUpSima/pCDhRecDlVtUDrB5mr6UVaSQrDTfhm+fHNmYA39uVgpOI0CSkpI3kEYcWSSqwhwYNRcXrH6c7CYqI2h+ZHvJEIODMhCM0NpXJGu0zAnf0IZDpqy3RRnSsGEYF95tve/NnWw7iez69/c2vnXTG376n7gfP/TPRZUFQZ/d2pnopZNsuRXRn97Q0rAlgwM0V5EundrTqK8r8h3vV8dtgz7vwsccmUJ9Tr0FeaKM9jlRPAnrXi2WmpPghKa8WV30bLAtCHs0AMzP/Hp6607RCF8j4LemxJdWx7febA/2q5T0mUhcxccjOcKu8kOZ2aufaZ++dRlf/rz+XzwJP393UyaaqKok6uuwpVJRVlacFrF9cKASH7qaKlyRn0Cpy6Vi5w8NJ3gRd/ayJz5zyZ9zud94/HSJV/4Bcjij0G53iui6rI6uvnkatX5wRMEdzQPsfbgVMlTnqEsYSAZxLZDqU+uAdYNg6t1ewCGIEPr1Np2uqaWdl5MRPwHA+csrUcJGcKQjQW3GTFl101lcThLAajOpSAOFKjOuEUEC5VolRrBttW/jizVtKYnddAUpWhG8aMB8udSFC5SqpjQwbUoFIVgRRMJf8lCFmRpRNsItbK9kf56+n2IjaoOnxFDAyEVBroRLTFW3Z3T/bxSX2G0bogqK8GC3LFnXV1k89CdDvKgaczAb/fB1KJO+dzsYjOVX4flj9ZLGpR7pqt9IdZ9ZbyUjplQRDGqWPSPqrCHQ6ul+2pTMAnaLgoKo6E93kDke70jfRK3IfO/QT4iDSYqNXZwgkDwMpFQpwnhOMdIeelzidmppzPzsUYLulCKjqZw95hQgFdhtB5K1WVQJcUEo6OKX6LPAXlnlWSiQR7UDXrPZDsdmzDf+BJnB3zwt/uL5Z2fUeKOAwkea5BrZ9Xxi5BlTBdqc/ifxpUNQDTYbkU3F+JJ+aP7x5olpZF5o/OlTop7IYPiQf+L1ubVlvKRMprmf5klpAWY0oLg5Ir+02+up7EA+uVTmEAlYjvnrL398vytryyW3Ky2EdRfIfEFeugKk6UvgQDJO+R0KsJdauHcrtcuX15n4qV9gbCg25fmNmtlIpioeBp022FAy8Vmi3ywlckH3hkmf6rauRSUMPCMnjee2FVn9DW70QQtPzh/XPCvW6+7amvVAiA6Sntc9ihLiM1jT6QqoiLBebL2x7BD4yIpbTjxNH5g9dLovhRXJY+8cJKIhjkqMVEXOUVpjo2EVhtMKkG+eBoZTk4wGflw1Fiy4/x9hJB/TBOjSKcFlbvMft6tnmRRGIYiTnqRNEm4tmwGJy/j9eVzDL6cH0KipcSSaeyF05MLfKp+7CztOcKrUaXeHHS65If95WyTD/5MoyJDFwXPPUltBpXZnUWG7xWkHF4U1yuXMWAET6wuhoYjLodKEf/EP+CND575vzHvzAleWFRpQCiU5L7m4lkbRmblKi/X7RopxJ/H8+j8UnyFg6ViYVAgWQ1xZXumgycbyglvg/WV84ahXqpvBnoy9iOYGmCBJWiIFYVcTDWeweJJHmgDmYQQOsTXCmozlKJ449dkEJ4+vWNZftl476L7WLD5JZ/Ag9gDacXyXYWx6uTSt7idXiMFDKmICKSfM6hhkrSr97UyLJqoNOkP5ZYkaWLU+4q3He60MaVLM86hP9KWQfxBWxokGRxi/pAVqCzgnNWUUrzDtJWdUVhtAggM7XQ6FxMrHUO8OtbyvaL+B5e9QB8RuHCz+RrpguPY0PaCEwiS7OSxgsOPYBWsmw0ubJc+OWlPvLt6w/rAkvhrppXHxBSoEQ4NX8OFsv7mBHvr9ha6Fm/UGXhSn2yLLSbBTPYVWE5YnY6RYg1lD7g6pNVzfsT3AoAH/nWYAFNl3wnpSAMM2bD8Sa8UmgBAplSveC6sV7WXpJnkVfm7EafBmzes6J9FqvzkWulT9bcsVVGzENB5EdPxBKnoEr4m21ywenNZaj3Gfc9E8UoZ23tshPNC3jYRPnB+XphjV0lBCAUEoNTunRBWxhDE/0OISTE+jBt9QUWxNr/Qqn/ewhPGA0mSk5moT+4RPqfwg78U8uJ4upGopXpGkSRmUhLD4lYmqHhdJ0GzljBcREh86snfs7GnMc+tT5lsdAGAbJHydldRn7v3y48XZa/gli7SY50AJZ5KXCvaoJ7sU7CxAJrnQhBKU+WRX3MfTsgGfM9XcZ8MpeTa+ydLFy5Zs0Zeuv4gpER5kDv1eeXL55gFftONyp5FxWCKC/zFCinBJPF0ERiLqLj0LrUeH8R3efLWE+WMfOgQyfCICF5Lzo/LbNyzADlj8sLKCDconoXjL3bpXt5xMS6EwTBiykj0KUmV/i5o6dxs40tj/FkGevqwGrz3pimAqtaTV6vbvwJnsqFZtinT1rja84Q5CL8YprQMgYigy1ES3AdRK/331rA8pNlbCfLGFfr0MYKK3m7j38Fyoi//rPM0vvNMj9eWH62wloC/BVyiJLxlQVd5TVMcUn0Nqb6t8w+txWw/HgZ00kb26pnIHLlmhVHnohOrH6MHG+/yxD6AzioGIvjwlo7TFnBAAtCt4bdplwwTExqju3dWaztA2UsJ2xMq6I29C2+jx3dQvUSiZakIfl8CL9pxx7Cz6wrL6/yM4NFiSxiLBFO0zgKjajqwXHPm6y92XoruBcn5RvheWylPgXSDEMlkHcaoF/C+iz+xm7+biPf8YKfNkh6UifeCwMfgdE4yh0FRz10SQEezA7BkYLzjtuj32Nc943Ykq/g7AUHHj/aO+3h+5V1OsdwGz5q2y/hkvHlBYxv/5moxZvgsOi1nzpxLNrPQZGbNIvr6RJpOoGvhfcTTBe7dxxY+6hwL8iBtjNau1fsZTg/Kh2707yWzxsJzxdosM7C8my2g1d9IqgoxQTnjC17T3kVzDv0vBHvC6VvI/F8zY9MTNDER/TRoyRTFSw4Thpzgv++o7zP917kF3G/jltMR6LENa6tKhhCjAOxhfNytc8bML6NPwdEvlrC8CdyJS65p6zgwpUE/LtjffUmK/2/rrRkNSFvR/sq+EvGFxft94v2+2XwhdK+UkonlPqYLdtbosZZz12y35avgj/hijh0wkhEnKcIq2ZFHzk6UVDoLaJM68NVUd4jGP8zgtw+gE38Il6zu+cFzDkffWV4hfs1LP/DAQx4TQbu2j4U96wPBmu33X0bfoD5f0bwrdJO5v+MILCgrF/XwXGcgBpFb7eYrN5KAeO47LTu7DuR34yZ/zuMt6H/7zB2L8p4UEopcsumKfuq43+H8e/I/x3GE0OZ8laIhf85sdjnvwUYADMnaYqt+Pq+AAAAAElFTkSuQmCC) no-repeat;
        margin: 10px 0;
        background-size: contain;
      }
    }
  }
</style>
