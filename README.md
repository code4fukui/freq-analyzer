# freq-analyzer

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A simple, real-time audio frequency analyzer built with the WebAudio API and Chart.js.

## Demo

https://code4fukui.github.io/freq-analyzer/

The application captures microphone input and displays a real-time, multi-line chart representing the intensity of different audio frequency bins. Below the chart, a detailed table shows the current and peak values for each frequency.

## Features

-   **Real-time Analysis**: Captures microphone audio and performs frequency analysis in real-time using the WebAudio API.
-   **Time-Series Chart**: Visualizes the frequency spectrum as a time-series line chart, showing the most recent values for each frequency bin.
-   **Data Table**: Displays the raw FFT value for each frequency bin, alongside the maximum value recorded since the last reset.
-   **Simple Controls**: Includes a checkbox to toggle the data table's visibility and a button to clear the recorded maximum values.

## Usage

1.  Open the [demo page](https://code4fukui.github.io/freq-analyzer/) in a modern web browser.
2.  Allow the page to access your microphone when prompted.
3.  The chart will immediately begin displaying the live frequency spectrum.
4.  The data table is shown by default. Uncheck "enable show value on the table" to hide it.
5.  Click the "clear max value" button to reset the peak values tracked in the table.

## Technical Details

-   **API**: Uses the WebAudio API's `AnalyserNode` to perform a Fast Fourier Transform (FFT) on the audio stream.
-   **Configuration**:
    -   `fftSize`: 32 (resulting in 16 frequency bins)
    -   `smoothingTimeConstant`: 0
-   **Visualization**: The chart is rendered using [Chart.js](https://code4fukui.github.io/Chart-es/Chart.js).

## License

MIT License — see [LICENSE](LICENSE).