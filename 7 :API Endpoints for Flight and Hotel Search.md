```python
from fastapi import FastAPI
from pydantic import BaseModel

@app.post("/search_flights/", response_model=AIResponse)
async def get_flight_recommendations(flight_request: FlightRequest):
    flights = await search_flights(flight_request)
    flights_text = format_travel_data("flights", flights)
    ai_recommendation = await get_ai_recommendation("flights", flights_text)
    return AIResponse(flights=flights, ai_flight_recommendation=ai_recommendation)
