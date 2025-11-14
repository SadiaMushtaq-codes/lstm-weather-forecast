# lstm-weather-forecast
Real-time weather forecasting using Bidirectional LSTM + MPI4Py + Streamlit dashboard
# SkyNet – AI Weather Forecaster (Talent Festival Demo)

**Live Demo:** https://your-streamlit-app.streamlit.app  
**GitHub:** https://github.com/yourname/skynet-weather

## Features
- Multivariate **Bi-LSTM** with uncertainty
- **MPI4Py** parallel training (4× speedup)
- Real-time **OpenWeatherMap** data
- Interactive **Streamlit** dashboard + **Folium** map
- Full evaluation vs ARIMA baseline

## Quick Start

```bash
# 1. Clone
git clone https://github.com/yourname/skynet-weather.git
cd skynet-weather

# 2. Install
pip install -r requirements.txt
# (for MPI) sudo apt-get install openmpi-bin libopenmpi-dev   # Ubuntu

# 3. Generate sample data
python generate_sample_data.py

# 4. Train (serial first)
python train_lstm.py

# 5. Benchmark speedup
python mpi_speed_test.py

# 6. Run dashboard
streamlit run app.py
