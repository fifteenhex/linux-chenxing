# Bach

## Bank address for infinity3/mercury5

[detailed here](https://github.com/fifteenhex/SDK_pulbic/blob/c1436fa7446457e8d6547874d27ee4e34be150cf/Mercury5/proj/sc/driver/hal/mercury/audio/inc/hal_bach.h#L41)

- 0x1f2a0400
- 0x1f2a0600
- 0x1f2a0800
- 0x1f206800

## bank 1 - control/DMA registers

| offset | name                            | 15          | 14            | 13             | 12        | 11          | 10          | 9          | 8          | 7        | 6        | 5            | 4        | 3        | 2        | 1        | 0        |
|--------|---------------------------------|-------------|---------------|----------------|-----------|-------------|-------------|------------|------------|----------|----------|--------------|----------|----------|----------|----------|----------|
| 0x000  | enable ctrl                     |             |               |                |           | bp_adc_hpf2 | bp_adc_hpf1 |            |            |          |          |              |          |          |          |          |          |
| 0x004  | sr0 sel                         | cic_1_sel   | cic_1_sel     |                |           | cic_3_sel   | cic_3_sel   | writer_sel | writer_sel | src1_sel | src1_sel | src1_sel     | src1_sel | src2_sel | src2_sel | src2_sel | src2_sel |
| 0x008  | ???                             |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x00c  | mux0 sel                        |             |               |                |           |             |             |            |            |          |          | mmc1 src sel |          |          |          |          |          |
| 0x010  | mux1 sel                        | adc_hpf_n   | adc_hpf_n     | adc_hpf_n      | adc_hpf_n |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x014  | mix1 sel                        |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x024  | sdm ctrl                        |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x04c  | codec i2s tx ctrl               |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x074  | synth ctrl                      |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x090  | adc dpga cfg1                   |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x094  | adc dpga cfg2                   |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x1d4  | dma test ctrl 5 (sine wave gen) | sine gen en | sine gen left | sine gen right |           |             |             |            |            | gain     | gain     | gain         | gain     | freq     | freq     | freq     | freq     |
|        |                                 |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |

## bank 2 

| offset | name          | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0      |
|--------|---------------|----|----|----|----|----|----|---|---|---|---|---|---|---|---|---|--------|
| 0x01c  | int en        |    |    |    |    |    |    |   |   |   |   |   |   |   |   |   | int en |
| 0x038  | mux3 sel      |    |    |    |    |    |    |   |   |   |   |   |   |   |   |   |        |
| 0x058  | au sys ctrl1  |    |    |    |    |    |    |   |   |   |   |   |   |   |   |   |        |
| 0x074  | dig mic ctrl0 |    |    |    |    |    |    |   |   |   |   |   |   |   |   |   |        |
| 0x078  | dig mic ctrl1 |    |    |    |    |    |    |   |   |   |   |   |   |   |   |   |        |

## bank 3

| offset | name   | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4      | 3      | 2      | 1      | 0      |
|--------|--------|----|----|----|----|----|----|---|---|---|---|---|--------|--------|--------|--------|--------|
| 0x010  |        |    |    |    |    |    |    |   |   |   |   |   | fs_sel | fs_sel | fs_sel | fs_sel | fs_sel |
|        |        |    |    |    |    |    |    |   |   |   |   |   |        |        |        |        |        |
|        |        |    |    |    |    |    |    |   |   |   |   |   |        |        |        |        |        |

## bank 4 - analog

| offset | name         | 15        | 14        | 13        | 12             | 11             | 10            | 9                | 8                | 7              | 6              | 5             | 4             | 3                  | 2                  | 1              | 0              | notes                                 |
|--------|--------------|-----------|-----------|-----------|----------------|----------------|---------------|------------------|------------------|----------------|----------------|---------------|---------------|--------------------|--------------------|----------------|----------------|---------------------------------------|
| 0x000  | analog ctrl0 |           |           |           |                | en msp         | en itest dac  | en dit adc0      | en dac disch     | en ck dac      | en ck dac      | en ck dac     | en ck dac     |                    | en chop adc0       | en byp inmux   | en byp inmux   |                                       |
| 0x004  | analog ctrl1 |           |           |           | en vref sfydch | en vref sfydch | en vref disch | en tst ibias adc | en tst ibias adc | en shrt r adc0 | en shrt l adc0 | en qs ldo dac | en qs ldo adc | en mute mic stg1 r | en mute mic stg1 l | en mute in mux | en mute in mux |                                       |
| 0x008  | analog ctrl2 | en sw tst | en sw tst | en sw tst | en sw tst      | en sw tst      | en sw tst     | en sw tst        | en sw tst        | en sw tst      | en sw tst      | en sw tst     | en sw tst     | en sw tst          | en sw tst          | en sw tst      | en sw tst      |                                       |
| 0x00c  | analog ctrl3 |           |           |           | vref           | vi             | ref_dac       | r0_dac           | mic stg2_l       | mic stg1_l     | ldo dac        | ldo adc       | l0 dac        | inmux              | inmux              | bias dac       | adc0           | power downs, probably 1 to power down |
| 0x010  | analog ctrl4 |           |           |           |                |                |               |                  |                  | rst dac        | rst dac        | rst dac       | rst dac       |                    |                    |                | rst adc0       |                                       |
|        |              |           |           |           |                |                |               |                  |                  |                |                |               |               |                    |                    |                |                |                                       |
|        |              |           |           |           |                |                |               |                  |                  |                |                |               |               |                    |                    |                |                |                                       |

### Register dumps

#### i2m, vendor u-boot

```
Wireless-tag# md.w 0x1f2a0400 0x100
1f2a0400: c1ff 0000 0080 0000 0003 0000 0080 0000    ................
1f2a0410: 0000 0000 8000 0000 0000 0000 0000 0000    ................
1f2a0420: 0000 0000 0200 0000 0000 0000 007d 0000    ............}...
1f2a0430: 0000 0000 0000 0000 3017 0000 0002 0000    .........0......
1f2a0440: 9400 0000 9400 0000 9400 0000 9400 0000    ................
1f2a0450: 8400 0000 d000 0000 9400 0000 9400 0000    ................
1f2a0460: 8400 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0470: 0000 0000 001d 0000 0000 0000 0000 0000    ................
1f2a0480: 0007 0000 0000 0000 0007 0000 0000 0000    ................
1f2a0490: 0007 0000 0000 0000 0007 0000 0000 0000    ................
1f2a04a0: 0000 0000 0000 0000 0007 0000 0000 0000    ................
1f2a04b0: 0007 0000 0000 0000 0007 0000 0000 0000    ................
1f2a04c0: 0007 0000 0000 0000 0007 0000 0000 0000    ................
1f2a04d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a04e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a04f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0500: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0510: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0520: 001f 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0530: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0540: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0550: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0560: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0570: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0580: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0590: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a05a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a05b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a05c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a05d0: 0000 0000 0000 0000 0000 0000 0440 0000    ............@...
1f2a05e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a05f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
```

```
Wireless-tag# md.w 0x1f2a0600 0x100
1f2a0600: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0610: 4000 0000 0100 0000 03e8 0000 0000 0000    .@..............
1f2a0620: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0630: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0640: 38c0 0000 3838 0000 0c04 0000 1c14 0000    .8..88..........
1f2a0650: 0001 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0660: 0000 0000 0000 0000 0000 0000 0202 0000    ................
1f2a0670: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0680: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0690: 0000 0000 1234 0000 5678 0000 0000 0000    ....4...xV......
1f2a06a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a06b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a06c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a06d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a06e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a06f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0700: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0710: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0720: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0730: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0740: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0750: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0760: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0770: 0000 0000 0000 0000 0000 0000 0080 0000    ................
1f2a0780: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0790: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a07a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a07b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a07c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a07d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a07e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a07f0: 0000 0000 0000 0000 0001 0000 0000 0000    ................
```

```
Wireless-tag# md.w 0x1f2a0800 0x100
1f2a0800: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0810: 0000 0000 8000 0000 0000 0000 0000 0000    ................
1f2a0820: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0830: 0000 0000 0000 0000 0000 0000 ffff 0000    ................
1f2a0840: 00f0 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0850: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0860: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0870: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0880: 00f0 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0890: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a08a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a08b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a08c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a08d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a08e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a08f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0900: 0080 0000 0078 0000 0000 0000 0000 0000    ....x...........
1f2a0910: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0920: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0930: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0940: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0950: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0960: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0970: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0980: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0990: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a09a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a09b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a09c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a09d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a09e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a09f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
```

```
Wireless-tag# md.w 0x1f206800 0x100
1f206800: 0204 0000 0000 0000 0080 0000 1fff 0000    ................
1f206810: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206820: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206830: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206840: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206850: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206860: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206870: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206880: 0040 0000 f0f0 0000 0000 0000 0000 0000    @...............
1f206890: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2068a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2068b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2068c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2068d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2068e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2068f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206900: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206910: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206920: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206930: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206940: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206950: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206960: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206970: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206980: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206990: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2069a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2069b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2069c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2069d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2069e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2069f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
```

#### i2m, ido openwrt after boot

```
0x1F206800 - 0x00000204
0x1F206804 - 0x00000000
0x1F206808 - 0x00000080
0x1F20680C - 0x00001FFF
0x1F206810 - 0x00000000
0x1F206814 - 0x00000000
0x1F206818 - 0x00000000
0x1F20681C - 0x00000000
0x1F206820 - 0x00000000
0x1F206824 - 0x00000000
0x1F206828 - 0x00000000
0x1F20682C - 0x00000000
0x1F206830 - 0x00000000
0x1F206834 - 0x00000000
0x1F206838 - 0x00000000
0x1F20683C - 0x00000000
0x1F206840 - 0x00000000
0x1F206844 - 0x00000000
0x1F206848 - 0x00000000
0x1F20684C - 0x00000000
0x1F206850 - 0x00000000
0x1F206854 - 0x00000000
0x1F206858 - 0x00000000
0x1F20685C - 0x00000000
0x1F206860 - 0x00000000
0x1F206864 - 0x00000000
0x1F206868 - 0x00000000
0x1F20686C - 0x00000000
0x1F206870 - 0x00000000
0x1F206874 - 0x00000000
0x1F206878 - 0x00000000
0x1F20687C - 0x00000000
0x1F206880 - 0x000000C0
0x1F206884 - 0x00000F0F
0x1F206888 - 0x00000000
0x1F20688C - 0x00000000
0x1F206890 - 0x00000000
0x1F206894 - 0x00000000
0x1F206898 - 0x00000000
0x1F20689C - 0x00000000
0x1F2068A0 - 0x00000000
0x1F2068A4 - 0x00000000
0x1F2068A8 - 0x00000000
0x1F2068AC - 0x00000000
0x1F2068B0 - 0x00000000
0x1F2068B4 - 0x00000000
0x1F2068B8 - 0x00000000
0x1F2068BC - 0x00000000
0x1F2068C0 - 0x00000000
0x1F2068C4 - 0x00000000
0x1F2068C8 - 0x00000000
0x1F2068CC - 0x00000000
0x1F2068D0 - 0x00000000
0x1F2068D4 - 0x00000000
0x1F2068D8 - 0x00000000
0x1F2068DC - 0x00000000
0x1F2068E0 - 0x00000000
0x1F2068E4 - 0x00000000
0x1F2068E8 - 0x00000000
0x1F2068EC - 0x00000000
0x1F2068F0 - 0x00000000
0x1F2068F4 - 0x00000000
0x1F2068F8 - 0x00000000
0x1F2068FC - 0x00000000
0x1F206900 - 0x00000000
0x1F206904 - 0x00000000
0x1F206908 - 0x00000000
0x1F20690C - 0x00000000
0x1F206910 - 0x00000000
0x1F206914 - 0x00000000
0x1F206918 - 0x00000000
0x1F20691C - 0x00000000
0x1F206920 - 0x00000000
0x1F206924 - 0x00000000
0x1F206928 - 0x00000000
0x1F20692C - 0x00000000
0x1F206930 - 0x00000000
0x1F206934 - 0x00000000
0x1F206938 - 0x00000000
0x1F20693C - 0x00000000
0x1F206940 - 0x00000000
0x1F206944 - 0x00000000
0x1F206948 - 0x00000000
0x1F20694C - 0x00000000
0x1F206950 - 0x00000000
0x1F206954 - 0x00000000
0x1F206958 - 0x00000000
0x1F20695C - 0x00000000
0x1F206960 - 0x00000000
0x1F206964 - 0x00000000
0x1F206968 - 0x00000000
0x1F20696C - 0x00000000
0x1F206970 - 0x00000000
0x1F206974 - 0x00000000
0x1F206978 - 0x00000000
0x1F20697C - 0x00000000
0x1F206980 - 0x00000000
0x1F206984 - 0x00000000
0x1F206988 - 0x00000000
0x1F20698C - 0x00000000
0x1F206990 - 0x00000000
0x1F206994 - 0x00000000
0x1F206998 - 0x00000000
0x1F20699C - 0x00000000
0x1F2069A0 - 0x00000000
0x1F2069A4 - 0x00000000
0x1F2069A8 - 0x00000000
0x1F2069AC - 0x00000000
0x1F2069B0 - 0x00000000
0x1F2069B4 - 0x00000000
0x1F2069B8 - 0x00000000
0x1F2069BC - 0x00000000
0x1F2069C0 - 0x00000000
0x1F2069C4 - 0x00000000
0x1F2069C8 - 0x00000000
0x1F2069CC - 0x00000000
0x1F2069D0 - 0x00000000
0x1F2069D4 - 0x00000000
0x1F2069D8 - 0x00000000
0x1F2069DC - 0x00000000
0x1F2069E0 - 0x00000000
0x1F2069E4 - 0x00000000
0x1F2069E8 - 0x00000000
0x1F2069EC - 0x00000000
0x1F2069F0 - 0x00000000
0x1F2069F4 - 0x00000000
0x1F2069F8 - 0x00000000
0x1F2069FC - 0x00000000
root@OpenWrt:/# 

```

0x80 and 0x84 are constantly changing:

```
0x1F206880 - 0x00000C80
0x1F206884 - 0x0000F0F0
```

```
0x1F206880 - 0x00000000
0x1F206884 - 0x0000F0F0
```

```
0x1F206880 - 0x00000080
0x1F206884 - 0x00004F0F
```

### i3 - our u-boot

```
md.w 0x1f2a0400 0x100
1f2a0400: c1ff 0000 0080 0000 0003 0000 0080 0000    ................
1f2a0410: 0000 0000 8000 0000 0000 0000 0000 0000    ................
1f2a0420: 0000 0000 0200 0000 0000 0000 007d 0000    ............}...
1f2a0430: 0000 0000 0000 0000 3017 0000 0002 0000    .........0......
1f2a0440: 9400 0000 9400 0000 9400 0000 9400 0000    ................
1f2a0450: 8400 0000 d000 0000 9400 0000 9400 0000    ................
1f2a0460: 8400 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0470: 0000 0000 001d 0000 0000 0000 0000 0000    ................
1f2a0480: 0007 0000 0000 0000 0007 0000 0000 0000    ................
1f2a0490: 0007 0000 0000 0000 0007 0000 0000 0000    ................
1f2a04a0: 0000 0000 0000 0000 0007 0000 0000 0000    ................
1f2a04b0: 0007 0000 0000 0000 0007 0000 0000 0000    ................
1f2a04c0: 0007 0000 0000 0000 0007 0000 0000 0000    ................
1f2a04d0: 0000 0000 0000 0000 0000 0000 03ff 0000    ................
1f2a04e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a04f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0500: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0510: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0520: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0530: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0540: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0550: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0560: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0570: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0580: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0590: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a05a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a05b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a05c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a05d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a05e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a05f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
```

```
=> md.w 0x1f2a0600 0x100
1f2a0600: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0610: 4000 0000 0100 0000 03e8 0000 0000 0000    .@..............
1f2a0620: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0630: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0640: 38c0 0000 3838 0000 0c04 0000 1c14 0000    .8..88..........
1f2a0650: 0001 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0660: 0000 0000 0000 0000 0000 0000 0202 0000    ................
1f2a0670: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0680: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0690: 0000 0000 1234 0000 5678 0000 0000 0000    ....4...xV......
1f2a06a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a06b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a06c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a06d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a06e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a06f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0700: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0710: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0720: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0730: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0740: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0750: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0760: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0770: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0780: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0790: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a07a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a07b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a07c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a07d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a07e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a07f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
```

```
=> md.w 0x1f2a0800 0x100
1f2a0800: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0810: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0820: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0830: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0840: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0850: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0860: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0870: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0880: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0890: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a08a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a08b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a08c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a08d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a08e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a08f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0900: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0910: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0920: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0930: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0940: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0950: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0960: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0970: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0980: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a0990: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a09a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a09b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a09c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a09d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a09e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2a09f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
```

```
=> md.w 0x1f206800 0x100
1f206800: 0204 0000 0000 0000 0080 0000 1fff 0000    ................
1f206810: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206820: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206830: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206840: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206850: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206860: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206870: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206880: 0000 0000 0101 0000 0000 0000 0000 0000    ................
1f206890: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2068a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2068b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2068c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2068d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2068e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2068f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206900: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206910: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206920: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206930: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206940: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206950: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206960: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206970: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206980: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f206990: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2069a0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2069b0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2069c0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2069d0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2069e0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
1f2069f0: 0000 0000 0000 0000 0000 0000 0000 0000    ................
```
