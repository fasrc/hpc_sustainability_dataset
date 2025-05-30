# Harvard's HPC Sustainability Dataset
IPMI, DCGM, Slurm, and other logs for researchers to use in their HPC Sustainability research.

IPMI Notes:
- Researchers should consider May 31st as the first full day of IPMI data. Previous days were setup days.

May 29, 2025
- We are pushing daily files for all our nodes in three separate clusters up to this Github.
- Within each day's gzip file, are about 1700 files; one for every node we are tracking.
- Each file has a timestamp on a separate line for every time an ipmi sdr was run on that node.
- We are investigating adding slurm and dcgm logs in the coming days.
