# Code snippet

```
In [51]: f='024204002755_INSP_BONE_L1_ECLIPSE/bone_0.dcm'
In [52]: import pydicom; ds=pydicom.dcmread(f)
```

# Output
```
Out[52]: ds

(0008, 0005) Specific Character Set              CS: 'ISO_IR 100'
(0008, 0008) Image Type                          CS: ['ORIGINAL', 'PRIMARY', 'AXIAL', 'CT_SOM5 SPI']
(0008, 0016) SOP Class UID                       UI: CT Image Storage
(0008, 0018) SOP Instance UID                    UI: 1.3.12.2.1107.5.1.4.57132.30000006120609190092100005347
(0008, 0020) Study Date                          DA: '20061206'
(0008, 0021) Series Date                         DA: '20061206'
(0008, 0022) Acquisition Date                    DA: '20061206'
(0008, 0023) Content Date                        DA: '20061206'
(0008, 0030) Study Time                          TM: '140832.359000'
(0008, 0031) Series Time                         TM: '141203.921000'
(0008, 0032) Acquisition Time                    TM: '141120.453695'
(0008, 0033) Content Time                        TM: '141120.453695'
(0008, 0050) Accession Number                    SH: 'SCO104960'
(0008, 0060) Modality                            CS: 'CT'
(0008, 0070) Manufacturer                        LO: 'SIEMENS'
(0008, 0080) Institution Name                    LO: 'RDG klinika FN Na Bulovce v Praze'
(0008, 0081) Institution Address                 ST: 'Street\nCity/2822378/\nDistrict\nCountry'
(0008, 0090) Referring Physician's Name          PN: 'KPHCH'
(0008, 1010) Station Name                        SH: 'CT57132'
(0008, 1030) Study Description                   LO: 'Thorax^HRUDNIK_STUDIE (Adult)'
(0008, 103e) Series Description                  LO: 'Thorax  1.0  B60f'
(0008, 1050) Performing Physician's Name         PN: 'PAT'
(0008, 1070) Operators' Name                     PN: 'LIB'
(0008, 1090) Manufacturer's Model Name           LO: 'Sensation 40'
(0008, 1140)  Referenced Image Sequence   1 item(s) ----
   (0008, 0000) Group Length                        UL: 98
   (0008, 1150) Referenced SOP Class UID            UI: CT Image Storage
   (0008, 1155) Referenced SOP Instance UID         UI: 1.3.12.2.1107.5.1.4.57132.30000006120609062090600001470
   ---------
(0008, 2112)  Source Image Sequence   1 item(s) ----
   (0008, 0000) Group Length                        UL: 92
   (0008, 1150) Referenced SOP Class UID            UI: 1.3.12.2.1107.5.9.1
   (0008, 1155) Referenced SOP Instance UID         UI: 1.3.12.2.1107.5.1.4.57132.30000006120609062090600001472
   ---------
(0009, 0000) Private Creator                     UN: b'\x1c\x00\x00\x00'
(0009, 0010) Private tag data                    LO: 'SIEMENS CT VA1 DUMMY'
(0010, 0000) Group Length                        UL: 70
(0010, 0010) Patient's Name                      PN: 'XXXX'
(0010, 0020) Patient ID                          LO: 'XXXX'
(0010, 0030) Patient's Birth Date                DA: 'XXXX'
(0010, 0040) Patient's Sex                       CS: 'M'
(0010, 1010) Patient's Age                       AS: '001D'
(0018, 0000) Group Length                        UL: 356
(0018, 0015) Body Part Examined                  CS: 'CHEST'
(0018, 0050) Slice Thickness                     DS: "1.000000"
(0018, 0060) KVP                                 DS: "120.000000"
(0018, 0090) Data Collection Diameter            DS: "500.000000"
(0018, 1000) Device Serial Number                LO: '57132'
(0018, 1020) Software Version(s)                 LO: 'syngo CT 2006A'
(0018, 1030) Protocol Name                       LO: 'HRUDNIK_STUDIE'
(0018, 1100) Reconstruction Diameter             DS: "325.000000"
(0018, 1110) Distance Source to Detector         DS: "1040.000000"
(0018, 1111) Distance Source to Patient          DS: "570.000000"
(0018, 1120) Gantry/Detector Tilt                DS: "0.000000"
(0018, 1130) Table Height                        DS: "160.000000"
(0018, 1140) Rotation Direction                  CS: 'CW'
(0018, 1150) Exposure Time                       IS: "500"
(0018, 1151) X-Ray Tube Current                  IS: "126"
(0018, 1152) Exposure                            IS: "45"
(0018, 1160) Filter Type                         SH: '0'
(0018, 1170) Generator Power                     IS: "13"
(0018, 1190) Focal Spot(s)                       DS: "1.200000"
(0018, 1200) Date of Last Calibration            DA: '20061206'
(0018, 1201) Time of Last Calibration            TM: '100949.000000'
(0018, 1210) Convolution Kernel                  SH: 'B60f'
(0018, 5100) Patient Position                    CS: 'HFS'
(0019, 0000) Private Creator                     UN: b'(\x00\x00\x00'
(0019, 0010) Private tag data                    LO: 'SIEMENS CT VA0  COAD'
(0019, 10b0) [Feed per Rotation]                 UN: b'16.8'
(0020, 0000) Group Length                        UL: 370
(0020, 000d) Study Instance UID                  UI: 1.3.12.2.1107.5.1.4.57132.30000006120609131090600000049
(0020, 000e) Series Instance UID                 UI: 1.3.12.2.1107.5.1.4.57132.30000006120609190092100005346
(0020, 0010) Study ID                            SH: '1'
(0020, 0011) Series Number                       IS: "4"
(0020, 0012) Acquisition Number                  IS: "2"
(0020, 0013) Instance Number                     IS: "1"
(0020, 0032) Image Position (Patient)            DS: ['-149.182617', '-322.182617', '17.000000']
(0020, 0037) Image Orientation (Patient)         DS: ['1.000000', '0.000000', '0.000000', '0.000000', '1.000000', '0.000000']
(0020, 0052) Frame of Reference UID              UI: 1.3.12.2.1107.5.1.4.57132.30000006120609062090600001469
(0020, 1040) Position Reference Indicator        LO: ''
(0020, 1041) Slice Location                      DS: "17.000000"
(0020, 4000) Image Comments                      LT: ''
(0021, 0000) Private Creator                     UN: b' \x00\x00\x00'
(0021, 0010) Private tag data                    LO: 'SIEMENS MED'
(0021, 1011) [Target]                            UN: b'13\\0'
(0028, 0000) Group Length                        UL: 268
(0028, 0002) Samples per Pixel                   US: 1
(0028, 0004) Photometric Interpretation          CS: 'MONOCHROME2'
(0028, 0010) Rows                                US: 512
(0028, 0011) Columns                             US: 512
(0028, 0030) Pixel Spacing                       DS: ['0.634766', '0.634766']
(0028, 0034) Pixel Aspect Ratio                  IS: ['1', '1']
(0028, 0100) Bits Allocated                      US: 16
(0028, 0101) Bits Stored                         US: 12
(0028, 0102) High Bit                            US: 11
(0028, 0103) Pixel Representation                US: 0
(0028, 0106) Smallest Image Pixel Value          US: 0
(0028, 0107) Largest Image Pixel Value           US: 4074
(0028, 1050) Window Center                       DS: ['-600.000000', '50.000000']
(0028, 1051) Window Width                        DS: ['1200.000000', '350.000000']
(0028, 1052) Rescale Intercept                   DS: "-1024.000000"
(0028, 1053) Rescale Slope                       DS: "1.000000"
(0028, 1055) Window Center & Width Explanation   LO: ['WINDOW1', 'WINDOW2']
(0029, 0000) Private Creator                     UN: b'\x82\x03\x00\x00'
(0029, 0010) Private tag data                    LO: 'SIEMENS CSA HEADER'
(0029, 0011) Private tag data                    LO: 'SIEMENS MEDCOM HEADER'
(0029, 1008) [CSA Image Header Type]             UN: b'SOM 5 '
(0029, 1009) [CSA Image Header Version]          UN: b'VA10A 971201'
(0029, 1010) [CSA Image Header Info]             UN: b'\x00\x00\x04\x00LT\x08\x003\x004\x006\x009\x00\x00\x00\x05\x00FD\x08\x00\x00\x00\x00\x00\x00\xf6t@\x00\x00\x06\x00FD\x08\x00\xa2\xf7|\x83\xe5\x9e\x12@\x00\x00\x07\x00SL\x04\x00\xbb\x03\x00\x00\x00\x00\x08\x00SL\x04\x00\xc8\x00\x00\x00\x00\x00\x0c\x00FD\x08\x00\xcd\xcc\xcc\xcc\xcc\xcc0@\x00\x00\r\x00SL\x04\x00\x01\x00\x00\x00\x00\x00\x13\x00SL\x04\x00Q\x01\x00\x00\x00\x00\x14\x00SL\x04\x00\x00\x00\x00\x00\x00\x00\x16\x00SL\x04\x002\x00\x00\x00\x00\x00\x18\x00SL\x04\x00\xa0\x02\x00\x00\x00\x00\x1a\x00SL\x04\x00:\xc2\x00\x00\x00\x00\x1d\x00LT\n\x00C\x00H\x00E\x00S\x00T\x00\x00\x00\x1e\x00FD\x08\x00\x00\x00\x00\x00\x00Pt@\x00\x00\x1f\x00FD\x08\x00\x00\x00\x00\x00\x00\x00*@\x00\x00 \x00FD\x08\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00!\x00SL\x04\x00\x01\x00\x00\x00\x00\x00"\x00SL\x04\x00\x03\x00\x00\x00\x00\x00%\x00SL\x04\x00\x08\x00\x00\x00\x00\x00\'\x00FD\x08\x00\x00\x00\x00\x00\x00\x00N@\x00\x00(\x00SL\x04\x00d\x01\x00\x00\x00\x00)\x00SL\x04\x00\x00\x00\x00\x00\x00\x00+\x00LT\x12\x004\x001\x002\x003\x001\x000\x006\x003\x001\x00\x00\x00,\x00SL\x04\x00&\x00\x00\x00\x00\x00-\x00SL\x04\x00\x00\x00\x00\x00\x00\x00/\x00FD\x08\x00333333\xe3?\x00\x000\x00LT\x08\x00P\x003\x000\x00G\x00\x00\x003\x00SL\x04\x00\x05\x00\x00\x00\x00\x005\x00SL\x04\x00\x00\x00\x00\x00\x00\x006\x00CS\x02\x00T \x00\x007\x00SL\x04\x00\x13\x03\x00\x00\x00\x008\x00SL\x04\x00+\x00\x00\x00\x00\x009\x00SL\x04\x00\x14\x00\x00\x00\x00\x00:\x00FD\x08\x00ffffff\xf6?\x00\x00;\x00SL\x04\x00\x01\x00\x00\x00\x00\x00<\x00SL\x04\x00\x02\x00\x00\x00\x00\x00=\x00FD\x08\x00\x00\x00\x00\x00\x00Pt@\x00\x00>\x00SL\x04\x00\x00\x00\x00\x00\x00\x00\x01\x01FD\x08\x00\xcd\xcc\xcc\xcc\xcc\xcc\x1b\xc0\x00\x00\x02\x01FD\x08\x00\x04\x0eW\xbd\xb2A\xec?\x00\x00\x03\x01FD\x08\x00\xe1z\x14\xaeG\xe1\xca\xbf\x00\x00\x05\x01IS\x06\x00503496\xff\xff\xff\xffCS\n\x00END!      '
(0029, 1131) [PMTF Information 1]                UN: b'4.0.111160728 '
(0029, 1132) [PMTF Information 2]                UN: b'\x00\x00\x08\x00'
(0029, 1133) [PMTF Information 3]                UN: b'\x00\x00\x00\x00'
(0029, 1134) [PMTF Information 4]                UN: b'DB TO DICOM '
(0029, 1140) [Application Header Sequence]       UN: b'\xfe\xff\x00\xe0t\x00\x00\x00)\x00\x10\x00\x16\x00\x00\x00SIEMENS MEDCOM HEADER )\x00A\x10\n\x00\x00\x00SOM 5 TPOS)\x00B\x10\x12\x00\x00\x00SOM 5 NULLPOSITION)\x00C\x10\x0e\x00\x00\x00VB10A 20030626)\x00D\x10\x0c\x00\x00\x00-000008310\x00\x06'
(140d, 0000) Private Creator                     UN: b'\x18\x00\x00\x00'
(140d, 1000) Private tag data                    UN: b'j4\xcd1\x98\x17\xafH\x86\x95\x00\t\x0f\xed\x81\xc5'
(160d, 0000) Private Creator                     UN: b'D\x00\x00\x00'
(160d, 1000) Private tag data                    UN: b'[6\xf2\xe3\xa2\x18oB\x9b\x10\xfb\xd4\xbee\xb9\x9f'
(160d, 1001) Private tag data                    UN: b'CLUT\x00\x00\x00\x00PREH\x01\x00\x00\x00PRES\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
(170d, 0000) Private Creator                     UN: b'\x18\x00\x00\x00'
(170d, 1000) Private tag data                    UN: b'7\xd9\x86\xe5\xc7\xdd\x91B\xb5\x8ci@\xbaz3\xd3'
(7fe0, 0000) Group Length                        UL: 524296
(7fe0, 0010) Pixel Data                          OW: Array of 524288 bytes
```
