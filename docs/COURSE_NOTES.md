# Course notes — what the slides and tutorial cover

## Module 5 (31 slides): Frequency response & Fourier series
1. Signals as time waveforms vs. frequency content (mass–spring example).
2. The **everlasting exponential** e^{st} is an eigenfunction of LTI systems: output = H(s)·e^{st}.
   For s = jω, H(jω) is the **frequency response** (amplitude and phase plots).
3. Frequency spectrum, spectral components, **bandwidth**, MP3 as an application.
4. **Fourier series**: any (nice) periodic signal = sum of harmonics. Trigonometric form (a₀, aₙ, bₙ),
   symmetry (even → cosines, odd → sines), compact exponential form, worked square/triangle examples.
5. Convergence by adding terms (Gibbs phenomenon); triangle wave = integral of square wave.
6. **System response to a periodic input**: scale each harmonic by |H(jkω₀)| and shift by ∠H(jkω₀).
   LTI systems cannot create new frequencies. Ideal delay, speech/vocal-tract filtering example.

→ Used in Lab 2 post-lab Parts B and C.

## Module 6 (34 slides): Fourier transform & filtering
1. From periodic to aperiodic: the Fourier transform X(ω) and its inverse; Hz vs rad/s.
2. Amplitude and phase spectra, transform of rectangular pulse / impulse / shifted impulse.
3. Properties: linearity, duality, scaling (wide in time ⇔ narrow in frequency), shifting, time convolution,
   frequency convolution, time integration.
4. **Y(ω) = H(ω)·X(ω)**: convolution in time ⇔ multiplication in frequency; impulse response ↔ frequency response.
5. Distortionless transmission, ideal filters, causal/realisable filters, filter design by truncating h(t).
6. Windowing, spectral spread and leakage, energy and bandwidth (e.g. 95% energy band), sample MATLAB code.

→ Used in Lab 2 post-lab A(c) (plot amplitude and phase response in MATLAB).

## Tute 5 Q6
Prove that input e^{st} gives output H(s)e^{st} with H(s) = ∫h(τ)e^{−sτ}dτ, then find H(s) from a
first-order differential equation by substituting the input and output into the equation.
This is exactly the technique used to get H(jω) = 1/(1 + jωRC) in Lab 2.

## How it all connects
Lab 1 (Fourier series, measure spectra) → Module 5 (response of a system to harmonics) →
Lab 2 (predict and measure the RC filter's effect on sine and square waves) → Module 6 (frequency-domain view of filtering).
