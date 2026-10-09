# Natal Chart for Gemini CLI

Connect Gemini CLI to the public [natalchart.co](https://natalchart.co/ai/) MCP server. It calculates natal charts, current planetary positions and synastry from the birth details or date supplied in the conversation.

## Install

```sh
gemini extensions install https://github.com/DiegoGarcimartin/natal-chart-gemini
```

Restart Gemini CLI after installation, then run `/extensions list` or `/mcp` to confirm that `natal-chart` is connected.

## Available tools

- `calculate_natal_chart`: planetary placements, Ascendant, houses, aspects and a written reading. Unknown birth time is supported, but the Ascendant and houses are then omitted.
- `get_planet_positions`: planetary positions and retrogrades now or at a supplied date.
- `compare_charts`: placements and cross-chart aspects for two birth charts.

Natal-chart results include `full_chart_url`. Open that link to see the interactive chart wheel and full reading on natalchart.co.

Try:

- “Calculate my natal chart: 2 November 1987, 06:15, Valladolid, Spain.”
- “Where are the planets now, and which are retrograde?”
- “Compare these two birth charts.”

## Data and limits

The extension connects directly to `https://natalchart.co/mcp` over Streamable HTTP. It needs no natalchart.co account, API key or local executable.

The first-party natalchart.co service receives the birth details or date needed for each calculation. It computes the result on demand and does not store names, birth data or chart results. It records limited operational telemetry without birth data, as described in the [privacy policy](https://natalchart.co/privacy/). Your Gemini provider may process the conversation under its own terms and privacy policy; this extension does not control that processing.

Planetary calculations use an astronomical ephemeris and historical time-zone rules. Astrological readings are symbolic interpretations, not scientific, medical, financial or predictive advice.

Documentation: [natalchart.co/ai](https://natalchart.co/ai/) · Support: [hello@natalchart.co](mailto:hello@natalchart.co)
