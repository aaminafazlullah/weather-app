1. What the app does:
A simple web app that lets users search for current weather conditions by city name. 
Built with Python and Flask, containerized with Docker.

2. Prerequisites:
-Python 3.11+ (Flask)
-Docker
-A free API key from OpenWeatherMap

3. How to run locally:
```
git clone https://github.com/Swethasreekumar1234/weather-app.git
cd weather-app
pip install -r requirements.txt
python app.py
```
Then open http://localhost:500 in your browser.

4. How to run with Docker:
```
docker pull aaminafazlullah/weather-app:latest
docker run -p 5000:5000 -e API_KEY=your_api_key_here aaminafazlullah/weather-app:latest
```
Then open http://localhost:5000 in your browser.

5. CI/CD Pipeline
This repo uses GitHub Actions with a 3-stage pipeline that runs automatically on every push to main:
1. **Checkout** — clones the repository onto a GitHub-hosted machine
2. **Build** — sets up Python, installs dependencies, and runs a smoke test
3. **Docker push** — builds the Docker image and pushes it to DockerHub

6. Environment Variables
Variable : Description 

| `API_KEY` | Your OpenWeatherMap API key |

7. DockerHub Image
https://hub.docker.com/r/aaminafazlullah/weather-app

<!----pipeline verified--->

