# Harvard's HPC Sustainability Dataset
IPMI, DCGM, Slurm, and other logs for researchers to use in their HPC Sustainability research. These data are available for all of the nodes in our three clusters at the Massachusetts Green High Performance Computing Center (MGHPCC). The clusters are Cannon (our primary cluster), FASSE (a secure enclave for higher security projects), and Slurm-Test (our test cluster).

Questions should be directed to Jason Wells: jrwells at fas.harvard.edu.

Service Notes:
- May 31, 2025: Our primary data center, which houses the three clusters, has a yearly outage every year for a few days. We make this into four days so we can do some updates without having to arrange further downtime with our researchers. Importantly, the monitoring server is not in this data center. I may not have the GPU monitoring in place for this event, but IPMI and slurmctld logs should be available. You will be able to see the power down of the clusters on May 31 and June 1 of 2025, and the powerup of the clusters on June 5/6, 2025.

General Notes:
- I was forced to use xz compression. I was really fighting github's file size limitation and had to upgrade to something better than gzip.
- 'xz -T0 -9' reduced the compressed file size 75% and sped it up greatly, FYI.
- 'tar xf <filename>' should handle the decompression the same way. Be prepared to wait (have lunch, etc.).

Weather Notes:
- We're scraping data every 5 minutes from KMAHIGHL4 on Wunderground, which is 1.5 miles from MGHPCC. You can see the data <a href="https://www.wunderground.com/dashboard/pws/KMAHIGHL4">here</a>.

DCGM Notes
- Researchers should consider June 6th as the first full day of DCGM data. Previous days were setup and maintenance days.

IPMI Notes:
- Researchers should consider May 31st as the first full day of IPMI data. Previous days were setup days.

June 2, 2025
- DCGM logs are ready to go but make little sense since everything is powered down. Those logs should start to make sense on the 5th.

May 31, 2025
- Upgraded to xz compression. See note.

May 29, 2025
- We are pushing daily files for all our nodes in three separate clusters up to this Github.
- Within each day's gzip file, are about 1750 files; one for every node we are tracking.
- Each file has a timestamp on a separate line for every time an ipmi sdr was run on that node, followed by the sdr data for that minute.
- We are investigating adding slurm and dcgm logs in the coming days.
