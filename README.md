# cdev_test

Bash script for running simple disk performance tests.

## Requirements
- `fio`
- `jq`
- `smartmontools`

## Usage
```bash
chmod +x cdev_test
./cdev_test [OPTIONS]
```

Example NVMe device test:
```bash
./cdev_test --device=/dev/nvme0n1 --report=report.txt
```

Example file-based test:
```bash
./cdev_test --work-file=./testfile
```

Results are saved to the report file (default `disks_test_report.txt`).

## Included tests
- Sequential read 1M Q1T1
- Sequential write 1M Q1T1
- Random read 4K Q1T1
- Random write 4K Q1T1
- Random read 4K Q32T16
- Random write 4K Q32T16
- Random read latency 4K Q1T1 (average access time)
- Throttling test - continuous write 60s

## License
The code is released under the GNU General Public License version 3.0.
See the `LICENSE` file for details.

