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

## License
The code is released under the GNU General Public License version 3.0.
See the `LICENSE` file for details.

