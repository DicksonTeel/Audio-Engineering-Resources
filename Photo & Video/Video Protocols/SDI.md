Serial digital interface (SDI) is a family of digital video interfaces first standardized by SMPTE (The Society of Motion Picture and Television Engineers) in 1989. For example, ITU-R BT.656 and SMPTE 259M define digital video interfaces used for broadcast-grade video. A related standard, known as high-definition serial digital interface (HD-SDI), is standardized in SMPTE 292M; this provides a nominal data rate of 1.485 Gbit/s.

Additional SDI standards have been introduced to support increasing video resolutions (HD, UHD and beyond), frame rates, stereoscopic (3D) video, and color depth. Dual link HD-SDI consists of a pair of SMPTE 292M links, standardized by SMPTE 372M in 1998; this provides a nominal 2.970 Gbit/s interface used in applications (such as digital cinema or HDTV 1080P) that require greater fidelity and resolution than standard HDTV can provide. 3G-SDI (standardized in SMPTE 424M) consists of a single 2.970 Gbit/s serial link that allows replacing dual link HD-SDI. 6G-SDI and 12G-SDI standards were published on March 19, 2015.

These standards are used for transmission of uncompressed, unencrypted digital video signals (optionally including embedded audio and time code) within television facilities; they can also be used for packetized data. SDI is used to connect together different pieces of equipment such as recorders, monitors, PCs and vision mixers. Coaxial variants of the specification range in length but are typically less than 300 meters (980 ft). Fiber optic variants of the specification such as 297M allow for long-distance transmission limited only by maximum fiber length or repeaters. SDI and HD-SDI are usually available only in professional video equipment because various licensing agreements restrict the use of unencrypted digital interfaces, such as SDI, prohibiting their use in consumer equipment. Several professional video and HD-video capable DSLR cameras and all uncompressed video capable consumer cameras use the HDMI interface, often called clean HDMI. There are various mod kits for existing DVD players and other devices, which allow a user to add a serial digital interface to these devices.

---

The various serial digital interface standards all use (one or more) coaxial cables with BNC connectors, with a nominal impedance of 75 ohms. This is the same type of cable used in analog video setups, which potentially makes for easier upgrades (though higher quality cables may be necessary for long runs at the higher bitrates). The specified signal amplitude at the source is 800 mV (±10%) peak-to-peak; far lower voltages may be measured at the receiver owing to attenuation. Using equalization at the receiver, it is possible to send 270 Mbit/s SDI over 300 meters (980 ft) without use of repeaters, but shorter lengths are preferred. The HD bitrates have a shorter maximum run length, typically 100 meters (330 ft).

Uncompressed digital component signals are transmitted. Data is encoded in NRZI format, and a linear feedback shift register is used to scramble the data to reduce the likelihood that long strings of zeroes or ones will be present on the interface. The interface is self-synchronizing and self-clocking. Framing is done by detection of a special synchronization pattern, which appears on the (unscrambled) serial digital signal to be a sequence of ten ones followed by twenty zeroes (twenty ones followed by forty zeroes in HD); this bit pattern is not legal anywhere else within the data payload.

Several bit rates are used in serial digital video signal:

