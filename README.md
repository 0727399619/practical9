<Doctype html>
    <html lang="en">
        <head>
            <script>
                function formatDate(date){
                       let minutes=date.getMinutes();
                       let hours=date.getHours();
                       let days=["Monday","Tuesday","Wednesday","Thursday","Friday","Saturday","Sunday"]
                       let day=days[date.getDay()];
                       if(minutes<10){
                        minutes='0${minutes}';
                       }
                       return '${day}${hours}:${minutes}';
                }
                function searchCity(currentcityName){
                    let apiKey="73dof19a030ad06t05b21e8521b4860f";
                    let apiurl='http://api.shecodes.io/weather/v1/current?query=${currentcityName}&key=${apikey}';
                }
                  function displayCity(event){
                    event.preventDefault();
                    let cityName=document.querySelector("#city-name");
                    let cityNamedisplayed=document.querySelector("h3");
                    cityNamedisplayed.innerHTML=cityName.value;
                     currentcityname=cityName.value 
                     searchCity(currentcityname);
                  }
                  let searchForm=document.querySelector("#search-form");
                  searchForm.addEventListener("submit",displayCity);
                
                
            </script>
            <style>
                body{
                    background-color: #f9f7fe;

                }
                a{
                    color: rgb(123,3,123);

                }
                header{
                    padding: 0 0 10px 0;
                    border-top: 5px solid rgb(175,172,172);
                    text-align: center;
                    text-decoration: underline;
                }
                h3{
                    padding: 40px 0 0 0;
                    border-top: 5px solid rgb(175,172,172);
                    font-size: 30px;
                    line-height: 30px;
                    text-transform: capitalize;
                }
                .weather-app{
                    background-color: rgb(175,172,172);
                    max-width: 600px;
                    margin: 100px auto;
                    padding: 30px;
                    border-radius: 30px;
                }
                h2{
                    color: rgb(81,49,10);
                }
                .weather-app-temperature-container{
                       display: flex;
                       padding: 40px 0 0 0;
                       border-top: 30px solid rgb(175,172,172);
                       line-height: 30px;
                       text-transform: capitalize;
                }
                .weather-data{
                    display: flex;
                    justify-content: space-between;
                }
                .weather-app-icon{
                    height: 80px;
                    width: 80px;
                    line-height: 20px;
                    padding-bottom: 10px;
                    margin-top: 3px;
                }
                .weather-app-temperature{
                    font-size: 80px;
                    margin-left: 10px;
                    font-weight: bold;
                }
                .weather-app-unit{
                    margin-top: 16px;
                    font-size: 28px;
                }
                .Humidity{
                    color: rgb(123,3,123);
                    font-weight: bold;
                }
                .form-input{
                    text-decoration: solid;
                    border: none;
                    width: 70%;
                    border-color: blueviolet;
                    border-radius: 5px;
                    font-size: 20px;
                    padding: 10px 15px;
                }
                .form-button{
                    border: none;
                    background-color: rgb(123,3,123);
                    color: whitesmoke;
                    padding: 10px 15px;
                    font-size: 20px;
                    text-transform: uppercase;
                    margin-left: 5px;
                    border-radius: 9px;
                }
                footer{
                    padding: 0 0 10px 0;
                    border-top: 5solid rgb(175,172,172) ;
                    text-align: center;
                    color: rgb(0 0 0 0.5);
                    font-size: 13px;
                }
            </style>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=devicw-width,initial-scale=1.0">
            <title>Document</title>
            <link rel="stylesheet"hef="styles.css"/>
            <script src="http://unpkg.com/axios@1.6.7/dist/axios.min.js"></script>
        </head>
        <body>
            <div class="weather-app">
                <header>
                    <div>
                        <h2>
                            Welcome to our Weather application</h2>
                    </div>
                </header>

                <main>
                    <div>
                        <form action=""class="search-form"id="search-form">
                            <input type="search"name="city-name"placeholder="Enter city name"
                            equired class="form-input"/>
                   <button type="submit"class="form-button">search</button>
                        </form>
                    </div>
                    <div class="weather-data">
                        <h3>Paris</h3>
                        <h3>
                        🌞18<strong>°c</strong></h3>
                        <div class="weather-app-temperature-container">
                            <div class=""id="weather-app-container">
                                <omg src="http://shecodes.assets.s3.amazonaws.com/api/weather/icon/broken-clouds-day.png"
                                alt="not loading"class="weather-app-icon">
                            </div>
                            <div class="weather-app-temperature"id="currenttemperaturevalue">12</div>
                            <div class="weather-app-unit">°c</div>
                        </div></div>
                        <div>
                            <p>
                                <span id="currenttime">
                                    Tuesday

                                    14.40
                                  ,
                                </span>
                                <span id="weatherdescription">
                                    scattered clouds</span>
                                    <br/>
                                    Humidity:
                                    <span id="Humidity"class="Humidity">
                                        66</span>
                                       , Wind speed:
                                       <span id="windspeed">
                                        4.3
                                       </span>
                            </p>
                        </div>
                </main>
                <footer>
                    <div>
                        Coded by<a href="http://gihub.com/Edward"target="_blank">
                            Edward Sikweya</a>and is on<a href="http://gihub.com/Edward/week7-Weather-API"
                            target="_blank">Github</a>
                            and hosted by
                            <a href="htttp://Edwardweatherapp.netlify.app/"target="_blaank">Netlify.</a>
                            <br>
                            The design was done using<a href="http://www.figma.com/" target="_blank">Figma</a>
                    </div>
                </footer>
            </div>
            <script src="index.js"></script>
         </body>
    </html>
# practical9
