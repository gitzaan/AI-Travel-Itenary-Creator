# TravelMapper

TravelMapper is a travel agent application that uses OpenAI, Google Gemini, and Google Maps APIs to create and map travel itineraries based on user input. It features a user-friendly interface hosted on Gradio for interactive experiences.

This project is an implementation of the Medium article by Martin Short: [Building a Smart Travel Itinerary Suggester with Langchain, Google Maps API, and Gradio](https://medium.com/towards-data-science/building-a-smart-travel-itinerary-suggester-with-langchain-google-maps-api-and-gradio-part-1-4175ff480b74).

## Features

- **Travel Itinerary Generation**: Enter a travel request, choose the model to use, and generate a detailed itinerary along with a map showing the suggested route.
- 
- **Basic Error Handling**: If an unrealistic request is entered, the application provides an explanation and may suggest alternatives.

- **Extended Trip Generation**: Generate trips with more stops than the Google Maps API query limit (25 waypoints). The application handles this by breaking the route into segments and sending multiple requests.


## Getting Started

### Create a `.env` File

Create a `.env` file in the top-level directory (i.e., `travel_mapper`) with the following content:

```
OPENAI_API_KEY={your_openai_key}
GOOGLE_MAPS_API_KEY={your_google_maps_api_key}
GOOGLE_PALM_API_KEY={your_google_palm_api_key}
```

### Install Dependencies

Make sure to install the required Python packages.
`pip install -r requirements.txt
`

### Running the Gradio App

To start the Gradio app, run the module for the user interface.
```python -m travel_mapper.user_interface.driver```
Alternatively, use the provided `run` script, ensuring it has execution permissions.
```travel_mapper/user_interface/run.sh```

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