- For standard definition applications, as defined by SMPTE 259M, the possible bit rates are 270 Mbit/s, 360 Mbit/s, 143 Mbit/s, and 177 Mbit/s. 270 Mbit/s is by far the most commonly used; though the 360 Mbit/s interface (used for widescreen standard definition) is sometimes encountered. The 143 and 177 Mbit/s interfaces were intended for transmission of composite-encoded (NTSC or PAL) video digitally, and are now considered obsolete.
- For enhanced definition applications (mainly 525P), there are several 540 Mbit/s interfaces defined, as well as an interface standard for a dual-link 270 Mbit/s interface. These are rarely encountered.
- For HDTV applications, the serial digital interface is defined by SMPTE 292M. Two bit rates are defined, 1.485 Gbit/s, and 1.485/1.001 Gbit/s. The factor of 1/1.001 is provided to allow SMPTE 292M to support video formats with frame rates of 59.94 Hz, 29.97 Hz, and 23.98 Hz, in order to be compatible with existing NTSC systems. The 1.485 Gbit/s version of the standard supports other frame rates in widespread use, including 60 Hz, 50 Hz, 30 Hz, 25 Hz, and 24 Hz. It is common to collectively refer to both standards as using a nominal bit rate of 1.5 Gbit/s.
- For very high-definition applications, requiring greater resolution, frame rate, or color fidelity than the HD-SDI interface can provide, the SMPTE 372M standard defines the dual link interface. As the name suggests, this interface consists of two SMPTE 292M interconnects operating in parallel. In particular, the dual link interface supports 10-bit, 4:2:2, 1080P formats at frame rates of 60 Hz, 59.94 Hz, and 50 Hz, as well as 12-bit color depth, RGB encoding, and 4:4:4 colour sampling.
- A nominal 3 Gbit/s interface (more accurately, 2.97 Gbit/s, but commonly referred to as "3 gig") was standardized by SMPTE as 424M in 2006. Revised in 2012 as SMPTE ST 424:2012, it supports all of the features supported by the dual 1.485 Gbit/s interface, but requires only one cable rather than two.

SMPTE 297-2006 defines an optical fiber system for transmitting bit-serial digital signals It is intended for transmitting SMPTE ST 259 signals (143 through 360 Mbit/s), SMPTE ST 344 signals (540 Mbit/s), SMPTE ST 292-1/-2 signals (1.485 Gbit/s and 1.485/1.001 Gbit/s) and SMPTE ST 424 signals (2.970 Gbit/s and 2.970/1.001 Gbit/s). In addition to optical specification, ST 297 also mandates laser safety testing and that all optical interfaces are labelled to indicate safety compliance, application and interoperability.

An 8-bit parallel digital interface is defined by ITU-R Rec. 601; this is obsolete (however, many clauses in the various standards accommodate the possibility of an 8-bit interface).

---

In SD and ED applications, the serial data format is defined to 10 bits wide, whereas in HD applications, it is 20 bits wide, divided into two parallel 10-bit datastreams (known as Y and C). The SD datastream is arranged like this:

```
Cb Y Cr Y' Cb Y Cr Y'
```
whereas the HD datastreams are arranged like this:

```
Y
Y Y' Y Y' Y Y' Y Y'
C
Cb Cr Cb Cr Cb Cr Cb Cr
```
For all serial digital interfaces (excluding the obsolete composite encodings), the native color encoding is 4:2:2 YCbCr format. The luminance channel (Y) is encoded at full bandwidth (13.5 MHz in 270 Mbit/s SD, ~75 MHz in HD), and the two chrominance channels (Cb and Cr) are subsampled horizontally, and encoded at half bandwidth (6.75 MHz or 37.5 MHz). The Y, Cr, and Cb samples are co-sited (acquired at the same instance in time), and the Y' sample is acquired at the time halfway between two adjacent Y samples.

In the above, Y refers to luminance samples, and C to chrominance samples. Cr and Cb further refer to the red and blue "color difference" channels; see Component Video for more information. This section only discusses the native color encoding of SDI; other color encodings are possible by treating the interface as a generic 10-bit data channel. The use of other colorimetry encodings, and the conversion to and from RGB colorspace, is discussed below.

Video payload (as well as ancillary data payload) may use any 10-bit word in the range 4 to 1,019 (00416 to 3FB16) inclusive; the values 0–3 and 1,020–1,023 (3FC16–3FF16) are reserved and may not appear anywhere in the payload. These reserved words have two purposes; they are used both for Synchronization packets and for Ancillary data headers.

A synchronization packet (commonly known as the timing reference signal or TRS) occurs immediately before the first active sample on every line, and immediately after the last active sample (and before the start of the horizontal blanking region). The synchronization packet consists of four 10-bit words, the first three words are always the same—0x3FF, 0, 0; the fourth consists of 3 flag bits, along with an error correcting code. As a result, there are 8 different synchronization packets possible.

