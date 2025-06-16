# cdev_test

Skrypt Bash do wykonywania prostych testów wydajności dysków.

## Wymagania
- `fio`
- `jq`
- `smartmontools`

## Użycie
```bash
chmod +x cdev_test
./cdev_test [OPCJE]
```

Przykład testu urządzenia NVMe:
```bash
./cdev_test --device=/dev/nvme0n1 --raport=raport.txt
```

Przykład testu plikowego:
```bash
./cdev_test --work-file=./testfile
```

Wyniki zapisywane są w pliku raportu (domyślnie `disks_test_raport.txt`).

## Licencja
Kod udostępniany jest na licencji GNU General Public License w wersji 3.0.
Szczegóły znajdują się w pliku `LICENSE`.

