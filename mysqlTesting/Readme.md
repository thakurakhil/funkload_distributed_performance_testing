
## Prepare Data

sysbench --test=oltp --oltp-table-size=1000 --mysql-db=dbtest --mysql-user=root --mysql-password=root prepare

## Test Run

sysbench --test=oltp --oltp-table-size=1000 --oltp-test-mode=complex --num-threads=50 --max-time=60 --mysql-db=dbtest --mysql-user=root --mysql-password=root run