In the HD-SDI and dual link interfaces, synchronization packets must occur simultaneously in both the Y and C datastreams. (Some delay between the two cables in a dual link interface is permissible; equipment which supports dual link is expected to buffer the leading link in order to allow the other link to catch up). In SD-SDI and enhanced definition interfaces, there is only one datastream, and thus only one synchronization packet at a time. Other than the issue of how many packets appear, their format is the same in all versions of the serial-digital interface.

The flags bits found in the fourth word (commonly known as the XYZ word) are known as H, F, and V. The H bit indicates the start of horizontal blank; and synchronization bits immediately preceding the horizontal blanking region must have H set to one. Such packets are commonly referred to as End of Active Video, or EAV packets. Likewise, the packet appearing immediately before the start of the active video has H set to 0; this is the Start of Active Video or SAV packet.

Likewise, the V bit is used to indicate the start of the vertical blanking region; an EAV packet with V=1 indicates the following line (lines are deemed to start at EAV) is part of the vertical interval, an EAV packet with V=0 indicates the following line is part of the active picture.

The F bit is used in interlaced and segmented-frame formats to indicate whether the line comes from the first or second field (or segment). In progressive scan formats, the F bit is always set to zero.

In the high definition serial digital interface (and in dual-link HD), additional check words are provided to increase the robustness of the interface. In these formats, the four samples immediately following the EAV packets (but not the SAV packets) contain a cyclic redundancy check field, and a line count indicator. The CRC field provides a CRC of the preceding line (CRCs are computed independently for the Y and C streams), and can be used to detect bit errors in the interface. The line count field indicates the line number of the current line.

The CRC and line counts are not provided in the SD and ED interfaces. Instead, a special ancillary data packet known as an EDH packet may be optionally used to provide a CRC check on the data.

Each sample within a given datastream is assigned a unique line and sample number. In all formats, the first sample immediately following the SAV packet is assigned sample number 0; the next sample is sample 1; all the way up to the XYZ word in the following SAV packet. In SD interfaces, where there is only one datastream, the 0th sample is a Cb sample; the 1st sample a Y sample, the 2nd sample a Cr sample, and the third sample is the Y' sample; the pattern repeats from there. In HD interfaces, each datastream has its own sample numbering—so the 0th sample of the Y datastream is the Y sample, the next sample the Y' sample, etc. Likewise, the first sample in the C datastream is Cb, followed by Cr, followed by Cb again.

Lines are numbered sequentially, starting from 1, up to the number of lines per frame of the indicated format (typically 525, 625, 750, or 1125 (Sony HDVS)). Determination of line 1 is somewhat arbitrary; however it is unambiguously specified by the relevant standards. In 525-line systems, the first line of vertical blank is line 1, whereas in other interlaced systems (625 and 1125-line), the first line after the F bit transitions to zero is line 1.

Note that lines are deemed to start at EAV, whereas sample zero is the sample following SAV. This produces the somewhat confusing result that the first sample in a given line of 1080i video is sample number 1920 (the first EAV sample in that format), and the line ends at the following sample 1919 (the last active sample in that format). Note that this behavior differs somewhat from analog video interfaces, where the line transition is deemed to occur at the sync pulse, which occurs roughly halfway through the horizontal blanking region.

Link numbering is only an issue in multi-link interfaces. The first link (the primary link), is assigned a link number of 1, subsequent links are assigned increasing link numbers; so the second (secondary) link in a dual-link system is link 2. The link number of a given interface is indicated by a VPID packet located in the vertical ancillary data space.

Note that the data layout in dual link is designed so that the primary link can be fed into a single-link interface, and still produce usable (though somewhat degraded) video. The secondary link generally contains things like additional LSBs (in 12-bit formats), non-cosited samples in 4:4:4 sampled video (so that the primary link is still valid 4:2:2), and alpha or data channels. If the second link of a 1080P dual link configuration is absent, the first link still contains a valid 1080i signal.

