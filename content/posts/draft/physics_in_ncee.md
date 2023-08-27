---
title: "Physics in NCEE"
date: 2022-07-12T01:13:45+08:00
draft: true
math: true
---

## Natural Unit
### Energy
$$E=m_P c^2 = \sqrt{ℏ c G^{-1}} c^2 = 543 \pu{kWh}$$
### Charge
$$q_P = \sqrt{2 \tau ε_0 c ℏ} = 1.87 \pu{aC}$$
### Mass
$$m_P = E c^{-2}$$
### Time
$$t_P = E^{-1} ℏ$$
### Length
$$l_P = E^{-1} c ℏ$$
### Temperature
$$T_P = E k_B^{-1}$$
### Current
$$I_P = E q_P ℏ^{-1}$$
### Resistance
$$R_P = q_P^{-2} ℏ$$
### Frequency
$$f_P = E ℏ^{-1}$$
### Force
$$F_P = E^2 c^{-1} ℏ^{-1}$$
### Pressure
$$P_P = E^4 c^{-3} ℏ^{-3}$$
### Power
$$P_P = E^2 ℏ^{-1}$$
### Voltage
$$V_P = E q_P^{-1}$$
### Capacitance
$$C_P = E^{-1} q_P^2$$
### Conductance
$$G_P = q_P^2 ℏ^{-1}$$
### Magnetic flux
$$φ_P = q_P^{-1} ℏ$$
### Magnetic induction
$$B_P = E^2 q_P^{-1} c^{-2} ℏ^{-1}$$
### Electrical inductance
$$L_P = E^{-1} q_P^{-2} ℏ^2$$

| Physical Quantity     | Symbol  | $$E$$ | $$q_P$$ | $$ℏ$$ | $$c$$ | $$k_B$$ |
|-----------------------|---------|-------|---------|-------|-------|---------|
| Mass                  | $$m_P$$ | 1     | 0       | 0     | -2    | 0       |
| Time                  | $$t_P$$ | -1    | 0       | 1     | 0     | 0       |
| Length                | $$l_P$$ | -1    | 0       | 1     | 1     | 0       |
| Temperature           | $$T_P$$ | 1     | 0       | 0     | 0     | -1      |
| Current               | $$I_P$$ | 1     | 1       | -1    | 0     | 0       |
| Resistance            | $$R_P$$ | 0     | -2      | 1     | 0     | 0       |
| Frequency             | $$f_P$$ | 1     | 0       | -1    | 0     | 0       |
| Force                 | $$F_P$$ | 2     | 0       | -1    | -1    | 0       |
| Pressure              | $$P_P$$ | 4     | 0       | -3    | -3    | 0       |
| Power                 | $$P_P$$ | 2     | 0       | -1    | 0     | 0       |
| Voltage               | $$V_P$$ | 1     | -1      | 0     | 0     | 0       |
| Capacitance           | $$C_P$$ | -1    | 2       | 0     | 0     | 0       |
| Conductance           | $$G_P$$ | 0     | 2       | -1    | 0     | 0       |
| Magnetic flux         | $$φ_P$$ | 0     | -1      | 1     | 0     | 0       |
| Magnetic induction    | $$B_P$$ | 2     | -1      | -1    | -2    | 0       |
| Electrical inductance | $$L_P$$ | -1    | -2      | 2     | 0     | 0       |

## Uniform acceleration

|$$     $$|$$ a,t,v              $$|$$ a,t,v_0              $$|$$ a,t,x                     $$|$$ a,v,v_0              $$|$$ a,v,x                   $$|$$ a,v_0,x                        $$|$$ t,v,v_0          $$|$$ t,v,x              $$|$$ t,v_0,x              $$|$$ v,v_0,x              $$|
|---------|------------------------|--------------------------|-------------------------------|--------------------------|-----------------------------|------------------------------------|----------------------|------------------------|--------------------------|--------------------------|
|$$ a   $$|$$ a                  $$|$$ a                    $$|$$ a                         $$|$$ a                    $$|$$ a                       $$|$$ a                              $$|$$ \frac{v-v_0}{t}   $$|$$ \frac{2vt-2x}{t^2} $$|$$ \frac{2x-2v_0t}{t^2} $$|$$ \frac{v^2-v_0^2}{2x} $$|
|$$ t   $$|$$ t                  $$|$$ t                    $$|$$ t                         $$|$$ \frac{v-v_0}{a}      $$|$$ \sqrt{\frac{2vt-2x}{a}} $$|$$ \frac{\sqrt{v_0^2+2ax}-v_0}{a} $$|$$ t                $$|$$ t                  $$|$$ t                    $$|$$ \frac{2x}{v_0+v}     $$|
|$$ v   $$|$$ v                  $$|$$ v_0+at               $$|$$ \frac{1}{2}at+\frac{x}{t} $$|$$ v                    $$|$$ v                       $$|$$ \sqrt{2ax+v_0^2}               $$|$$ v                $$|$$ v                  $$|$$ \frac{2x}{t}-v_0     $$|$$ v                    $$|
|$$ v_0 $$|$$ v-at               $$|$$ v_0                  $$|$$ \frac{x}{t}-\frac{1}{2}at $$|$$ v_0                  $$|$$ \sqrt{v^2-2ax}          $$|$$ v_0                            $$|$$ v_0              $$|$$ \frac{2x}{t}-v     $$|$$ v_0                  $$|$$ v_0                  $$|
|$$ x   $$|$$ vt-\frac{1}{2}at^2 $$|$$ v_0t+\frac{1}{2}at^2 $$|$$ x                         $$|$$ \frac{v^2-v_0^2}{2a} $$|$$ x                       $$|$$ x                              $$|$$ \frac{v+v_0}{2}t $$|$$ x                  $$|$$ x                    $$|$$ x                    $$|

