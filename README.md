#SPF Estimator Using Transmittance Data (ISO23675)

This Python tool estimates the **Sun Protection Factor (SPF)** of a sunscreen formulation using **% transmittance data** and a simplified model inspired by **ISO 23675**. It uses mock solar irradiance and erythemal effectiveness values for illustrative purposes.
#Features
- Converts % transmittance to **absorbance**
- Uses mock **Erythemal Action Spectrum (Eλ)** and **Solar Spectrum (Sλ)**
- Calculates SPF using the **numerical integration approach**
- Designed for extensibility and real-world adaptation

#Method Overview (ISO23675)
SPF is estimated using:
SPF=∑(Eλ * Sλ) / ∑(Eλ * Sλ * 10^(-Aλ))
Where:
- **Eλ** = erythemal effectiveness
- **Sλ** = solar irradiance (mock data used here)
- **Aλ** = absorbance, converted from transmittance

#File Structure

---

#Example Input File (`sample_data.csv`)

```csv
Wavelength,Transmittance (%)
290,15.0
291,14.2
...
400,30.5
pip install pandas numpy
Estimated SPF (ISO 23675): 17.34