In the case of 1080p60, 59.94, or 50 Hz video over a dual link; each link contains a valid 1080i signal at the same field rate. The first link contains the 1st, 3rd, and 5th lines of odd fields and the 2nd, 4th, 6th, etc. lines of even fields, and the second link contains the even lines on the odd fields, and the odd lines on the even fields. When the two links are combined, the result is a progressive-scan picture at the higher frame rate.

---

Like SMPTE 259M, SMPTE 292M supports the SMPTE 291M standard for ancillary data. Ancillary data is provided as a standardized transport for non-video payload within a serial digital signal; it is used for things such as embedded audio, closed captions, timecode, and other sorts of metadata. Ancillary data is indicated by a 3-word packet consisting of 0, 3FF, 3FF (the opposite of the synchronization packet header), followed by a two-word identification code, a data count word (indicating 0–255 words of payload), the actual payload, and a one-word checksum. Other than in their use in the header, the codes prohibited to video payload are also prohibited to ancillary data payload.

Specific applications of ancillary data include embedded audio, EDH, VPID and SDTI.

In dual link applications; ancillary data is mostly found on the primary link; the secondary link is to be used for ancillary data only if there is no room on the primary link. One exception to this rule is the VPID packet; both links must have a valid VPID packet present.

Both the HD and SD serial interfaces provide for 16 channels of embedded audio. The two interfaces use different audio encapsulation methods — SD uses the SMPTE 272M standard, whereas HD uses the SMPTE 299M standard. In either case, an SDI signal may contain up to sixteen audio channels (8 pairs) embedded 48 kHz, 24-bit audio channels along with the video. Typically, 48 kHz, 24-bit (20-bit in SD, but extendable to 24 bit) PCM audio is stored, in a manner directly compatible with the AES3 digital audio interface. These are placed in the (horizontal) blanking periods, when the SDI signal carries nothing useful, since the receiver generates its own blanking signals from the TRS.

In dual-link applications, 32 channels of audio are available, as each link may carry 16 channels.

SMPTE ST 299-2:2010 extends the 3G SDI interface to be able to transmit 32 audio channels (16 pairs) on a single link.

As the standard definition interface carries no checksum, CRC, or other data integrity check, an EDH (Error Detection and Handling) packet may be optionally placed in the vertical interval of the video signal. This packet includes CRC values for both the active picture, and the entire field (excluding those lines at which switching may occur, and which should contain no useful data); equipment can compute their own CRC and compare it with the received CRC in order to detect errors.

EDH is typically only used with the standard definition interface; the presence of CRC words in the HD interface make EDH packets unnecessary.

VPID (or video payload identifier) packets are increasingly used to describe the video format. In early versions of the serial digital interface, it was always possible to uniquely determine the video format by counting the number of lines and samples between H and V transitions in the TRS. With the introduction of dual link interfaces, and segmented-frame standards, this is no longer possible; thus the VPID standard (defined by SMPTE 352M) provides a way to uniquely and unambiguously identify the format of the video payload.

---

The active portion of the video signal is defined to be those samples which follow an SAV packet, and precede the next EAV packet; where the corresponding EAV and SAV packets have the V bit set to zero. It is in the active portion that the actual image information is stored.

Several color encodings are possible in the serial digital interface. The default (and most common case) is 10-bit linearly sampled video data encoded as 4:2:2 YCbCr. (YCbCr is a digital representation of the YPbPr colorspace). Samples of video are stored as described above. Data words correspond to signal levels of the respective video components, as follows:

- The luma (Y) channel is defined such that a signal level of 0 mV is assigned the codeword 64 (40 hex), and 700 millivolts (full scale) is assigned the codeword 940 (3AC hex) .
- For the chroma channels, 0 mV is assigned the code word 512 (200 hex), −350 mV is assigned a code word of 64 (40 hex), and +350 mV is assigned a code word of 960 (3C0 hex).

Note that the scaling of the luma and chroma channels is not identical. The minimum and maximum of these ranges represent the preferred signal limits, though the video payload may venture outside these ranges (providing that the reserved code words of 0–3 and 1020–1023 are never used for video payload). In addition, the corresponding analog signal may have excursions further outside of this range.

