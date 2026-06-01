# DN-Side Device Constraints

This document lists the standard linear constraints for DN-side controllable devices used in the case study.

## OLTC

The substation squared voltage is regulated by

\[
v_{0,t,\omega}=1+\Delta V^{\mathrm{OLTC}}\tau_{\omega}^{\mathrm{OLTC}}, \quad \forall t.
\]

where \(\tau_{\omega}^{\mathrm{OLTC}}\in[-\overline{\tau}^{\mathrm{OLTC}},\overline{\tau}^{\mathrm{OLTC}}]\).

## SVG

For each \(k\in\mathcal{N}^{\mathrm{SVG}}\),

\[
-\overline{Q}_{k}^{\mathrm{SVG}}
\le Q_{k,t,\omega}^{\mathrm{SVG}}
\le \overline{Q}_{k}^{\mathrm{SVG}}, \quad \forall t.
\]

## DN-side PV

For each \(k\in\mathcal{N}^{\mathrm{PV}}\),

\[
0 \le P_{k,t,\omega}^{\mathrm{PV}}
\le \overline{P}_{k,t,\omega}^{\mathrm{PV,DN}}, \quad \forall t.
\]

## DN-side ESS

\[
0 \le P_{t,\omega}^{\mathrm{ch,ESS}}
\le \overline{P}^{\mathrm{ch,ESS}} z_{t,\omega}^{\mathrm{ESS}},
\]

\[
0 \le P_{t,\omega}^{\mathrm{dis,ESS}}
\le \overline{P}^{\mathrm{dis,ESS}}(1-z_{t,\omega}^{\mathrm{ESS}}),
\]

\[
E_{t+1,\omega}^{\mathrm{ESS}}
=
E_{t,\omega}^{\mathrm{ESS}}
+\eta^{\mathrm{ch,ESS}}P_{t,\omega}^{\mathrm{ch,ESS}}\Delta t
-\frac{1}{\eta^{\mathrm{dis,ESS}}}P_{t,\omega}^{\mathrm{dis,ESS}}\Delta t.
\]

\[
\underline{E}^{\mathrm{ESS}}
\le E_{t,\omega}^{\mathrm{ESS}}
\le \overline{E}^{\mathrm{ESS}},
\quad
E_{1,\omega}^{\mathrm{ESS}}
=
E_{T+1,\omega}^{\mathrm{ESS}}
=
E^{\mathrm{ESS,init}}.
\]
