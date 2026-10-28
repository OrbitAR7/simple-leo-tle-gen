# simple-leo-tle-gen

A small Streamlit app that builds a Walker Delta constellation (i: T/P/F) in circular LEO, writes it out as TLEs, and plots the satellites on a map.

Each satellite gets RAAN = 360°·p/P and mean anomaly = 360°·s/S + 360°·F·p/T, where p is its plane index, s its slot in the plane, S = T/P satellites per plane and F the phasing factor. The epoch is the current UTC time. Mean motion comes from the two-body period at the requested altitude. When SGP4 reads it back, the mean altitude comes out within about 0.3 km of the request, because the TLE mean motion is a Kozai mean element, not a two-body one.

The TLEs are synthetic. The NORAD IDs and international designators are random placeholders, and drag terms are zero. They are meant for loading into SGP4-based tools (STK, GMAT, Skyfield, etc.) to study geometry and coverage, not for tracking real objects.

## Run

```sh
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
streamlit run streamlit_app.py
```

Streamlit prints a local URL (e.g. `http://localhost:8501`).

## Files

- `streamlit_app.py`: UI (altitude, inclination, planes, satellites per plane, F)
- `t_utils.py`: TLE generation, checksums, plots

## Possible extensions

- Walker Star (RAAN spread over 180°) and repeat-ground-track constellations
- J2-consistent mean elements (sun-synchronous inclination for a given altitude)

<img width="1828" height="885" alt="Screenshot 2025-11-13 at 2 23 59 PM" src="https://github.com/user-attachments/assets/4c7d5374-77ee-48ad-9290-11a71ea5af95" />