## Force

$$G=mg$$
$$F=fx$$
$$F=\mu F_N$$
$$F=G\frac{Mm}{r^2}$$
$$F=m\frac{v^2}{r}=m\omega^2 r=m\frac{\tau^2}{T^2}r$$

$$v_{a}'=\left(\frac{m_a-m_b}{m_a+m_b}\right)v_a+\left(\frac{2m_b}{m_a+m_b}\right)v_b$$
$$v_{b}'=\left(\frac{2m_a}{m_a+m_b}\right)v_a+\left(\frac{m_b-m_a}{m_a+m_b}\right)v_b$$

## Electrical

$$E=\frac{F}{q}$$
$$E=\frac{kQ}{r^2}$$
$$E=\frac{U}{d}$$

$$F=qE$$
$$F=k\frac{q_1q_2}{r^2}$$
$$U_{1,2}=\frac{W_{1,2}}{q}=\varphi_1-\varphi_2$$
$$\varphi=\frac{E_p}{q}$$
$$W=qEd$$
$$W_{AB}=qU_{AB}$$
$$C=\frac{Q}{U}$$
$$C=\frac{\varepsilon_r S}{2\tau kd}$$
$$E=E_1+E_2$$
$$I=\frac{q}{t}=\frac{E}{R+r}=\frac{U}{R}$$
$$U=E-Ir$$
$$Q=I^2Rt$$
$$W=UIt$$
$$R=\rho\frac{L}{S}$$
$$\rho=\frac{RS}{L}$$

## Magnetism
$$B=\frac{F}{IL}$$
$$B=\frac{\Phi}{S}$$
$$F=BIL\sin\theta$$
$$F=qvB$$
$$r=\frac{mv}{qB}$$
$$T=\frac{\tau m}{qB}$$
$$E=n\frac{\Delta \Phi}{\Delta t}$$
$$E=BLv\sin\theta$$
$$E=\frac{B\theta L^2}{2}$$
$$E=nBS\theta\sin\theta t$$

## AC

$$E_m=nBS\theta$$
$$E=\frac{1}{\sqrt{2}}nBS\theta$$
$$\bar{E}=n\frac{\Delta\Phi}{\Delta t}$$
$$E'=nBS\omega\sin\theta t$$
$$\frac{U_1}{U_2}=\frac{n_1}{n_2}$$
$$P_\text{in}=P_\text{out}$$
$$f_1=f_2$$
$$I_1n_1=I_2n_2$$
$$P_\text{loss}=\frac{P^2 R}{U^2}$$

## Thermodynamics

$$\frac{p_1 V_1}{T_1}=\frac{p_2 V_2}{T_2}$$

## Wave

$$T=\tau \sqrt{\frac{L}{g}}$$

$$T=\tau \frac{m}{k}$$
$$v=f\lambda=\frac{\lambda}{T}$$
$$T=\tau\sqrt{LC}$$
$$\lambda = \frac{c}{f}=cT$$
$$p=mv$$
$$I=Ft$$
$$Ft=mv_2-mv_1$$
$$v_1'=\frac{m_1-m_2}{m_1+m_2}v_1+\frac{2m_2}{m_1+m_2}v_2$$
$$v_2'=\frac{m_2-m_1}{m_1+m_2}v_2+\frac{2m_1}{m_1+m_2}v_2$$
$$v=\frac{m_1v_1+m_2v_2}{m_1+m_2}$$

## Optical

$$n_{1,2}=\frac{\sin\theta_1}{sin\theta_2}$$
$$n=\frac{\sin i}{sin r}=\frac{c}{v}$$
$$\sin C = \frac{1}{n}$$
$$E=h\nu$$
$$p=\frac{h}{\lambda}$$
$$\Delta x=L\frac{\lambda}{d}$$
$$h\nu=W_0+\frac{1}{2}mv^2$$
$$E_n=\frac{E_1}{n^2}$$
$$E_1=-13.6\pu{eV}$$
$$E_\text{high}-E_\text{low}=h\nu$$
$$r_n=n^2 r_1$$
$$N=\frac{n(n-1)}{2}$$
$$m'=m\left(\frac{1}{2}\right)^{\frac{t}{T}}$$
$$m'=m\exp\left(-\ln 2 \frac{t}{T}\right)$$
$$E=mc^2$$
$$\Delta E=(m-m')c^2$$
