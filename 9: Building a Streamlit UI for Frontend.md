```python
import streamlit as st
import requests
from datetime import datetime, timedelta

# API URLs
API_BASE_URL = "http://localhost:8000"
API_URL_FLIGHTS = f"{API_BASE_URL}/search_flights/"
API_URL_HOTELS = f"{API_BASE_URL}/search_hotels/"
API_URL_COMPLETE = f"{API_BASE_URL}/complete_search/"
API_URL_ITINERARY = f"{API_BASE_URL}/generate_itinerary/"
...
