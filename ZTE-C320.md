Cek versi OLT
```bash
show system-group
```

Cek onu state
```bash
show gpon onu state
```
### Deskripsi Phase State:
| State | Deskripsi |
| --- | --- |
| `offline`   | OLT tidak menemukan ONU karena ONU sedang **Offline**. |
| `logging`   | OLT telah menemukan ONU dan mengukur jarak. |
| `syncMib`   | OLT telah mengukur jarak ke ONU dan sedang melakukan sinkronisasi data. |
| `working`   | Sinkronisasi data selesai, dan service dapat di konfigurasi (**Online**). |
| `LOS`       | Link Fiber antara OLT dan ONU rusak sehingga ONU **Offline** |
| `DyingGasp` | ONU dimaikan |

Melihat ONU yang belum di konfigurasi
```bash
show gpon onu uncfg
```

Cek Detail Config di Interface ke arah onu
```bash
show run interface gpon-onu_x/y/z:a
```
### Deskripsi Parameter:
- **x**: Nomor slot pada OLT.
- **y**: Nomor port pada card OLT di slot.
- **z**: Nomor card OLT.
- **a**: Nomor ONU yang ingin ditampilkan statusnya.
### Contoh Penggunaan:
show run interface gpon-onu_1/1/4:2
