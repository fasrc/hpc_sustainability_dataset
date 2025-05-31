# Harvard's HPC Sustainability Dataset
IPMI, DCGM, Slurm, and other logs for researchers to use in their HPC Sustainability research.

General Notes:
- Sorry for the use of xz compression. I was really fighting github's file size limitation and had to upgrade to something better than gzip.
- 'xz -T0 -9' reduced the compressed file size 75% and sped it up greatly, FYI.
- 'tar xf <filename>' should handle the decompression the same way. Be prepared to wait (have lunch, etc.).

IPMI Notes:
- Researchers should consider May 31st as the first full day of IPMI data. Previous days were setup days.

May 31, 2025
- Upgraded to xz compression. See note.

May 29, 2025
- We are pushing daily files for all our nodes in three separate clusters up to this Github.
- Within each day's gzip file, are about 1750 files; one for every node we are tracking.
- Each file has a timestamp on a separate line for every time an ipmi sdr was run on that node, followed by the sdr data for that minute.
- We are investigating adding slurm and dcgm logs in the coming days.
