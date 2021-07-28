# QUIC and SATCOM 


# QUIC and SATCOM literature overview

## How Quick Is QUIC in Satellite Networks
- 2018-06
- Han Zhang, Tianqi Wang, Yue Tu, Kanglian Zhao, Wenfeng Li
- https://doi.org/10.1007/978-981-10-6571-2_47
- QUIC version: gQUIC Q039
  - Client: Google Chromium
  - Server: Google quic test server (was part of proto-quic)
  - Parameters/Features: CUBIC, 0-RTT, MUX
- Emulation
  - RTT {200 ms, 400 ms, 600 ms}
  - Data rate {256 kpbs, 512 kpbs, 1 Mbps}
  - BER {10^-7, 10^-6, 10^-5}
- Type of benchmark: websites {344K, 784K, 2.3M}, PLT
- Comparison with TCP
  - without PEP
  - default TCP settings (MTU 1500, IW 10), TLS1.2, HTTP/{1.1, 2}

## Google QUIC performance over a public SATCOM access
- 2019-02
- Ludovic Thomas, Emmanuel Dubois, Nicolas Kuhn, Emmanuel Lochin
- https://doi.org/10.1002/sat.1301
  - Related IETF presentation: https://datatracker.ietf.org/doc/slides-103-maprg-quic-and-satcom-nicolas-kuhn/
- QUIC version: gQUIC Q039
  - Client: Google Chrome 67
  - Server: Public Google server (404 page & some image)
  - Parameters/Features: BBR, 0-RTT, IW=32
- Real satellite link
  - RTT 750ms
  - Data rate 25/5 Mbps
- Type of benchmark: website (11k), file (5.3M)
- Comparison with TCP
  - with PEP
  - TLS1.2, HTTP/2 ("ChromeNoQuic")
  - TFO

## Satellite Internet Performance Measurements
- 2019-03
- Joerg Deutschmann, Kai-Steffen Hielscher, Reinhard German
- https://doi.org/10.1109/NetSys.2019.8854494
  - Related IETF presentation: https://datatracker.ietf.org/doc/slides-104-maprg-satellite-internet-performance-measurements-jorg-deutschmann/
- QUIC version: gQUIC Q043
  - Client: Google Chrome 69
  - Server: Chromium QUIC, quic-go
  - Parameters/Features: unspecified/default
- Real satellite links (3 different operators)
  - varying RTTs
  - Data rate 20/2 Mbps, 30/2 Mbps, 15/3 Mbps
- Type of benchmark: websites {1.4M, 10M}
- Comparison with TCP
  - with PEP, without PEP using OpenVPN
  - TCP settings (CUBIC, SACK, Window scaling, IW=10, no ECN), TLS1.2, HTTP/{1.1, 2}

## Measuring QUIC Dynamics over a High Delay Path
- Gorry Fairhurst, Ana Custura, Tom Jones
- IETF105 MAPRG https://datatracker.ietf.org/meeting/105/materials/slides-105-maprg-measuring-quic-dynamics-over-a-high-delay-path-01
- QUIC client and server: quicly v20 (draft-20)
  - Parameters/Features: Reno, IW=10, MSS=1460
- Real satellite link
  - varying RTT, RTT > 550 ms
  - Data rate (average) 8.5/1.4 Mbit/s
- Type of benchmark: files {100k, 1M}
- Comparison with TCP
  - with PEP, without PEP using OpenVPN
  - TCP settings (CUBIC, SACK, Window scaling, IW=20/10, MSS=1460/1358), TLS{1.2, 1.3}


## TO BE CONTINUED
