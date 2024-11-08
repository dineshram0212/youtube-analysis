# ytanalysis

`ytanalysis` is a Python package designed to analyze YouTube channel statistics using the YouTube Data API. With this package, you can retrieve information about a YouTube channel, including subscriber count, video details, views, likes, comments, and more. It also provides visualization tools to help analyze video views and monthly posting frequency.

## Features

- Retrieve detailed YouTube channel statistics (subscribers, views, total videos, etc.)
- Extract video statistics such as views, likes, and comments
- Export video data to a CSV file for further analysis
- Generate visualizations for top-performing videos and monthly posting frequency

## Installation

To install this package, use `pip`:

```bash
pip install ytanalysis
```

## Prerequisites

You need a YouTube Data API key to use this package. Follow these steps to obtain one:

1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new project (or select an existing one) and navigate to **APIs & Services** > **Library**.
3. Search for "YouTube Data API v3" and enable it for your project.
4. Go to **APIs & Services** > **Credentials** and create an API key.
5. Copy the API key for later use.

## Usage

### Initialization

To initialize the `YTAnalysis` class, replace `YOUR_YOUTUBE_API_KEY` with your actual API key and `CHANNEL_URL` with the YouTube channel URL you want to analyze:

```bash
from ytanalysis import YTAnalysis

api_key = "YOUR_YOUTUBE_API_KEY"
channel_url = "https://www.youtube.com/channel/CHANNEL_ID"

yt = YTAnalysis(channelURL=channel_url, apikey=api_key)
```

### Methods

#### Get Channel Details

```bash
channel_info = yt.getChannelDetail()
print(channel_info)
```

#### Get Video Details

```bash
video_details = yt.getVideoDetail()
print(video_details)
```

#### Export Data to CSV

```bash
yt.export_csv()
```

#### Plot Most Viewed Videos

```bash
yt.plotViews(values=10, mostViewed=True, save=False)
```

#### Plot Monthly Video Counts

```bash
yt.plotVideoCount(save=False)
```