As YPbPr (and YCbCr) are both derived from the RGB colorspace, a means of converting is required. There are three colorimetries typically used with digital video:

SD and ED applications typically use a colorimetry matrix specified in ITU-R Rec. 601.
Most HD, dual link, and 3 Gbit/s applications use a different matrix, specified in ITU-R Rec. 709.
The 1035-line MUSE HD standards specified by SMPTE 260M (primarily used in Japan and now largely considered obsolete), used a colorimetry matrix specified by SMPTE 240M. This colorimetry is nowadays rarely used, as the 1035-line formats have been superseded by 1080-line formats.

The dual-link and 3 Gbit/s interfaces additionally support other color encodings besides 4:2:2 YCbCr, namely:

4:2:2 and 4:4:4 YCbCr, with an optional alpha (used for linear keying, a.k.a. alpha compositing) or data (used for non-video payload) channel
4:4:4 RGB, also with an optional alpha or data channel
4:2:2 YCbCr, 4:4:4 YCbCr, and 4:4:4 RGB, with 12 bits of color information per sample, rather than 10. Note that the interface itself is still 10 bit; the additional 2 bits per channel are multiplexed into an additional 10-bit channel on the second link.
If an RGB encoding is used, the three primaries are all encoded in the same fashion as the Y channel; a value of 64 (40 hex) corresponds to 0 mV, and 940 (3AC hex) corresponds to 700 mV.

12-bit applications are scaled in a similar fashion to their 10-bit counterparts; the additional two bits are considered to be LSBs.

For portions of the vertical and horizontal blanking regions which are not used for ancillary data, it is recommended that the luma samples be assigned the code word 64 (40 hex), and the chroma samples be assigned 512 (200 hex); both of which correspond to 0 mV. It is permissible to encode analog vertical interval information (such as vertical interval timecode or vertical interval test signals) without breaking the interface, but such usage is nonstandard (and ancillary data is the preferred means for transmitting metadata). Conversion of analog sync and burst signals into digital, however, is not recommended—and neither is necessary in the digital interface.

Different picture formats have different requirements for digital blanking, for example all so called 1080 line HD formats have 1080 active lines, but 1125 total lines, with the remainder being vertical blanking.

---

The various versions of the serial digital interface support numerous video formats:

- The 270 Mbit/s interface supports 525-line, interlaced video at a 59.94 Hz field rate (29.97 Hz frame rate), and 625-line, 50 Hz interlaced video. These formats are highly compatible with NTSC and PAL-B/G/D/K/I systems respectively; and the terms NTSC and PAL are often (incorrectly) used to refer to these formats. (PAL is a composite color encoding scheme, and the term does not define the line-standard, though it is most usually encountered with 625i) while the serial digital interface— other than the obsolete 143 Mbit/s and 177 Mbit/s forms- is a component standard.
- The 360 Mbit/s interface supports 525i and 625i widescreen. It can also be used to support 525p, if 4:2:0 sampling is used.
- The various 540 Mbit/s interfaces support 525p and 625p formats.
- The nominal 1.49 Gbit/s interfaces support most high-definition video formats. Supported formats include 1080/60i, 1080/59.94i, 1080/50i, 1080/30p, 1080/29.97p, 1080/25p, 1080/24p, 1080/23.98p, 720/60p, 720/59.94p, and 720/50p. In addition, there are several 1035i formats (an obsolete Japanese television standard), half-bandwidth 720p standards such as 720/24p (used in some film conversion applications, and unusual because it has an odd number of samples per line), and various 1080psf (progressive, segmented frame) formats. Progressive Segmented frames formats appear as interlace video but contain video which is progressively scanned. This is done to support analog monitors and televisions, many of which are incapable of locking to low field rates such as 30 Hz and 24 Hz.
- The 2.97 Gbit/s dual link HD interface supports 1080/60p, 1080/59.94p, and 1080/50p, as well as 4:4:4 encoding, greater color depth, RGB encoding, alpha channels, and nonstandard resolutions (often encountered in computer graphics or digital cinema).
- A quad link interface of HD-SDI supports UHDTV-1 resolution 2160/60p