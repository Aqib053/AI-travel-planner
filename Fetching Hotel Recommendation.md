```python
@app.post("/search_hotels/", response_model=AIResponse)
async def get_hotel_recommendations(hotel_request: HotelRequest):
    hotels = await search_hotels(hotel_request)
    hotels_text = format_travel_data("hotels", hotels)
    ai_recommendation = await get_ai_recommendation("hotels", hotels_text)
    return AIResponse(hotels=hotels, ai_hotel_recommendation=ai_recommendation)
