# Double-Sideband-Modulation
1.1 I NTRODUCTION
Double Sideband modulation is the easiest and most direct type of analog modulation. In this scheme, the
modulated signal is obtained using a direct multiplication of the modulating signal (i.e. the message) by a cosine
carrier. This multiplication results in shifting the entire spectrum of the message to a center frequency defined
by the carrier frequency. The modulation is said to be double sideband transmitted carrier (DSB-TC) when the
carrier is transmitted along the modulation term. If the carrier term is omitted, the modulation is termed
double sideband suppressed carrier (DSB-SC). DSB-TC has a significant advantage in the receiver design (i.e.
the envelop detector). Also transmitting the carrier independently enables us to extract useful information
such as the carrier frequency which can be helpful for carrier synchronization. However, the DSB-TC loses to
the other variant (i.e. the SC) in terms of power efficiency.
1.2 A IM
In this experiment, you’re required to achieve the following:
1.
2.
3.
4.
Get familiar with the concept of DSB modulation, and its parameters.
Study the performance of the DSB modulation.
Examine different detectors (coherent detector, envelope detector).
Study the performance of coherent detection in the presence of frequency or phase mismatch.
1.3 P ROCEDURE
1. Use Matlab to read the attached audio file, which has a sampling frequency Fs= 48 KHz. Find the
spectrum of this signal (the signal in frequency domain).
[audioread, fft , fftshift , plot]
2. Using an ideal Filter, remove all frequencies greater than 4 KHz.
3. Obtain the filtered signal in time domain and frequency domain, this is a band limited signal of BW=4
KHz. [ifftshift ,ifft]
4. sound the filtered audio signal (make sure that there is only a small error in the filtered signal)
[sound]
5. Modulate the carrier with the filtered signal you obtained, you are required to generate both types
of modulation (DSB-TC and DSB-SC). Choose a carrier frequency of 100 KHz. For the DSB-TC take the
DC bias added to message before modulation to be twice the maximum of the message (modulation
index =0.5 in this case).
Note: You will also need to increase the sampling frequency of the filtered audio signal, the
sampling frequency must be at least 2 times the carrier frequency, In this simulation use
Fs = 5 𝐹 𝑐 .
[ resample]
You have to sketch the modulated signal of both DSB-TC & DSB-SC in frequency domain.6. For both types of modulations (DSB-SC & DSB-TC), use envelop detector to receive the message
(assume no noise). Note: to obtain the envelope you can use the following matlab command.
𝑒𝑛𝑣𝑒𝑙𝑜𝑝𝑒 = 𝑎𝑏𝑠(ℎ𝑖𝑙𝑏𝑒𝑟𝑡(𝑚𝑜𝑑𝑢𝑙𝑎𝑡𝑒𝑑 𝑠𝑖𝑔𝑛𝑎𝑙))
7. After the reception of both modulation types using envelope detector, sketch the received
signal in time domain, and Play the received signal back (Note: to sound signal after
demodulation process you have to decrease the sampling frequency again). What
observation can you make of this or which type of modulation the envelope detector can be
used with?
For DSB-SC, perform steps 9-11.
8. Use coherent detection to receive the modulated signal with SNR=0, 10, 30 dB then sound the
received signals and plot them in both time and frequency domain.
9. Repeat the coherent detection with frequency error, F=100.1 KHz instead of 100 KHz and Find
the error. Do you have a name for this phenomenon?
10. Repeat the coherent detection with phase error = 20 0 .
1.4 U SEFUL M ATLAB FUNCTIONS
audioread,fft, fftshift, ifft, ifftshift , plot, awgn, resample, sound, hilbert, abs, max.
1.5 HINT
You are not allowed to use built in functions like ammod, amdemod
